# NexoSolutions — Sistema NFC + QR para inmobiliarias

NexoSolutions conecta carteles físicos de propiedades con fichas web individuales mediante NFC y código QR, con acceso directo al WhatsApp de la inmobiliaria.

## Estado del proyecto

MVP estático en construcción. El enfoque inicial es servicio gestionado: NexoSolutions publica y mantiene manualmente las fichas; la inmobiliaria proporciona y aprueba el contenido. La autogestión se evaluará después de validar el piloto. El modelo comercial previsto separa el alta inicial del mantenimiento recurrente; precios y alcance comercial siguen pendientes de validación.

## Documentación principal

- [Documento maestro de continuidad y auditoría](docs/NEXOSOLUTIONS_DOCUMENTO_MAESTRO_CONTINUIDAD.md)
- [Landing del servicio](index.html)
- [Ficha demo independiente](propiedades/casa-demo/index.html)
- [Plantilla de venta](plantillas/venta.html)
- [Plantilla de alquiler](plantillas/alquiler.html)

## Demo pública prevista

- Landing: https://sprightly-creponne-dc7e51.netlify.app/
- Ficha de demostración: https://sprightly-creponne-dc7e51.netlify.app/propiedades/casa-demo/

Las URLs anteriores corresponden al sitio Netlify configurado previamente. Verificar el último despliegue antes de asumir que reflejan la última versión de `main`.

## Flujo del MVP

1. El cartel muestra NFC y QR.
2. Ambos abren la misma URL estable de la ficha de la propiedad.
3. La ficha presenta datos y fotos confirmados.
4. El botón de WhatsApp inicia el contacto con la inmobiliaria.

El QR de acceso no debe repetirse dentro de la ficha; eso crea un recorrido redundante. No publicar fichas con marcadores de plantilla, datos ficticios o WhatsApp sin probar.

## Alcance actual

Incluye páginas estáticas, fichas individuales, plantillas manuales de venta y alquiler y gestión inicial por NexoSolutions. No incluye base de datos, panel de administración, CRM, aplicación móvil ni analítica avanzada.

## Validación

Objetivo inicial: piloto con 3 inmobiliarias de San Carlos, Maldonado o Punta del Este, con 1–2 propiedades por inmobiliaria. No se prometen ventas ni resultados garantizados. Consultar el documento maestro para riesgos, decisiones, checklist y próximos pasos.
