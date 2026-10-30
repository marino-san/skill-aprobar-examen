# skill-aprobar-examen

Skills de [Claude Code](https://claude.com/claude-code) para preparar y aprobar exámenes de la facultad. Por ahora trae una:

**tutor-examen**: un tutor que lee la carpeta de la materia (programa, diapositivas, guías, libros, modelos de examen), entiende cómo es la cátedra y qué evalúa, te hace las preguntas que le faltan, te toma un diagnóstico y arma un plan de trabajo hasta el día del examen. Después lo lleva sesión a sesión: parrillas de preguntas, lecturas exactas del libro (sección y página), ejercicios para resolver a mano y prácticas de laboratorio, y recalcula los plazos según cómo vas rindiendo.

Sirve para cualquier materia. Lo de cada materia lo guarda en una carpeta `_tutor/` dentro de la carpeta de esa materia, así que la skill es la misma para todos y cada uno tiene su propio plan.

## Instalar

Desde una terminal (una sola vez):

```
claude plugin marketplace add marino-san/skill-aprobar-examen
claude plugin install tutor-examen@skill-aprobar-examen
```

O desde adentro de Claude Code, con `/plugin` → *Marketplaces* → agregar `marino-san/skill-aprobar-examen`, y después instalar `tutor-examen`.

## Usar

1. Juntá el material de la materia en una carpeta (programa, cronograma, diapositivas, guías, libros en PDF, modelos de examen). Cuanto más completo, mejor el plan.
2. Abrí Claude Code en esa carpeta.
3. Decile algo como «quiero preparar el parcial de Análisis II» o «arrancá el tutor».

La primera sesión es el onboarding: lee todo y te pregunta lo que falta. En las siguientes, decí «seguimos con el tutor» y retoma donde quedaron.

## Actualizar

Las mejoras llegan a todos cuando se publica una versión nueva. Para traerla:

```
claude plugin marketplace update skill-aprobar-examen
claude plugin update tutor-examen@skill-aprobar-examen
```

Y reiniciá Claude Code. Si no querés acordarte, activá la actualización automática del marketplace desde `/plugin` → *Marketplaces*.

Tu carpeta `_tutor/` no se toca al actualizar.

## Proponer una mejora

Si se te ocurre algo que le serviría a cualquiera que prepare un examen, abrí un pull request. Está explicado en [CONTRIBUTING.md](CONTRIBUTING.md). Si no usás git, abrí un [issue](https://github.com/marino-san/skill-aprobar-examen/issues) contando la idea.

Lo que es solo tuyo (cómo te gusta estudiar) no hace falta proponerlo: decíselo al tutor y lo guarda en `_tutor/preferencias.md`.

## Qué hay en el repo

```
.claude-plugin/marketplace.json     el catálogo: qué plugins trae este repo
plugins/
  tutor-examen/
    .claude-plugin/plugin.json      nombre y versión del plugin
    skills/tutor-examen/
      SKILL.md                      las instrucciones del tutor
      references/plantillas.md      plantillas de los archivos de _tutor/
CHANGELOG.md                        qué cambió en cada versión
CONTRIBUTING.md                     cómo proponer cambios y publicar versiones
```

Para sumar otra skill, se agrega otra carpeta en `plugins/` y su entrada en `marketplace.json` (ver [CONTRIBUTING.md](CONTRIBUTING.md#agregar-otra-skill)). Quien ya agregó el marketplace la ve sin hacer nada más.

## Licencia

[MIT](LICENSE).
