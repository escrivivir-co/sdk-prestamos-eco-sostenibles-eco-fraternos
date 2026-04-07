# Cadena ética energética y computacional — mod ECOin

> Adaptación de los cuatro criterios de cadena ética del SDK al activo ECOin.
> En lugar de una cadena material (extracción → taller → producto),
> ECOin tiene una cadena energética y computacional
> (energía solar → hardware libre → software libre → blockchain pública).
>
> Referencia genérica: `sdk/cadena-etica/criterios.md`

---

## Por qué «cadena ética» en un activo digital

El SDK exige que el activo del préstamo tenga cadena ética verificable. Con oro, la cadena es material: quién extrajo el mineral, en qué condiciones, con qué certificación. Con ECOin, no hay mineral — pero hay energía, hardware, software y red. La pregunta no cambia: ¿puedo decirle al receptor, con documentos en la mano, cuál es la historia de lo que le estoy prestando?

En ECOin, la historia es: de dónde viene la electricidad que minó esta moneda, con qué máquina, con qué código, en qué red. Si la electricidad viene de carbón, el hardware de una fábrica opaca, el código es privativo, y la red es controlada por un oligopolio de nodos, entonces ECOin no es diferente de cualquier otra cripto-mercancía. La cadena ética es lo que hace la diferencia.

---

## Los cuatro criterios adaptados

### Criterio 1: Trazabilidad del origen — blockchain pública

**SDK genérico:** El activo puede rastrear documentalmente su cadena de producción desde el origen.

**En ECOin:** Cada ECO nace como recompensa de un bloque minado. El bloque existe en una blockchain pública, verificable por cualquiera en el block explorer (`ecoin.03c8.net/blockexplorer`). El hash del bloque, la dirección del minero, la fecha y la recompensa son datos públicos e inmutables.

La trazabilidad de ECOin no es documental-analógica (un certificado en papel) sino computacional-verificable: el propio protocolo la garantiza. Es, paradójicamente, más trazable que el oro — nadie puede falsificar un hash SHA-256 o un bloque validado por consenso de la red.

**Documento que lo acredita:** Captura del block explorer con el hash del bloque que generó los ECO prestados, o del transfer que los trajo al wallet del prestamista.

---

### Criterio 2: Trabajo digno en el nodo artesanal — hardware libre y energía solar

**SDK genérico:** El proveedor trabaja en condiciones de autonomía y dignidad económica.

**En ECOin con SNH-KIT:** El nodo proveedor opera un SNH-KIT: hardware libre (diseño publicado bajo licencia abierta, carcasa imprimible en 3D), alimentado por energía solar, ejecutando SNH-OS (sistema operativo libre con eMiner integrado). El operador del nodo es un agente autónomo que decide cuándo minar, cuánto minar, y cómo distribuir sus ECO.

El «trabajo digno» aquí no es una factura de un artesano — es la autonomía computacional de un operador que no depende de infraestructura centralizada, ni de electricidad de red, ni de software privativo. El nodo solar es el taller artesanal del siglo XXI.

**Documento que lo acredita:**
- Certificado del nodo proveedor (autodeclaración de configuración: hardware, fuente de energía, software)
- Dirección ECOin del nodo verificable en la blockchain

**Nivel mínimo:** Que el operador pueda demostrar que su nodo funciona con energía renovable y hardware/software libre. La autodeclaración es el mínimo; la verificabilidad del nodo en la red es la prueba adicional.

---

### Criterio 3: Impacto positivo documentado — economía distribuida con UBI

**SDK genérico:** La certificación ética debe estar vinculada a un mecanismo de premium que beneficie a los productores primarios.

**En ECOin:** No hay «productores primarios» en el sentido extractivo. Pero hay un mecanismo análogo al premium: la UBI (Renta Básica Universal) de Oasis. Cada participante activo en la red recibe una asignación semanal de ECO — no como caridad, sino como retribución por mantener viva la red con su participación. El mecanismo está integrado en el protocolo social de Oasis, no depende de una auditoría externa sino de la gobernanza distribuida (módulos Parliament y Courts).

**Impacto adicional:** El marketplace de Oasis permite que los ECO circulen sin intermediarios entre productores y consumidores. Los módulos Projects y Tribes canalizan inversión colectiva. El impacto no es un premium sobre un precio de mercado — es la construcción de un circuito económico alternativo completo.

**Documento que lo acredita:** Estado del módulo UBI para el wallet del receptor (verificable en Oasis), actividad del marketplace y proyectos asociados.

---

### Criterio 4: Impacto ambiental mínimo verificable — energía solar, no fósil

**SDK genérico:** La producción del activo debe estar sujeta a criterios ambientales verificables.

**En ECOin con SNH-KIT:** La huella ambiental del minado de ECOin depende directamente de la fuente de energía. Un ECO minado con carbón tiene huella de carbón. Un ECO minado con panel solar tiene huella solar.

El SNH-KIT es explícitamente solar: el kit incluye panel fotovoltaico y está diseñado para operar off-grid. Esto no es greenwashing — es diseño de hardware. La fuente de energía no es un certificado añadido a posteriori sino una decisión arquitectónica del sistema.

**Documento que lo acredita:** Especificaciones del SNH-KIT (publicadas en `wiki.solarnethub.com`), autodeclaración del operador del nodo sobre su fuente de energía.

**Nota:** ECOin puede minarse sin SNH-KIT, con hardware convencional y electricidad de red. En ese caso, el criterio 4 requiere que el operador declare su fuente de energía y, si no es renovable, el mod debe documentar esa limitación explícitamente. La cadena ética no exige perfección — exige transparencia.

---

## Tabla resumen

| Criterio SDK | Oro (mod-oro) | ECOin (mod-ecoin) |
|---|---|---|
| 1. Trazabilidad | Certificado Fairmined/Fairtrade | Hash del bloque en blockchain pública |
| 2. Trabajo digno | Factura del orfebre/joyera | Nodo solar autónomo (SNH-KIT) |
| 3. Impacto positivo | Premium Fairmined a mineros | UBI + marketplace + gobernanza distribuida |
| 4. Impacto ambiental | Minería artesanal sin mercurio | Energía solar, hardware reciclable |

---

## Qué no exige este mod

- No exige que todos los ECO del préstamo hayan sido minados con SNH-KIT. Pueden haber sido adquiridos de otro nodo. Lo que exige es que el prestamista pueda documentar la cadena hasta un nodo verificable.
- No exige auditoría externa. La blockchain es el auditor. El block explorer es público.
- No exige que la fuente de energía sea 100 % solar. Exige que sea declarada y, preferiblemente, renovable.

---

## La pregunta antes de prestar ECO

La misma que con oro, adaptada: «¿Puedo decirle al receptor, con hashes en la mano, cuál es la historia energética y computacional de lo que le estoy prestando?» Si la respuesta es sí — si puedo señalar el bloque, el nodo, la fuente de energía, el software libre — entonces el ECO es apto para el eje eco-sostenible. Si no puedo, es un token opaco, y un token opaco no es un préstamo fraterno.

---

*Para los criterios genéricos del SDK, ver `sdk/cadena-etica/criterios.md`.
Para las certificaciones por tipo de activo, ver `sdk/cadena-etica/certificaciones-tipo.md`.*
