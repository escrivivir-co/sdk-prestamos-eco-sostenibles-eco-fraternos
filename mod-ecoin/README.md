# mod-ecoin — préstamo fraterno en moneda ECOin sobre red Oasis

> Instanciación del SDK de préstamos eco-sostenibles y eco-fraternos
> para el activo: **ECOin** — criptomoneda de economía solar —
> operada sobre la red **Oasis** de SolarNET.HuB (SNH).
>
> SDK base en `main`: [`README.md`](../README.md) ·
> [`sdk/concepto.md`](../sdk/concepto.md)

---

## El circuito

```
   ┌─────────────────────────────────────────────┐
   │            RED OASIS / SolarNET.HuB         │
   │                                              │
   │   eMiner ───→ Wallet ───→ Transfer           │
   │   (solar)      (ECO)       (smart-contract)  │
   └──────┬───────────┬──────────────┬────────────┘
          │           │              │
          ▼           ▼              ▼
      PROVEEDOR    PRESTAMISTA    RECEPTOR
      (nodo SNH)   (holder ECO)   (wallet Oasis)
      mina / valida  transfiere    recibe / opera
      energía solar  préstamo 0%   4 opciones
```

---

## El doble eje en ECOin

### Eco-sostenible

En el mod oro la cadena ética era Fairmined → joyera → rosario: trazabilidad sobre materia. En ECOin la cadena ética es **energética y computacional**: la moneda se mina con energía solar a través de un kit de hardware libre (SNH-KIT) y se verifica en una blockchain de código abierto (GPLv3). La eco-sostenibilidad no está en el material sino en la fuente: cada ECO creado ha consumido fotones, no combustibles fósiles; ha pasado por circuitos documentados (SCRYPT / POW+POS+POT), no por servidores opacos; y ha sido registrado en un ledger federal y distribuido, no en un banco central.

La diferencia nuclear con el oro: el oro es escaso por geología; ECOin es escaso por diseño (~225 millones ECO) y su escasez se transparenta en un explorador de bloques público. La cadena ética no se certifica con Fairmined: se verifica con `ecoin.03c8.net/blockexplorer`.

### Eco-fraterno

En el mod oro la fraternidad era un rosario que no persigue al receptor. En ECOin la fraternidad tiene una dimensión adicional: **la moneda vive dentro de una red social distribuida que ya tiene UBI** (Universal Basic Income semanal por participación). El suelo económico fraterno del SDK no es solo el préstamo al 0 %: es el ecosistema completo de Oasis donde el receptor puede operar un marketplace, recibir ingreso básico, y participar en gobernanza — todo sin intermediarios centralizados.

La cláusula-umbral de solvencia se transforma: no es "¿ha superado el receptor el umbral en euros?" sino "¿tiene el receptor capacidad de operación autónoma dentro de la red?". El préstamo de ECO no busca que el receptor vuelva al circuito fiat: busca que el receptor **construya suelo dentro del circuito alternativo** y, si un día puede, devuelva al prestamista el equivalente nominal en ECO.

Y la propiedad más radical: **ECOin es borrable**. Como dice el lore de Mr Robot que inspira este proyecto: al no tener soporte material, disolver los nodos basta para anular el entramado de deuda. El préstamo eco-fraterno en ECOin incluye, como escenario filosófico límite, la posibilidad de que la propia moneda desaparezca — y con ella la deuda. No es que se borre: es que *puede* borrarse. Esa posibilidad de extinción voluntaria del sistema monetario es la prueba última de que la fraternidad prevalece sobre el interés.

---

## Los tres roles instanciados

| Rol | En el SDK genérico | En mod-ecoin |
|---|---|---|
| **Proveedor** | Artesano que crea el activo | **Nodo SNH**: operador de un SNH-KIT solar que mina ECO, valida transacciones, y sostiene la red. No es artesano de materia: es artesano de infraestructura. |
| **Prestamista** | Financia y formaliza | **Holder ECO**: persona o colectivo que posee ECO minados o adquiridos. Transfiere al receptor mediante smart-contract (módulo Transfers de Oasis). El contrato a 0 % se documenta en la blockchain y en el contrato civil paralelo. |
| **Receptor** | Portador del activo | **Wallet Oasis**: persona que recibe ECO en su wallet dentro de la red Oasis. Opera las 4 opciones del SDK: conservar (staking POS), devolver gradualmente (transfers parciales), liquidar (marketplace Oasis), o rebotar (invertir en bienes/servicios del marketplace para generar actividad económica). |

Para los cuadernillos completos:
- [`mod-ecoin/roles/cuadernillo-nodo-snh.md`](roles/cuadernillo-nodo-snh.md) — el proveedor
- [`mod-ecoin/roles/cuadernillo-prestamista.md`](roles/cuadernillo-prestamista.md) — el prestamista
- [`mod-ecoin/roles/cuaderno-receptor.md`](roles/cuaderno-receptor.md) — el receptor

---

## Las 5 fases para ECOin

