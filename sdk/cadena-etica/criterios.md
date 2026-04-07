# Criterios de cadena ética para el activo del préstamo

> Documento de referencia del SDK. Define qué significa "cadena ética"
> en el contexto de un préstamo eco-sostenible: qué criterios debe cumplir
> el activo, cómo verificarlos, y qué documentación producen esos criterios.
> Los criterios son genéricos; la certificación concreta varía por tipo de activo
> — ver `cadena-etica/certificaciones-tipo.md` para el catálogo de certificaciones.

---

## Por qué la cadena ética importa para un préstamo

Un préstamo fraterno podría hacerse con cualquier bien — efectivo, un objeto ordinario, o cualquier activo con valor de mercado. El SDK especifica que el activo debe tener cadena ética porque el doble eje del préstamo no es solo fiscal y relacional: es también material. El eje eco-sostenible no se sostiene si el bien que pasa de manos llegó a través de una cadena de extracción opaca, trabajo no remunerado, o impacto ambiental no declarado. La ética del acto de prestar empieza antes de la firma del contrato: empieza en quién produjo el bien, en qué condiciones, con qué impacto.

Esto no es perfeccionismo: es coherencia. El préstamo fraterno pretende activar la economía con cuidado de la cadena completa. Si la cadena no se examina, el acto no es coherente con lo que proclama.

---

## Los cuatro criterios de cadena ética

### Criterio 1: Trazabilidad del origen

El activo puede rastrear documentalmente su cadena de producción desde el origen de la materia prima hasta el taller del proveedor. La trazabilidad no tiene que ser perfecta — la perfección es inalcanzable en cualquier cadena de suministro global —, pero tiene que ser verificable en los eslabones clave: quién extrajo o produjo la materia prima, a qué precio, bajo qué condiciones laborales y ambientales básicas.

**Documento que lo acredita:** certificado de trazabilidad emitido por el proveedor de la materia prima certificada, o por el organismo certificador correspondiente.

**Nivel mínimo:** que el proveedor pueda señalar una certificación reconocida para los materiales principales del activo. El tipo de certificación varía por activo — ver `cadena-etica/certificaciones-tipo.md`.

---

### Criterio 2: Trabajo digno en el nodo artesanal

El {{PROVEEDOR}} — el artesano, fabricante, o productor que convierte la materia prima en {{ACTIVO}} — trabaja en condiciones de autonomía y dignidad económica: es un agente económico independiente que fija sus precios, declara su actividad ante la administración tributaria, y recibe pago justo por su oficio. El proyecto no exige que el proveedor sea un actor perfecto del comercio justo: exige que no sea un actor de trabajo informal, precario, o no remunerado disfrazado de encargo.

**Documento que lo acredita:** la factura del proveedor, que por su propia existencia demuestra que hay un agente económico formal que declara la operación.

**Por qué esto importa:** El objetivo del eje eco-sostenible es que el dinero circula y toca tierra antes de llegar al receptor. Si el {{PROVEEDOR}} trabaja en informal o no cobra precio justo, el dinero no toca tierra: atraviesa sin impacto el nodo que debería activar trabajo digno.

---

### Criterio 3: Impacto positivo documentado en los productores primarios

La certificación ética de los materiales del activo debe estar vinculada a un mecanismo de premium — un sobreprecio sobre el precio de mercado que se destina directamente a los productores primarios o a las comunidades de origen — y ese mecanismo debe estar auditado periódicamente por un organismo independiente.

Un certificado de "origen responsable" que no incluye un premium verificable y un mecanismo de auditoría es una etiqueta sin contenido: puede garantizar que hubo buenas intenciones, pero no que hubo impacto medible. El SDK rechaza los certificados vacíos y exige al menos un organismo de tercera parte con protocolo de auditoría.

**Documento que lo acredita:** la certificación de los materiales de la categoría de activo del mod, que debe incluir descripción del mecanismo de premium y referencia a las auditorías del organismo certificador.

---

### Criterio 4: Impacto ambiental mínimo verificable

La extracción o producción de la materia prima del activo debe estar sujeta a criterios ambientales que se verifiquen en el proceso de certificación: ausencia de uso de sustancias altamente tóxicas sin control, respeto a perímetros de protección ambiental, gestión de residuos del proceso productivo. Los criterios concretos varían por tipo de activo — la minería artesanal de oro tiene estándares diferentes a la producción de textil orgánico o la extracción de madera certificada —, pero la certificación debe contemplar el factor ambiental explícitamente.

**Documento que lo acredita:** el mismo certificado de trazabilidad y certificación ética, que en las certificaciones bien estructuradas incluye criterios ambientales junto con los sociales.

---

## Qué no exige el SDK

El SDK no exige que el activo sea ecológicamente perfecto ni que la cadena completa sea auditada hasta el último eslabón. Toda cadena global de suministro tiene opacidades — la certificación reduce la opacidad, no la elimina. Lo que el SDK exige es:

- Que exista al menos una certificación reconocida de tercera parte para los materiales principales
- Que esa certificación incluya un mecanismo de premium y un protocolo de auditoría
- Que el proveedor sea un agente económico formal que factura y declara
- Que la documentación de todos estos elementos esté archivada en la carpeta del mod

Los cuatro criterios son verificables documentalmente, no aspiracionalmente. Si no se puede demostrar el cumplimiento de los criterios con documentos, no se cumple.

---

## La pregunta que hay que hacerse antes de elegir el activo

Antes de que el prestamista elija el activo para el mod, la pregunta correcta no es "¿tiene este bien valor suficiente para el préstamo?" sino "¿puedo decirle al receptor, con documentos en la mano, cuál es la historia de lo que le estoy prestando?" Si la respuesta es sí, el activo es apto para el eje eco-sostenible. Si la respuesta es "no, pero tiene mucho valor", el activo puede ser adecuado para un préstamo ordinario pero no para un préstamo eco-sostenible y eco-fraterno según el SDK.

---

*Para las certificaciones concretas según tipo de activo, ver `cadena-etica/certificaciones-tipo.md`. Para el registro y archivo de la documentación de cadena ética, ver `sdk/plantillas/anexo-tecnico.template.md`.*
