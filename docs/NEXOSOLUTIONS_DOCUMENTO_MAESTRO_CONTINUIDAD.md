# NexoSolutions — Documento maestro de continuidad
**Proyecto:** NexoSolutions — Sistema NFC + QR para inmobiliarias  
**Versión:** 1.0  
**Fecha de auditoría documental:** 17 de octubre de 2026  
**Repositorio:** https://github.com/PocketBlack/nexosolutions-nfc  
**Rama de trabajo:** `main`  
**Estado:** MVP estático en construcción; validación comercial pendiente.

> Este documento consolida decisiones, activos, estado comprobado, riesgos y próximos pasos. Distingue lo implementado de lo planificado. No implica que se haya probado cada URL, el despliegue más reciente ni una etiqueta NFC física en esta auditoría.

---

## 1. Resumen ejecutivo

NexoSolutions propone conectar el cartel físico de una propiedad con una ficha web individual mediante **NFC y QR**. Ambos accesos deben abrir la misma URL estable de esa propiedad. La ficha presenta información útil y un botón de contacto directo por WhatsApp de la inmobiliaria.

El propósito inicial no es garantizar ventas ni reemplazar el trabajo comercial de la inmobiliaria. Es reducir pasos entre ver el cartel, conocer la propiedad y consultar.

**Decisión de producto:** empezar como servicio gestionado por NexoSolutions para aprender de clientes reales y validar disposición a pagar. Luego, si la demanda lo justifica, desarrollar una herramienta autónoma para que cada inmobiliaria gestione sus propias fichas. El mantenimiento será una oferta recurrente separada del alta/instalación inicial.

## 2. Modelo de negocio y monetización

### 2.1 Modelo por etapas

1. **MVP gestionado:** NexoSolutions configura la ficha, publica, vincula QR/NFC y realiza cambios acordados. La inmobiliaria entrega y aprueba los datos y recibe las consultas.
2. **Servicio recurrente:** ofrecer un plan de mantenimiento periódico que cubra un alcance explícito (por ejemplo, soporte, cambios de contenido dentro de límites acordados, comprobaciones técnicas y gestión de publicación). El alcance, la frecuencia, los tiempos de respuesta y el precio aún están **por definir**.
3. **Autogestión:** cuando haya evidencia de demanda y uso recurrente, evaluar un panel autenticado para que las inmobiliarias creen, editen, publiquen, desactiven y retiren sus fichas. Este desarrollo no forma parte del MVP actual.
4. **Mantenimiento de la herramienta:** puede ofrecerse como servicio adicional o plan diferenciado si se construye la plataforma autónoma.

### 2.2 Principio comercial

No depender exclusivamente de un pago único de instalación. El alta inicial remunera la configuración e implementación; la cuota recurrente remunera el servicio continuo que se acuerde. El cliente no debe recibir una promesa de mantenimiento ilimitado por un pago único.

No se ha definido aún:
- precio de alta/instalación;
- cuota mensual o anual;
- límites de fichas activas, cambios, soporte o almacenamiento;
- costo y propiedad de la placa física;
- impuestos, condiciones de pago o política de cancelación;
- si habrá paquetes por cantidad de propiedades.

No inventar precios ni prometer retorno de inversión. Validar el problema, el interés y la disposición a pagar antes de fijar tarifas.

### 2.3 Hipótesis a validar con clientes

- Las inmobiliarias usan carteles físicos y reciben consultas originadas por personas que los ven.
- NFC + QR y una ficha móvil mejoran el acceso a la información y al contacto.
- Las inmobiliarias valoran que NexoSolutions administre las fichas al principio.
- Están dispuestas a pagar por implementación y por continuidad/mantenimiento.
- Hay interés suficiente para justificar después una herramienta de autogestión.

## 3. Cliente y piloto

**Mercado inicial:** inmobiliarias de San Carlos, Maldonado y Punta del Este, Uruguay.  
**Piloto objetivo:** 3 inmobiliarias; 1–2 propiedades reales por inmobiliaria.  
**Canal inicial:** contactos y negocios de la zona, priorizando conversaciones directas y demostración.

No consta en este documento que una inmobiliaria haya aceptado participar ni que se haya enviado una propuesta comercial. La página de Facebook compartida como posible contacto (`buysaninmobiliaria`) sigue siendo un prospecto por validar, no un cliente confirmado.

### Preguntas de validación
1. ¿Colocan carteles físicos en las propiedades?
2. ¿Reciben consultas de personas que descubren la propiedad desde la calle?
3. ¿Cómo comparten hoy fotos, precio, características y contacto?
4. ¿Les resulta útil abrir una ficha desde NFC o QR?
5. ¿Probarían el sistema con una propiedad real?
6. ¿Qué esperan que incluya el alta y qué mantenimiento recurrente pagarían?
7. ¿Quién actualizará precio, disponibilidad y condiciones, y con qué urgencia?

