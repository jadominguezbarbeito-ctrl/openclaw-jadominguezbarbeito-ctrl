# TOOLS.md - Herramientas disponibles y cómo usarlas

Todas las herramientas pasan por Zapier MCP y usan la cuenta de prueba de 4Geeks. Solo puedo usar lo que aparece en este archivo.

## Google Docs
- **Acción:** crear documento desde texto (`google_docs_create_document_from_text`).
- **Cuándo usarlo:** cuando Jesús pida un documento, informe, presupuesto, resumen o cualquier texto para guardar o compartir.
- **Nombre del documento:** el tema del que trata, sin fecha ni prefijos. Ejemplo: `Presupuesto baño Pérez`.
- **Formato:** el contenido se envía en HTML básico (`<h1>`, `<h2>`, `<p>`, `<ul><li>`, `<strong>`). Nunca texto plano sin etiquetas.

## Google Calendar
- **Acción:** crear evento con texto rápido (`google_calendar_quick_add_event`).
- **Cuándo usarlo:** cuando Jesús pida agendar una cita, visita, reunión o recordatorio.
- **Zona horaria:** siempre Europe/Madrid (hora de España).
- **Si no indica hora:** a las 18:00.
- **Duración por defecto:** 1 hora. Escribo siempre la hora de inicio y de fin en el texto. Ejemplo: `Visita obra Pérez el 12 de noviembre de 18:00 a 19:00`.

## Telegram
- Es el canal donde hablo con Jesús.
- **Confirmación al terminar una tarea:** aviso por Telegram con el enlace al documento o evento y un resumen de una o dos líneas de lo que he hecho.

## No disponible: no usar
- **Gmail:** está registrado pero sin cuenta conectada. No lo uso.
- **Google Drive, Google Tasks y cualquier otro servicio:** no están habilitados. No los uso.
- Nunca lanzo flujos de autorización (OAuth de Google u otros) ni conecto cuentas nuevas.
- Nunca uso `enable_zapier_action`, `disable_zapier_action` ni `discover_zapier_actions` para activar o cambiar acciones sin que Jesús lo pida expresamente.
