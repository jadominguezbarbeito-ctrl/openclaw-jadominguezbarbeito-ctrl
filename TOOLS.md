# TOOLS.md - Herramientas disponibles y cómo usarlas

Todas las herramientas pasan por Zapier MCP y usan la cuenta de prueba de 4Geeks. Solo puedo usar lo que aparece en este archivo.

## Google Docs
- **Acción:** crear documento desde texto (`google_docs_create_document_from_text`).
- **Cuándo usarlo:** cuando Jesús pida un documento, informe, presupuesto, resumen o cualquier texto para guardar o compartir.
- **Nombre del documento:** el tema del que trata, sin fecha ni prefijos. Ejemplo: `Presupuesto baño Pérez`.
- **Formato:** el contenido se envía en HTML básico (`<h1>`, `<h2>`, `<p>`, `<ul><li>`, `<strong>`). Nunca texto plano sin etiquetas.

## Google Calendar
- **Acción:** crear evento detallado con `execute_zapier_write_action` y la acción `detailed_event` de Google Calendar. Nunca uses `google_calendar_quick_add_event`: pone mal las fechas.
- **Cuándo usarlo:** cuando Jesús pida agendar una cita, visita, reunión o recordatorio.
- **Zona horaria:** siempre Europe/Madrid (hora de España).
- Calendario: el principal ("primary") de la cuenta conectada en Zapier. No preguntes el ID.
- **Si no indica hora:** a las 18:00.
- **Duración por defecto:** 1 hora. Paso siempre fecha, hora de inicio y hora de fin como campos separados, en formato ISO y zona Europe/Madrid. Ejemplo: "Visita obra Pérez", inicio 2026-11-12T18:00, fin 2026-11-12T19:00.

## Telegram
- Es el canal donde hablo con Jesús.
- **Confirmación al terminar una tarea:** aviso por Telegram con el enlace al documento o evento y un resumen de una o dos líneas de lo que he hecho.

## No disponible: no usar
- **Gmail:** está registrado pero sin cuenta conectada. No lo uso.
- **Google Drive, Google Tasks y cualquier otro servicio:** no están habilitados. No los uso.
- Nunca lanzo flujos de autorización (OAuth de Google u otros) ni conecto cuentas nuevas.
- Nunca uso `enable_zapier_action`, `disable_zapier_action` ni `discover_zapier_actions` para activar o cambiar acciones sin que Jesús lo pida expresamente.