## 4. Recorrido funcional acordado

1. La inmobiliaria facilita información y fotos autorizadas, número de WhatsApp y referencia de la propiedad.
2. NexoSolutions crea una ficha web individual y revisa los datos con la inmobiliaria.
3. Se publica la ficha en una URL estable.
4. El QR impreso en la placa y la etiqueta NFC se configuran para apuntar **a la misma URL de la ficha**.
5. El interesado acerca el móvil a NFC o escanea el QR.
6. La ficha muestra información del inmueble y un CTA para iniciar una consulta por WhatsApp.
7. La inmobiliaria responde y gestiona la oportunidad comercial.
8. NexoSolutions actualiza o despublica la ficha cuando lo solicite la inmobiliaria, según el acuerdo de servicio.

**Importante:** no poner el QR de acceso a la propiedad dentro de esa misma ficha: produciría un recorrido redundante o un bucle. El QR físico abre la ficha; el botón dentro de la ficha abre WhatsApp.

## 5. Alcance del MVP

### Incluido
- Páginas web estáticas y adaptables a móvil.
- Una URL diferenciada por propiedad.
- Acceso por QR y NFC a la misma ficha.
- Plantillas separadas para venta y alquiler.
- Datos y fotos proporcionados o autorizados por la inmobiliaria.
- CTA a WhatsApp con número autorizado y mensaje predefinido.
- Gestión manual de cambios y publicación por NexoSolutions.
- Pruebas básicas de navegación y escaneo antes de entregar.

### Excluido por ahora
- Base de datos y panel de administración.
- Cuentas de usuario, permisos y autenticación.
- CRM, seguimiento de leads y analítica avanzada.
- Aplicación móvil.
- Integración automática con portales inmobiliarios.
- Generación automática de fichas desde formularios.
- Recorridos 360° como requisito (pueden incorporarse si existen y aportan valor).
- Garantías de ventas, visitas o resultados comerciales.

No ampliar el alcance hasta validar uso real y disposición a pagar.

## 6. Organización técnica prevista

Repositorio único y sitio estático de bajo costo. Cada ficha se publica como un directorio independiente. La estructura objetivo propuesta es:

```text
/
├── index.html
├── README.md
├── docs/
│   └── NEXOSOLUTIONS_DOCUMENTO_MAESTRO_CONTINUIDAD.md
├── plantillas/
│   ├── venta.html
│   └── alquiler.html
├── propiedades/
│   └── casa-demo/
│       └── index.html
└── inmobiliarias/
    └── <slug-inmobiliaria>/
        └── propiedades/
            └── <slug-propiedad>/
                └── index.html
```

La estructura bajo `inmobiliarias/` es una convención futura recomendada; todavía no se ha migrado la demo existente ni se ha creado esa estructura para clientes reales.

### Infraestructura conocida
- GitHub: `PocketBlack/nexosolutions-nfc`, rama `main`.
- Netlify: sitio reportado como `sprightly-creponne-dc7e51.netlify.app`.
- URL prevista para la landing: https://sprightly-creponne-dc7e51.netlify.app/
- URL de la ficha demo: https://sprightly-creponne-dc7e51.netlify.app/propiedades/casa-demo/

El estado de despliegue más reciente no fue comprobado en esta auditoría documental. El último estado previamente reportado indicaba publicación automática desde `main`, con commit `088d041`; después se añadieron plantillas. Hay que confirmar en Netlify qué commit está publicado antes de afirmar que la versión más reciente está en producción.

## 7. Auditoría del repositorio — estado observado

Archivos inspeccionados en `main`:
- `README.md`
- `index.html`
- `propiedades/casa-demo/index.html`
- `plantillas/venta.html`
- `plantillas/alquiler.html`

### `index.html` — landing de servicio
- Existe una landing estática con explicación del servicio y una demostración integrada.
- Los controles cambian entre la sección del servicio y la ficha demo dentro del mismo documento.
- La ilustración del QR de la landing es un patrón visual de muestra, no un código QR funcional para producción.
- Debe comprobarse que el usuario puede llegar con claridad a la ficha pública independiente y que no se confunda una demo integrada con una ficha real.

