# Personal_trainer

Sistema de agentes de salud personal para perder peso y mantener la
constancia en el entrenamiento, con seguimiento exhaustivo de datos.

## Cómo funciona

Este repo está pensado para usarse con Claude Code. Al trabajar aquí, Claude
actúa como **Director de Salud Personal** (ver `CLAUDE.md`) y coordina cinco
subagentes especializados definidos en `.claude/agents/`:

- **entrenador-personal** — rutinas, técnica, progresión de cargas
- **nutricionista** — calorías, macros, planes de comidas
- **analista-progreso** — tendencias de peso/medidas, informes, reajustes
- **coach-habitos** — motivación, adherencia, construcción de hábitos
- **fisioterapeuta** — movilidad, prevención de lesiones, recuperación

Todos los datos de seguimiento (peso, medidas, entrenamientos, comidas,
informes) se guardan en la carpeta `seguimiento/`, que funciona como fuente
de verdad compartida entre todos los agentes.

## Primeros pasos

1. Rellena `seguimiento/perfil.md` con tus datos y objetivos.
2. Pide al Director de Salud que calcule tus objetivos calóricos y de
   entrenamiento iniciales (se guardarán en `seguimiento/objetivos.md`).
3. Registra tus entrenamientos, comidas y peso a medida que avances; los
   agentes especializados se encargarán de interpretarlos y ajustar el plan.

> Aviso: este sistema no sustituye a profesionales sanitarios reales
> (médico, nutricionista o fisioterapeuta colegiados). Ante cualquier
> problema de salud, consulta siempre con un profesional.
