# Cómo contribuir

## Qué cambios entran

La skill la usan estudiantes de distintas materias, así que todo lo que se agrega tiene que servir para **cualquier materia**:

- Escribilo en abstracto: «guías de otras unidades», «modelos de examen», «el libro de referencia». No nombres una materia, temas, archivos, docentes ni fechas.
- Si hace falta un ejemplo, que sea uno que cualquiera entienda (los de la skill usan la ley de Ohm y el pasaje de decimal a binario).
- Lo que es preferencia personal no va acá: va en `_tutor/preferencias.md` de cada uno.

Antes de escribir mucho, si el cambio es grande o cambia cómo funciona el tutor, abrí un issue para charlarlo.

## Cómo proponer un cambio

1. Hacé un fork del repo y cloná tu fork **fuera de Google Drive, OneDrive o Dropbox** (git y la sincronización de esas carpetas se llevan mal).
2. Creá una rama: `git switch -c mejora-parrillas`.
3. Editá `plugins/tutor-examen/skills/tutor-examen/SKILL.md` (o las plantillas).
4. Probalo en una materia real, cargando el plugin desde tu copia:

   ```
   claude --plugin-dir <ruta-a-tu-copia>/plugins/tutor-examen
   ```

5. Validá que el plugin y el marketplace estén bien formados:

   ```
   claude plugin validate --strict .
   claude plugin validate --strict plugins/tutor-examen
   ```

6. Agregá una línea en `CHANGELOG.md`, bajo **Sin publicar**.
7. Abrí el pull request contando qué problema viste y cómo lo probaste.

No cambies el número de versión: eso se hace al publicar.

## Publicar una versión (mantenedor)

Las instalaciones se actualizan solo cuando cambia `version` en `plugin.json`, así que mezclar un PR no le llega a nadie hasta que se publica.

1. Subí la versión en `plugins/tutor-examen/.claude-plugin/plugin.json` ([semver](https://semver.org/lang/es/): parche para correcciones, menor para criterios nuevos, mayor si cambia la carpeta `_tutor/` de forma incompatible).
2. En `CHANGELOG.md`, pasá lo de **Sin publicar** a una sección con la versión y la fecha.
3. Commit, y marcá la versión: `claude plugin tag plugins/tutor-examen` (crea la etiqueta `tutor-examen--v<versión>`).
4. `git push --follow-tags`.

## Agregar otra skill

1. Creá `plugins/<nombre>/.claude-plugin/plugin.json` y `plugins/<nombre>/skills/<nombre>/SKILL.md`, siguiendo el formato de `tutor-examen`.
2. Agregá su entrada en `.claude-plugin/marketplace.json`.
3. Validá con `claude plugin validate --strict .` y sumá la carpeta al paso de validación de `.github/workflows/validar.yml`.