### `propiedades/casa-demo/index.html` — ficha independiente
- Existe una ficha móvil con datos ficticios claramente indicados, precio de ejemplo, características, descripción y botón de WhatsApp.
- `PROPERTY_URL` apunta a la URL pública prevista de la ficha.
- El QR se genera usando un servicio externo (`api.qrserver.com`) y dirige a esa URL.
- El número de WhatsApp está vacío; el botón avisa que falta configurarlo.
- Imágenes y datos son ilustrativos, no corresponden a una oferta inmobiliaria real.
- La generación del QR depende de un servicio de terceros y de conectividad. Evaluar si conviene guardar un QR generado durante el alta, sin bloquear el piloto por anticipado.
- El usuario confirmó previamente que el QR abre correctamente desde su móvil. No se considera probado en esta auditoría que siga funcionando después del último cambio/despliegue.

### `plantillas/venta.html` y `plantillas/alquiler.html`
- Ambas plantillas existen y usan marcadores `{{...}}` que deben reemplazarse antes de publicar.
- Los espacios de fotos son marcadores visuales; no son todavía una rutina de carga de imágenes.
- Los enlaces de WhatsApp requieren un número internacional solo con dígitos y un texto correctamente codificado para URL.
- No se debe publicar una ficha con marcadores sin sustituir, datos incompletos presentados como confirmados o enlaces rotos.
- La plantilla de alquiler incluye costos, garantías, requisitos y condiciones; completar solo con información confirmada por la inmobiliaria.
- Las plantillas son un punto de partida, no un generador automático ni un CMS.

### Riesgos técnicos y operativos abiertos
1. No hay un proceso automatizado de publicación; el reemplazo de marcadores es manual.
2. No hay una lista de control de QA formal aplicada automáticamente.
3. No se verificó en esta auditoría el último deploy de Netlify.
4. El WhatsApp real de la demo no está configurado.
5. No se ha registrado ni probado una etiqueta NFC física.
6. No se ha probado el flujo completo con una propiedad real y una inmobiliaria real.
7. La política de privacidad, autorización de fotos, actualización de precios y retirada de fichas debe acordarse con cada cliente.
8. Los términos comerciales de mantenimiento, cancelación, propiedad del soporte físico y continuidad de URLs aún están por definir.

## 8. Política de contenido y responsabilidades

**La inmobiliaria:**
- aporta y autoriza fotos, descripción, precio, ubicación pública, características, disponibilidad, costos y condiciones;
- confirma que tiene derecho a publicar el contenido;
- designa el número de WhatsApp;
- revisa y aprueba la ficha antes de su publicación;
- notifica cambios de precio, disponibilidad o condiciones;
- gestiona las consultas y la relación con potenciales compradores/inquilinos.

**NexoSolutions:**
- configura y publica la ficha dentro del alcance acordado;
- configura y verifica QR/NFC cuando corresponda;
- mantiene la infraestructura y realiza cambios incluidos en el plan contratado;
- no garantiza que una ficha genere consultas, visitas o ventas;
- no debe publicar datos no confirmados ni mantener como vigente una ficha retirada cuando recibe una solicitud válida de baja.

### Baja y continuidad
Antes de contratar, dejar por escrito:
- qué sucede con la ficha y la URL al cancelar;
- cuánto tiempo se mantiene publicada tras finalizar el servicio;
- si se entrega una copia del contenido;
- quién conserva la placa física;
- qué elementos técnicos y plantillas siguen siendo propiedad de NexoSolutions;
- qué ocurre con enlaces QR/NFC si la ficha se despublica.

No prometer una URL “para siempre”. La estabilidad depende de mantener el dominio, el hosting y la cuenta operativos.

## 9. Política de precios — pendiente de validación

La propuesta comercial debe separar claramente:
- **Alta/implementación:** preparación inicial, publicación, configuración de contactos y prueba del acceso.
- **Mantenimiento recurrente:** alcance definido y cobro periódico.
- **Extras:** cambios fuera del límite, nuevas fichas, fotografía, video, placa física, urgencias u otros trabajos, solo si se deciden y presupuestan.

La cuota no se justifica por el valor de venta de la propiedad, sino por el servicio continuo entregado. No se ha acordado cobrar comisión por la venta ni porcentaje del precio del inmueble; no presentarlo como parte del modelo sin una decisión explícita posterior.

## 10. Estado del proyecto

| Área | Estado | Evidencia / nota |
|---|---|---|
| Propuesta NFC + QR | Definida | Cartel → ficha → WhatsApp |
| MVP estático | En construcción | Landing y ficha demo en repo |
| Plantilla venta | Creada, no validada para producción | Marcadores manuales |
| Plantilla alquiler | Creada, no validada para producción | Marcadores manuales |
| QR demo | Validado previamente por el usuario | Requiere revalidación tras cambios |
| Etiqueta NFC física | Pendiente | No comprada ni probada según el estado conocido |
| WhatsApp de demo | Pendiente | Número vacío |
| Deploy más reciente | Pendiente de verificar | Confirmar commit publicado en Netlify |
| Piloto con inmobiliarias | Pendiente | Objetivo: 3 inmobiliarias, 1–2 propiedades cada una |
| Precio de alta y cuota | Pendiente | No inventar importes |
| Acuerdo de servicio | Pendiente | Responsabilidades, mantenimiento y bajas |
| Autogestión | Futura | Solo tras validar demanda recurrente |

