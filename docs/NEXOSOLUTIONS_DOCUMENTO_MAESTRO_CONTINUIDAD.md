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
