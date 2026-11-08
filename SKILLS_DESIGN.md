# SKILLS_DESIGN.md - Diseño de las skills de Goat

Diseño de las skills antes de implementarlas. Todas usan solo los servicios ya conectados (Google Docs, Google Calendar y Telegram) y respetan los cinco archivos de configuración (IDENTITY, SOUL, AGENTS, USER y TOOLS).

| Skill | Servicio | Para qué |
|---|---|---|
| planificar-semana | Google Calendar | Organizar la semana de estudio, trabajo y tiempo libre |
| libreta-aprendizaje | Google Docs | Guardar lo aprendido en clase cada semana |
| preguntas-repaso | Google Docs | Repasar lo aprendido con preguntas y soluciones |

---

## Skill 1: planificar-semana

**¿Qué hace?**
Organiza mi semana de estudio, trabajo y tiempo libre y crea los eventos en Google Calendar.

**¿Qué input necesita?**
- Lo que le doy yo: mis horarios fijos de la semana (trabajo y clases), mi objetivo de la semana y cuántas horas quiero dedicar a cada cosa.
- Lo que ya sabe por los 5 archivos:
  - USER.md: trabajo en AC Reformas, hago el bootcamp de 4Geeks y vivo en A Coruña.
  - TOOLS.md: zona horaria Europe/Madrid, 18:00 si no indico hora, duración de 1 hora por defecto, confirmación por Telegram.
  - AGENTS.md y SOUL.md: antes de crear nada me enseña la lista de eventos y espera mi "sí"; no inventa horarios que no le he dado.

**¿Cómo es un buen output?**
- Formato: un evento por bloque, con título claro ("Estudio 4Geeks: TypeScript", "Trabajo AC Reformas", "Tiempo libre"), día, hora de inicio y de fin.
- Dónde aparece: en Google Calendar (cuenta de prueba), y un mensaje en Telegram con el resumen de la semana y los enlaces a los eventos.
- Cómo sabré que funcionó: los eventos aparecen en Calendar en el día y la hora correctos, sin solaparse, y me llega el resumen por Telegram.

---

## Skill 2: libreta-aprendizaje

**¿Qué hace?**
Convierte lo que aprendí en clase durante la semana en un documento de repaso ordenado en Google Docs. Crea un documento nuevo cada semana.

**¿Qué input necesita?**
- Lo que le doy yo: mis notas o un resumen de lo que se dio en clase esa semana (temas, ejemplos, dudas).
- Lo que ya sabe por los 5 archivos:
  - USER.md: hago el bootcamp AI Engineering de 4Geeks y mi objetivo es trabajar como ingeniero de IA.
  - SOUL.md: escribe claro y conciso; si algo de mis notas no está claro, lo dice en vez de suponer.
  - USER.md: no inventa contenido que no se dio en clase.
  - TOOLS.md: crea el documento en HTML básico y lo nombra por el tema.
  - AGENTS.md: me enseña el título y los apartados y espera mi "sí" antes de crearlo.

**¿Cómo es un buen output?**
- Formato: documento titulado "Libreta 4Geeks: <tema principal de la semana>", con cuatro apartados:
  1. Temas vistos.
  2. Conceptos clave (explicación sencilla y un ejemplo de cada uno).
  3. Lo que me costó.
  4. Para repasar.
- Dónde aparece: en Google Docs (cuenta de prueba), y un mensaje en Telegram con el enlace y un resumen de una línea.
- Cómo sabré que funcionó: abro el enlace, el documento tiene los 4 apartados y lo que pone coincide con lo que le conté, sin cosas inventadas.

---

## Skill 3: preguntas-repaso

**¿Qué hace?**
Crea un documento de preguntas de repaso sobre lo aprendido en una semana concreta, con las soluciones al final.

**¿Qué input necesita?**
- Lo que le doy yo: el contenido de la libreta de aprendizaje de esa semana (lo pego en el chat, o lo usa directamente si acaba de crear la libreta en la misma conversación).
- Lo que ya sabe por los 5 archivos:
  - USER.md: hago el bootcamp AI Engineering de 4Geeks; las preguntas son para repasar el bootcamp.
  - USER.md y SOUL.md: no inventa; solo pregunta sobre lo que aparece en la libreta de esa semana.
  - TOOLS.md: crea el documento en HTML básico y lo nombra por el tema.
  - AGENTS.md: antes de crearlo me dice cuántas preguntas hará y sobre qué temas, y espera mi "sí".
  - TOOLS.md: al terminar me avisa por Telegram con el enlace.

**¿Cómo es un buen output?**
- Formato: documento titulado "Preguntas de repaso: <tema de la semana>", con 10 preguntas numeradas (tipo test con 4 opciones o de respuesta corta). Las soluciones van al final, bajo el título "Soluciones: no mirar hasta terminar", separadas de las preguntas por bastante espacio en blanco.
- Dónde aparece: en Google Docs (cuenta de prueba), y un mensaje en Telegram con el enlace.
- Cómo sabré que funcionó: abro el enlace y compruebo que:
  - todas las preguntas tratan sobre lo de esa semana;
  - ninguna pregunta deja ver su respuesta;
  - las soluciones están al final y coinciden con las preguntas.