## 11. Plan de trabajo priorizado

### Fase 1 — estabilizar y auditar la demo
1. Confirmar el commit desplegado en Netlify y revisar la URL pública.
2. Probar en móvil: landing, acceso a ficha independiente, QR, navegación y tamaños.
3. Verificar que ningún QR de muestra se confunda con un QR listo para imprimir.
4. Dejar el WhatsApp como pendiente explícito hasta recibir un número autorizado.
5. Completar una ficha de prueba con contenido ficticio controlado y verificar la sustitución de marcadores.
6. Crear y usar una lista de control de QA.

### Fase 2 — validación comercial
1. Contactar prospectos de la zona con una demostración breve.
2. Confirmar que utilizan carteles y entender su flujo actual.
3. Solicitar una prueba con una propiedad real y aprobación de contenido.
4. Preguntar por disposición a pagar por implementación y mantenimiento, sin fijar precios arbitrarios.
5. Registrar feedback, objeciones y resultado de cada conversación.

### Fase 3 — piloto
1. Incorporar 3 inmobiliarias, con 1–2 propiedades cada una, si aceptan.
2. Crear URLs estables y fichas revisadas.
3. Generar el QR de cada ficha y registrar la etiqueta NFC con la misma URL.
4. Probar ambos accesos en móviles compatibles y comprobar el CTA de WhatsApp.
5. Medir operativamente errores, consultas reportadas por la inmobiliaria, cambios solicitados y tiempo de mantenimiento. No atribuir ventas al sistema sin evidencia.

### Fase 4 — decidir el siguiente producto
Revisar evidencia del piloto antes de invertir en panel, base de datos o automatización. Diseñar autogestión solo si las inmobiliarias la necesitan y el ingreso recurrente puede sostener el costo.

## 12. Checklist de publicación de una ficha

- [ ] Nombre y referencia interna de propiedad definidos.
- [ ] Venta o alquiler correctamente indicado.
- [ ] Precio, moneda y disponibilidad confirmados.
- [ ] Ubicación pública revisada para no exponer información no autorizada.
- [ ] Fotos autorizadas y optimizadas para móvil.
- [ ] Dormitorios, baños, áreas, cochera y características confirmados.
- [ ] Costos, impuestos, gastos comunes, garantías y requisitos completados cuando corresponda; no inventar datos.
- [ ] Descripción revisada y aprobada por la inmobiliaria.
- [ ] Número de WhatsApp autorizado y probado.
- [ ] Mensaje de WhatsApp URL-encoded y con referencia de la propiedad.
- [ ] URL estable abierta desde una ventana privada y desde móvil.
- [ ] QR escaneado desde otro dispositivo y verificado que abre esa misma URL.
- [ ] NFC programado como enlace URI a esa misma URL y probado en un móvil compatible.
- [ ] La ficha no contiene marcadores `{{...}}`, enlaces rotos ni datos ficticios.
- [ ] Aprobación de la inmobiliaria registrada antes de publicar.
- [ ] Fecha y persona responsable de última actualización registradas.

## 13. Registro de decisiones

- **D-001:** MVP estático y manual; evitar base de datos, panel, CRM y analítica avanzada antes de validar pago.
- **D-002:** NFC y QR apuntan a la misma URL individual de la propiedad.
- **D-003:** La ficha no incluye un QR de acceso redundante; su CTA principal conduce a WhatsApp.
- **D-004:** NexoSolutions administra las fichas al comienzo; la inmobiliaria aporta y aprueba el contenido.
- **D-005:** La autogestión es una etapa futura, no parte del MVP actual.
- **D-006:** El modelo comercial debe contemplar alta inicial más mantenimiento recurrente con alcance explícito; importes aún no definidos.
- **D-007:** Piloto objetivo de 3 inmobiliarias y 1–2 propiedades por inmobiliaria.
- **D-008:** No comprar placas ni asumir costos adicionales antes de verificar interés y necesidad; confirmar cualquier costo de plataforma antes de pagarlo.
- **D-009:** No prometer resultados de ventas ni publicar datos no confirmados.
- **D-010:** URLs estables mientras la infraestructura y el servicio estén mantenidos; la política de cancelación y baja debe ser explícita.

## 14. Cómo continuar en una nueva conversación

