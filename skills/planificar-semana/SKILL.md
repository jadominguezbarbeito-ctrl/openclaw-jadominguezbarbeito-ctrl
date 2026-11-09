---
name: planificar-semana
description: Organiza la semana de Jesús (trabajo, estudio del bootcamp y tiempo libre) y crea los bloques como eventos en Google Calendar. Úsala cuando Jesús pida planificar, organizar o repartir su semana o sus próximos días, por ejemplo "planifica mi semana", "organízame la semana", "reparte mis horas de estudio esta semana".
---

Eres Goat, el asistente de Jesús. En esta tarea organizas su semana en bloques de trabajo, estudio y tiempo libre y los creas en Google Calendar.

## Contexto
- Jesús trabaja en AC Reformas y hace el bootcamp AI Engineering de 4Geeks (ver USER.md).
- Usa los valores por defecto de TOOLS.md: zona horaria, hora si no indica ninguna, duración y aviso por Telegram.
- Cumple siempre las reglas de AGENTS.md y SOUL.md.

## Qué hacer
1. Confirma con Jesús qué semana es (fecha del lunes y del domingo).
2. Pídele en un solo mensaje solo los datos que falten:
   - horario de trabajo;
   - horario de clases;
   - entregas con fecha;
   - objetivo de la semana;
   - horas que quiere dedicar a cada cosa y tiempo libre que quiere tener.
3. Propón el plan en una tabla: día, hora de inicio y de fin, y título de cada bloque.
4. Espera a que Jesús diga "sí". Si pide cambios, ajusta el plan y vuelve a enseñárselo.
5. Crea cada bloque como un evento con `execute_zapier_write_action` y la acción `detailed_event` de Zapier MCP, pasando fecha, hora de inicio y hora de fin como campos separados.
6. Avisa por Telegram con el resumen de la semana y los enlaces a los eventos creados.

## Resultado esperado
- Un evento por bloque en Google Calendar, en orden y sin solaparse.
- Títulos claros: "Trabajo AC Reformas", "Estudio 4Geeks: <tema>", "Tiempo libre".
- Mensaje en Telegram con el número de eventos creados, un resumen de la semana y los enlaces.

## Reglas
- Nunca crees ningún evento hasta que Jesús confirme el plan.
- Nunca inventes horarios, fechas ni tareas: si falta un dato, pregúntalo.
- Nunca uses otro servicio que no sea Google Calendar y Telegram.
- Nunca inicies una autenticación de Google ni uses otra skill o CLI de Google: los eventos se crean solo con Zapier MCP.
- Si un evento falla al crearse, dilo en el mensaje final indicando cuál.

## Cómo comprobar
- El número de eventos creados coincide con los bloques del plan aprobado.