| Fase | Genérica (SDK) | Instanciada (ecoin) |
|---|---|---|
| **1** | Comisionar el activo | **Minar / adquirir ECO.** El prestamista opera un nodo SNH-KIT o adquiere ECO de un nodo-proveedor. La "comisión" es la prueba de origen energético solar. |
| **2** | Documentar el activo | **Documentar la trazabilidad on-chain.** Hash de la transacción de minado / adquisición, captura del block explorer, certificado de origen del nodo (ubicación, fuente energética, versión SNH-OS). |
| **3** | Formalizar el préstamo | **Smart-contract + contrato civil.** Transfer en Oasis con metadata del préstamo. Contrato civil paralelo con las 4 cláusulas del SDK adaptadas a ECOin (el "modelo fiscal" aplica según jurisdicción del prestamista). |
| **4** | Acto de entrega | **Ejecución del Transfer.** El ECO llega al wallet del receptor. Se entrega el cuaderno-receptor con las 4 opciones. La entrega es un hash verificable en el blockchain explorer. |
| **5** | Registro y seguimiento | **Monitorización on-chain + registro civil.** El estado del préstamo se verifica en la blockchain. Las devoluciones son transfers de vuelta. El registro de retornos vive tanto en el ledger como en el documento de seguimiento del mod. |

Para las bitácoras operativas: [`mod-ecoin/bitacoras/`](bitacoras/)

---

## Los 4 escenarios de devolución para ECOin

| Escenario | En ECOin |
|---|---|
| **A: Intacto** | El receptor conserva los ECO en su wallet (staking POS genera interés en coin age). Nunca supera el umbral. Préstamo en suspenso. Los ECO trabajan como reserva dentro de la red. |
| **B: Gradual** | El receptor envía transfers parciales de ECO al prestamista cuando puede. Valor nominal del momento del préstamo. Cada devolución: un hash en la blockchain. |
| **C: Liquidación** | El receptor usa los ECO en el marketplace de Oasis para cubrir necesidades (bienes, servicios, proyectos). Los ECO circulan en la economía de la red. No hay devolución. |
| **D: Rebote** | El receptor invierte ECO (crowdfunding via módulo Projects, compra de herramientas via Shops, participación en Tribes). Prospera dentro de la red. Activa devolución. |

---

## Índice de ficheros del mod

| Ruta | Contenido | SDK base |
|---|---|---|
| `mod-ecoin/README.md` | Este fichero | — |
| `mod-ecoin/proyecto.config.md` | Config del mod | `sdk/config.template.md` |
| `mod-ecoin/roles/cuadernillo-nodo-snh.md` | Cuadernillo del proveedor (nodo SNH) | `sdk/roles/proveedor.template.md` |
| `mod-ecoin/roles/cuadernillo-prestamista.md` | Cuadernillo del prestamista | `sdk/roles/prestamista.template.md` |
| `mod-ecoin/roles/cuaderno-receptor.md` | Cuadernillo del receptor | `sdk/roles/receptor.template.md` |
| `mod-ecoin/cadena-etica/ecoin-cadena-energetica.md` | Cadena ética: energía solar + software libre | `sdk/cadena-etica/criterios.md` |
| `mod-ecoin/bitacoras/bitacora-fase-{1-5}.md` | Bitácoras de las 5 fases | `sdk/plantillas/bitacora-fase.template.md` |
| — | — | `sdk/concepto.md` |
| — | — | `sdk/legal/clausulas-base.md` |
| — | — | `sdk/legal/estructura-fiscal.md` |

---

## Referencia rápida de la cadena ética

| Eslabón | Descripción | Verificación |
|---|---|---|
| **Energía** | Solar — el SNH-KIT opera con panel fotovoltaico | Modelo y fuente documentados en bitácora fase 1 |
| **Hardware** | SNH-KIT — hardware libre, carcasa DIY 3D-printable, fuentes publicadas | `wiki.solarnethub.com/kit/overview` |
| **Software** | ECOin (GPLv3), SNH-OS (libre), Oasis (libre, distribuido, cifrado) | `code.03c8.net/epsylon/ecoin` · `code.solarnethub.com` |
| **Red** | Blockchain ECOin con explorador público + red Oasis federada | `ecoin.03c8.net/blockexplorer` |
| **Gobernanza** | UBI semanal, Parliament (elecciones), Courts (justicia), Tribes (comunidades) | Módulos nativos de Oasis v.0.6.9+ |

Para el documento completo: [`mod-ecoin/cadena-etica/ecoin-cadena-energetica.md`](cadena-etica/ecoin-cadena-energetica.md)

---

## El timeline de Oasis como contexto

El proyecto ECOin no nace en el vacío. SolarNET.HuB tiene una historia de 20 años desde la primera semilla (2006) pasando por Lorea.org, BorderCheck, Phone Liberation Network, hasta el lanzamiento de ECOin en 2014, mencionado en Mr Robot (2015), integrado en SNH-OS (2024), y desplegado como paquete para Android y AMD64 (2026). Oasis opera con sistemas de IA (42), gobierno (Parliament), justicia (Courts), y renta básica (UBI). El mod-ecoin del SDK se inserta en este ecosistema como la capa de formalización que conecta el circuito fraterno con el marco legal civil necesario para que el préstamo exista ante la administración tributaria.

---

## Invocación

```
@{agente} MOD-ECOIN {tema}
```