Usar este documento como fuente principal de continuidad. Antes de volver a investigar un punto, comprobar primero este documento, los archivos relevantes del repositorio y los commits recientes. No repetir auditorías sin una pregunta concreta nueva o evidencia de cambio. Registrar decisiones nuevas en la sección 13 y actualizar el estado cuando un pendiente se verifique.

**Próxima acción recomendada:** verificar el despliegue real de Netlify y ejecutar la Fase 1 antes de tocar el diseño o comprar hardware.


## 15. Costos de infraestructura, despliegues y crecimiento

Esta sección se agrega para evitar que la evolución a autogestión cree costos variables que NexoSolutions no pueda trasladar ni controlar. Los precios y límites de proveedores cambian: revisar sus páginas oficiales y el plan real de la cuenta antes de contratar o comprometer un precio al cliente.

### 15.1 Netlify: distinguir edición de contenido y despliegue

La ficha actual es HTML estático publicado en Netlify. En este enfoque, editar archivos y publicar una versión nueva suele generar un despliegue de producción. En los planes de créditos publicados por Netlify, cada despliegue de producción exitoso consume 15 créditos; las vistas previas y los despliegues de rama no consumen créditos. El plan Free publicado incluye 300 créditos al mes y se detiene al alcanzar el límite; Personal aparece a USD 9/mes con 1.000 créditos. Consultar siempre la tarifa actual y el tipo de plan de la cuenta.

Referencia oficial: https://www.netlify.com/pricing/ y https://docs.netlify.com/manage/accounts-and-billing/billing/billing-for-credit-based-plans/how-credits-work/

**Implicación de diseño:** si cada cliente modifica el HTML o un archivo del repositorio para cambiar precio, fotos o disponibilidad, puede disparar despliegues de producción y consumir créditos de la cuenta de NexoSolutions. No se debe entregar a los clientes acceso de escritura al repositorio como método normal de autogestión.

### 15.2 Arquitectura recomendada por etapas

**Etapa A — MVP gestionado estático**
- Mantener las fichas estáticas y el proceso manual mientras se valida el servicio.
- Agrupar cambios pequeños cuando sea razonable y publicar solo cuando estén aprobados.
- No agregar backend ni base de datos solo por anticipación.
- Registrar el costo y el tiempo de cada ficha/cambio para conocer el costo real del servicio.

**Etapa B — autogestión sin despliegue por cada cambio**
- Separar la aplicación de la información de cada propiedad.
- La aplicación se despliega cuando cambia su código; los cambios de precio, texto, fotos o disponibilidad se guardan como datos y se muestran en tiempo de ejecución.
- Guardar datos estructurados en PostgreSQL (por ejemplo, inmobiliarias, propiedades, usuarios, estado de publicación y referencias a imágenes).
- Guardar fotografías y archivos en almacenamiento de objetos/medios, no dentro del repositorio Git ni como grandes blobs en PostgreSQL. En la base de datos se guarda la URL/ruta, metadatos y relación con la propiedad.
- Añadir autenticación y autorización por inmobiliaria antes de permitir autogestión. Una inmobiliaria no debe poder editar las propiedades de otra.
- Limitar tamaño/tipo de archivos, cantidad de fotos, cuota de almacenamiento y permisos de eliminación.
- No adoptar esta etapa hasta validar que los clientes realmente necesitan autogestión y que la cuota recurrente puede cubrir la infraestructura y el soporte.

Un CMS conectado a Git puede seguir generando un despliegue por cada cambio; no asumir que “tener un panel” resuelve automáticamente el costo de deploy. La condición de aceptación de la futura arquitectura será que una edición ordinaria de contenido no requiera desplegar el sitio de producción.

### 15.3 Papel de cada servicio

- **GitHub:** repositorio del código, plantillas, documentación y control de versiones. No debe ser el almacén de fotos comerciales ni de datos de clientes.
- **Netlify:** alojamiento estático/CDN y publicación de la versión web durante el MVP. Si se mantiene en la arquitectura futura, presupuestar créditos por despliegues, solicitudes, transferencia y cualquier cómputo usado.
- **Render:** opción candidata para alojar una API/backend y PostgreSQL gestionado cuando se necesite autogestión. No es obligatorio incorporarlo en el MVP estático.
- **Almacenamiento de objetos/medios:** servicio separado para fotografías y archivos. Evaluar precio por GB almacenado, transferencia/egreso, operaciones, transformaciones de imágenes y backups.
- **Backups:** política independiente del proveedor principal; verificar restauración, no solo que exista una opción de backup.

### 15.4 Render PostgreSQL y protección de datos

La documentación oficial de Render indica que su PostgreSQL gratuito tiene capacidad de 1 GB, expira a los 30 días y no incluye backups administrados ni recuperación PITR. Las bases de datos pagas reciben backups continuos con recuperación a un punto en el tiempo; la ventana indicada es de 3 días en Hobby y 7 días en Pro o superior. Render cobra el almacenamiento de PostgreSQL por separado según su página de precios y el plan de cómputo.

