# Plantillas de `_tutor/`

Son el punto de partida, no un formulario: sacá las secciones que no apliquen a la materia y agregá las que hagan falta. Lo que importa es que la próxima sesión pueda retomar leyendo solo estos archivos.

## `01-onboarding.md`

```markdown
# Onboarding — <Materia> (<código>)

Fecha: <AAAA-MM-DD>. Fuente: lectura de <carpeta> por <n> subagentes (<cómo se dividió>). Lo marcado **[verificar]** es inferencia o inconsistencia.

## 1. La cátedra
- Docentes, horarios, consultas, campus o canal de avisos.
- Evaluación: cómo se aprueba, fechas u oportunidades, qué se puede llevar al examen (fórmulas, glosario).
- Regla de cobertura: qué temas entran en cada fecha.

### Fechas
| Fecha | Qué |
|---|---|

Orden en que la cátedra da los temas: <tema> (<fecha>) → <tema> → …

### Bibliografía
Oficial (programa): …
En la carpeta: <libro, edición, archivo>. Si se extrajo a `.md`: formato del marcador de página y desfase PDF ↔ libro. Cómo se cita: «<libro>, sección X.Y, p. N».

## 2. Qué evalúa: los modelos de examen
<n> modelos: <id> (<fecha>, oficial o de alumno, con o sin solución). Formato: cantidad de ejercicios, tiempo, puntaje.

| Tema | <modelo 1> | <modelo 2> | … |
|---|---|---|---|

**Estructura tipo del examen:** 1. … 2. …
**Nunca aparecen:** …
**Errores en los enunciados:** …

## 3. Cómo da los temas la cátedra
| Material (diapositiva, apunte) | Págs. | Centro | Al pasar | Ejemplos numéricos |
|---|---|---|---|---|

Terminología propia de la cátedra: …
**Huecos entre el material y el examen:** lo que el examen pide y el material no explica.

## 4. Guías, ejercicios, laboratorios y herramientas
- Guías y ejercicios: qué hay, qué está resuelto, cuáles son tipo examen.
- Glosario o fórmulas permitidas: qué trae y qué no.
- Laboratorios y herramientas (software, simuladores, máquinas virtuales).

## 5. Respuestas del estudiante (paso 1.2, <fecha>)
- Examen a preparar: <fecha> (<n> días).
- Temario: …
- Libros: principal y de apoyo.
- Modelos de examen: cuáles se usan.
- Tiempo disponible: <h> por día → <total> h.

## 6. Inconsistencias detectadas
1. …
```

## `02-esqueleto-plan.md`

```markdown
# Esqueleto del plan — <examen>, <fecha>

Estado: **esqueleto** (paso 2.1). El contenido de cada módulo se completa en el 2.3, después del diagnóstico. Base: `01-onboarding.md`.

## Marco
- Hoy <fecha>. Último día de estudio: <fecha>. **<n> días × <h> h = <total> h.**
- Temario asumido: … (lo que está en reserva y cuándo se activa).
- Orden de recorrido = orden de la cátedra: <módulo> → <módulo> → … → Modelos de examen.
- Pesos según los modelos de examen: <módulo> ~<x> %, …

## Módulos
| # | Módulo | Prerrequisitos que se cubren | Qué entra (según los modelos) | Horas tentativas |
|---|---|---|---|---|

## Ciclo de cada módulo
1. Parrilla de entrada: qué sabe ya; decide cuánto se lee.
2. Mandar a leer: sección y página exactas.
3. Resolver a mano: fuentes de ejercicios.
4. Simular, si suma y hay tiempo.
5. Parrilla de cierre: con el formato del examen.

Proporción esperada: leer ~<x> %, resolver a mano ~<x> %, parrillas ~<x> %, simular ~<x> %.

## Calendario tentativo (se recalcula cada día)
| Días | Módulo |
|---|---|

## Reglas
- Si un módulo se atrasa, qué se recorta primero (lo «al pasar») y qué nunca (los ejercicios tipo examen).
- Si sobra tiempo, qué se agrega.
```

## `03-diagnostico.md`

```markdown
# Diagnóstico — <fecha>

## Módulo <n>: <nombre>
| Pregunta | Respuesta | ¿Bien? |
|---|---|---|

Conclusión: qué sabe, qué no, cuánto hay que leer y practicar. Ajuste de horas: …
```

## `04-plan.md`

```markdown
# Plan — <examen>, <fecha>

## Módulo <n>: <nombre> — <h> h, <días>
- **Parrilla de entrada:** …
- **Leer:** <libro>, sección X.Y, p. N–M (para qué).
- **Resolver a mano:** <fuente>, ejercicios …
- **Simular:** <tarea>, qué medir y qué traer.
- **Parrilla de cierre:** …
```

## `bitacora.md`

```markdown
# Bitácora

## <AAAA-MM-DD> (<día>) — sesión <n>: <tema>
- Hecho: …
- Horas del estudiante: <h> (plan: <h>).
- Agregado o descartado: … (y por qué).
- Plazos: <sin cambios | recálculo>. Quedan <n> días = <h> h.
- Pendientes del estudiante: …
- **Próximo paso:** …
```

## `preferencias.md`

```markdown
# Preferencias del estudiante

- <AAAA-MM-DD>: <criterio>, por ejemplo «prefiere los ejercicios antes que la lectura», «no hay tiempo de laboratorio los fines de semana».
```