Referencias oficiales:
- https://render.com/docs/free
- https://render.com/docs/postgresql-backups
- https://render.com/docs/postgresql
- https://render.com/pricing

**Regla operativa:** nunca usar una base gratuita temporal como única copia de datos de clientes. Para datos de producción, elegir un plan vigente con backup y definir además una exportación independiente periódica, acceso restringido y una prueba de restauración. Los backups del proveedor no reemplazan una estrategia propia de recuperación.

### 15.5 Crecimiento del almacenamiento

Los gigabytes se refieren al volumen ocupado; también pueden existir cargos por transferencia, solicitudes, procesamiento y backups. Fotos y videos suelen crecer mucho más rápido que los datos de texto de una ficha.

Registrar por inmobiliaria:
- cantidad de fichas activas;
- cantidad de imágenes por ficha y tamaño medio;
- GB almacenados y GB transferidos al mes;
- solicitudes/visitas aproximadas;
- cantidad de ediciones/publicaciones;
- costo real de proveedor y tiempo de soporte.

Aplicar límites explícitos: tipos y tamaño máximo de archivo, número de fotos por ficha incluido en el plan, política de archivos originales, limpieza de contenido retirado y retención de copias. No cobrar por GB hasta definir medición y reglas transparentes; inicialmente puede ser más sencillo incluir una cuota razonable y cobrar por ampliaciones previamente acordadas.

### 15.6 GitHub: qué cuesta y qué no

El repositorio Git no es lo mismo que el hosting, la base de datos o el almacenamiento de fotos. GitHub ofrece repositorios públicos y privados en sus planes gratuitos; las funciones de uso medido, como GitHub Actions, Git LFS y Packages, tienen cuotas y reglas de facturación propias. GitHub Actions es gratuito para ejecutores estándar en repositorios públicos, pero los artefactos/almacenamiento y otros productos tienen límites según el plan.

Referencias oficiales:
- https://github.com/pricing
- https://docs.github.com/es/billing/reference/product-usage-included
- https://docs.github.com/es/actions/concepts/billing-and-usage

Para el repositorio actual, compuesto principalmente por HTML, CSS, JavaScript y documentación, no se prevé un costo por el simple hecho de mantener el código en GitHub Free. Esto no significa que todo producto de GitHub sea gratuito ni que Netlify/Render/almacenamiento sean gratuitos. Evitar subir fotografías de propiedades, videos, backups o archivos grandes al historial Git.

### 15.7 Principio para fijar el mantenimiento

El precio recurrente debe cubrir, como mínimo, los costos asignables de infraestructura, almacenamiento y transferencia, copias de seguridad cuando correspondan, mantenimiento técnico y tiempo de soporte, más margen. No fijar una cuota antes de conocer estos costos y el alcance incluido.

Para evitar que el proveedor genere un gasto ilimitado:
1. mantener recargas automáticas desactivadas hasta comprender el consumo, cuando el plan lo permita;
2. establecer presupuestos/alertas y revisar el uso mensualmente;
3. definir cuotas por cliente y reglas para ampliaciones;
4. no prometer almacenamiento, tráfico o cambios ilimitados;
5. documentar un procedimiento de exportación y baja;
6. revisar precios oficiales antes de cada cambio de arquitectura.

## 16. Decisiones nuevas sobre infraestructura

- **D-011:** No entregar a clientes acceso de escritura al repositorio como mecanismo de autogestión.
- **D-012:** En la futura autogestión, una edición normal de contenido debe actualizar datos sin requerir un deploy de producción.
- **D-013:** Mantener el MVP estático y sin base de datos mientras se valida el servicio.
- **D-014:** Render PostgreSQL es una opción futura para backend/datos estructurados, no una contratación inmediata.
- **D-015:** Fotografías y videos se almacenarán fuera de Git y, preferentemente, fuera de PostgreSQL, en almacenamiento de medios/objetos con cuotas y costos medibles.
- **D-016:** Ninguna base gratuita temporal será la única copia de datos de producción; se requieren backups y una prueba de restauración.
- **D-017:** La cuota de mantenimiento debe cubrir infraestructura, almacenamiento/transferencia y soporte dentro de límites explícitos.


## 17. Auditoría integral de estado — Constancia NS-AUD-2026-10-18-01

**Fecha:** 18 de octubre de 2026 (Uruguay).  
**Alcance:** documento maestro, README, landing, ficha demo independiente, plantillas de venta/alquiler, HEAD de `main`, comparación de commits y despliegue de producción de Netlify.  
**Método:** inspección de archivos reales y metadatos del proveedor. Esta auditoría no equivale a una prueba manual en un teléfono ni a una prueba física de NFC.

### 17.1 Resultado ejecutivo

**Estado: MVP web demostrativo publicado; todavía NO listo para instalar en un cliente real.**

El repositorio contiene una landing estática, una ficha demo independiente y dos plantillas de fichas. El despliegue de producción de Netlify está en estado `ready` y corresponde al commit `b15eafbda8477cb5af40be03231343efd4ea61f3`, que elimina el QR redundante dentro de la ficha independiente. Se verificó en el contenido de GitHub que esa ficha ya no contiene el bloque QR ni la llamada al servicio externo de generación QR.

Esto acredita que el cambio está publicado según los metadatos de Netlify, pero no demuestra por sí solo que el recorrido se haya probado en navegador o teléfono después del despliegue.

### 17.2 Fuentes inspeccionadas y evidencias

1. Documento maestro en `main`: inspeccionado. La auditoría previa tenía fecha 17 de octubre de 2026 y dejaba pendiente confirmar el deploy más reciente.
2. `README.md`: inspeccionado. Describe el producto como MVP estático, gestionado manualmente, con piloto pendiente.
3. `index.html`: inspeccionado. Contiene la landing y una ficha de ejemplo integrada que se muestra/oculta con JavaScript; no navega a una página independiente al pulsar los botones de demo.
4. `propiedades/casa-demo/index.html`: inspeccionado antes y después de la corrección. Conserva datos y gráficos ficticios, botón de WhatsApp sin número autorizado y URL de propiedad configurada en el código. El bloque QR interno fue eliminado.
5. `plantillas/venta.html`: inspeccionada. Usa marcadores `{{...}}`, placeholders para fotografías y un enlace WhatsApp con marcadores que requieren sustitución/codificación correctas.
6. `plantillas/alquiler.html`: inspeccionada. Usa marcadores similares para precio, disponibilidad, condiciones, requisitos, imágenes y WhatsApp.
7. GitHub: el commit `b15eafbda8477cb5af40be03231343efd4ea61f3` modifica únicamente `propiedades/casa-demo/index.html`; comparación contra `46a0610a6542f22a43ecf27ca20645270400cf57` informa 1 commit por delante, 0 por detrás, 1 archivo modificado.
8. Netlify: deploy `6ad429032a192082cc330037`, rama `main`, estado `ready`, contexto `production`, commit `b15eafbda8477cb5af40be03231343efd4ea61f3`, sin mensaje de error reportado por el proveedor.

### 17.3 Qué existe, qué funciona y qué está probado

| Elemento | Estado comprobado | Alcance de la evidencia |
|---|---|---|
| Repositorio y rama `main` | Existe | Lectura de archivos y metadatos de commits |
| Landing estática | Existe en el repositorio | Inspección de HTML/CSS/JS; no prueba manual visual en varios dispositivos |
| Demo integrada | Existe | Cambio de vista gestionado por JavaScript en el mismo documento |
| Ficha demo independiente | Existe | HTML estático con contenido ficticio |
| Plantilla de venta | Existe | No es una ficha de cliente lista: requiere reemplazar marcadores |
| Plantilla de alquiler | Existe | No es una ficha de cliente lista: requiere reemplazar marcadores |
| Deploy de producción | `ready` | Confirmado en metadatos de Netlify para el commit exacto |
| QR redundante dentro de la ficha independiente | Eliminado del código actual | Confirmado en el contenido del archivo; no es un QR físico |
| QR de acceso en una placa | No verificado en esta auditoría | La landing muestra un patrón visual ilustrativo, no un QR de producción |
| NFC físico | Pendiente | No hay evidencia de etiqueta programada ni prueba física |
| WhatsApp real de inmobiliaria | Pendiente | No hay número autorizado configurado |
| Ficha con propiedad real | Pendiente | No se ha suministrado contenido de un cliente ni aprobación |
| Recorrido extremo a extremo en teléfono | Pendiente de repetir | Hay un antecedente de prueba QR informado previamente por el usuario, pero no se repitió tras el último deploy |
| Cliente/piloto/ventas | No acreditado | No hay aceptación de cliente ni resultados comerciales en las fuentes inspeccionadas |

### 17.4 Diferencias respecto de la auditoría anterior

- **Resuelto:** se confirmó el despliegue de producción pendiente de la auditoría previa. Netlify publica el commit `b15eafbda8477cb5af40be03231343efd4ea61f3` y lo reporta `ready`.
- **Resuelto en código:** se eliminó el QR interno redundante de la ficha independiente y se retiró su generador externo.
- **Sigue abierto:** la landing y la ficha independiente son dos experiencias distintas; la landing contiene una demo interna, y la ficha independiente no se abre desde un enlace de demo explícito que haya sido probado en este ciclo.
- **Sigue abierto:** el patrón de QR de la landing es ilustrativo y no debe imprimirse ni confundirse con un código funcional.
- **Sigue abierto:** el botón WhatsApp de la ficha independiente no inicia una consulta real porque no tiene un número autorizado.
- **Sigue abierto:** las plantillas no son generadores automáticos y conservan marcadores que impiden publicarlas sin personalización.
- **Sigue abierto:** no hay evidencia nueva de etiqueta NFC física, ficha real, cliente piloto, precios acordados o aceptación comercial.

### 17.5 Riesgos, contradicciones y limitaciones

1. **Riesgo de confundir demo con producto operativo:** la landing enseña el concepto, pero la representación de placa y QR es ilustrativa.
2. **Riesgo de expectativa incorrecta:** el texto describe una experiencia NFC + QR + WhatsApp completa, aunque NFC y WhatsApp real todavía no han sido probados con datos autorizados.
3. **Riesgo de publicación manual:** las plantillas pueden publicar marcadores sin sustituir si no se aplica un checklist.
4. **Riesgo de dependencia de operación:** todavía no se ha demostrado un procedimiento repetible de alta, aprobación, publicación, baja y actualización de una ficha.
5. **Riesgo comercial:** no se validaron la urgencia del problema, la disposición a pagar ni el mantenimiento recurrente.
6. **Riesgo operativo/contractual:** falta acordar precio, alcance, tiempos de cambios, autorización de contenido, baja, continuidad de URL y propiedad de placa.
7. **Limitación de esta auditoría:** se inspeccionó el código y el estado del despliegue mediante conectores; no se ejecutó un navegador automatizado, no se tomó un teléfono para repetir el escaneo, no se compró/programó NFC y no se realizó una transacción real.
8. **Sin evidencia de regresión de código:** la última modificación reportada se limita al archivo de ficha independiente. Esto no sustituye pruebas funcionales.

### 17.6 Prioridades actualizadas

**P0 — Verificación funcional pública**
1. Abrir la landing y la ficha independiente desde un navegador real.
2. Confirmar que los botones de demo llevan a la vista esperada y que se puede regresar a la landing.
3. Revisar la visualización móvil y escritorio.
4. Confirmar que la ficha demo identifica inequívocamente todos los datos ficticios y que no hay QR interno.
5. Documentar resultados como probado/no probado; no inferirlos del estado `ready` del deploy.

**P1 — Preparar un piloto real sin sobredesarrollar**
1. Crear una ficha de prueba desde una de las plantillas y comprobar que no quedan marcadores.
2. Definir el protocolo para recibir datos/fotos autorizados, revisión y aprobación escrita.
3. Conseguir un número de WhatsApp autorizado cuando exista una inmobiliaria piloto.
4. Solo con interés real, conseguir una etiqueta NFC de prueba y verificar que NFC y QR abren la misma URL.
5. Registrar precio/alcance de piloto y mantenimiento antes de prometer una prestación.

**P2 — Validación de negocio**
- Hablar con prospectos, registrar objeciones y disposición a pagar. El objetivo inicial de tres inmobiliarias y 1–2 propiedades por inmobiliaria sigue siendo una meta, no un resultado.
- No crear base de datos, panel, CRM ni sistema de analítica todavía.

### 17.7 Siguiente paso concreto y criterio de finalización

**Siguiente paso:** prueba manual del recorrido web en navegador de escritorio y teléfono, utilizando la landing pública y la ficha independiente.

**Se considera finalizado cuando:** (a) ambos URLs cargan sin error; (b) la landing abre su demo integrada y permite regresar; (c) la ficha independiente carga y se adapta a móvil; (d) el CTA informa claramente que WhatsApp real está pendiente, sin simular una consulta exitosa; (e) no hay QR interno redundante; (f) se registra qué se probó y en qué dispositivo. Esto no certifica NFC físico ni autoriza aún una instalación en cliente.

### 17.8 Balance de evolución y recomendación

Desde la auditoría anterior, el proyecto avanzó en dos puntos verificables: se confirmó el deploy de producción más reciente y se corrigió el QR redundante en la ficha independiente. La base técnica está suficientemente formada para continuar con QA y preparación del piloto, pero no existe evidencia suficiente para declarar el producto listo para una instalación real.

**Recomendación operativa:** congelar nuevas funcionalidades. Ejecutar ahora el QA público del recorrido web; después preparar una ficha real solo cuando una inmobiliaria aporte y apruebe sus datos. No comprar hardware en cantidad, contratar infraestructura adicional ni prometer resultados comerciales antes de validar el primer piloto.

