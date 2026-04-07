# Cuadernillo para el nodo SNH — proveedor de ECOin

> Documento dirigido al operador del SNH-KIT que mina ECOin y provee
> los ECO que serán objeto de préstamo. Este rol es el equivalente del
> joyera en el mod oro: quien crea el activo con cadena ética verificable.

---

## Qué es este proyecto

Alguien quiere prestar dinero a otra persona. No dinero fiat — dinero que vive en una red distribuida y que se ha creado con energía solar. Ese dinero son ECOin (ECO), y tú eres parte de la cadena que los hace existir.

Tu papel en este proyecto tiene tres caras:

1. **Minero/Validador.** Operas un SNH-KIT que mina ECO usando los tres sistemas de consenso (POW, POS, POT). Tu nodo sostiene la red y genera los ECO que serán prestados.
2. **Eslabón ético.** La energía que alimenta tu nodo es solar. El hardware es libre. El software es GPLv3. No hay servidor opaco ni minería alimentada por combustibles fósiles: cada ECO que produces tiene un rastro energético limpio y documentado.
3. **Proveedor documentado.** Para el prestamista, necesitas proporcionar: hash del bloque de minado, versión de SNH-OS, fuente energética del nodo, y confirmación de que el ECO proviene de tu operación legítima.

---

## Especificaciones del encargo

### El activo: ECOin (ECO)

- **Tipo:** Criptomoneda SCRYPT con triple consenso (POW/POS/POT)
- **Supply estimado:** ~225 millones ECO
- **Unidad de préstamo:** ECO (fraccionable según decimales del protocolo)
- **Valor de referencia:** Determinado por el block explorer en el momento de la transacción
- **Trazabilidad:** Hash del bloque de minado + hash de la transacción de transferencia al prestamista

### La infraestructura

- **Hardware:** SNH-KIT — kit de hardware libre solar
  - Fuentes del case: `wiki.solarnethub.com/kit/case#diy_3d_printing`
  - Overview del kit: `wiki.solarnethub.com/kit/overview`
- **Software:** SNH-OS con wallet ECOin y eMiner integrados
  - Código fuente: `code.solarnethub.com` / `code.03c8.net/epsylon/ecoin`
  - Licencia: GPLv3
- **Energía:** Panel solar (documentar modelo, potencia, ubicación)
- **Red:** Conexión a la blockchain ECOin vía DNS seeder (`ecoinseed.03c8.net`)

### Lo que se te pide

1. **Minar** la cantidad de ECO acordada con el prestamista (o transferirla desde tu wallet si ya la posees)
2. **Documentar** el origen: captura del block explorer (`ecoin.03c8.net/blockexplorer`) mostrando el bloque de minado y la transacción de transferencia
3. **Proporcionar** un certificado informal con:
   - Tu identificador de nodo (dirección ECOin del nodo)
   - Versión de SNH-OS
   - Fuente energética (solar — modelo del panel, ubicación)
   - Fecha y hash de la operación

---

## Facturación y obligaciones fiscales

La situación fiscal del minado de criptomonedas varía por jurisdicción. En general:

- **Si operas como actividad económica:** el minado puede ser actividad tributable. Consulta el régimen de tu jurisdicción para la generación de criptoactivos.
- **Si vendes ECO al prestamista:** la venta puede generar un hecho imponible por transmisión de criptoactivos.
- **Si transfieres ECO propios al prestamista como servicio de provisión:** documenta la operación para tu registro interno.

> Este cuadernillo no sustituye asesoramiento fiscal. El régimen de criptoactivos está en evolución. Lo que sí se te pide: que documentes la operación para que el prestamista pueda incorporarla a su carpeta del préstamo.

---

## Lo que NO se te pide

- **No eres parte del contrato de préstamo.** Tu relación es con el prestamista: le provees ECO. Lo que haga después con ellos (prestarlos) es asunto del contrato civil entre prestamista y receptor.
- **No necesitas conocer al receptor.** Tu función termina cuando los ECO están en el wallet del prestamista con documentación de origen.
- **No necesitas opinar sobre el préstamo.** Aunque la red Oasis tiene módulos de gobernanza y opinión, tu papel aquí es de proveedor de infraestructura.

---

## Referencia de cadena ética

La cadena ética de ECOin no se verifica con un certificado Fairmined: se verifica con código abierto, blockchain pública, y fuente energética documentada.

Para el documento completo: `mod-ecoin/cadena-etica/ecoin-cadena-energetica.md`

---

## Tu checklist

- [ ] SNH-KIT operativo con energía solar
- [ ] SNH-OS actualizado con wallet ECOin y eMiner
- [ ] ECO minados / disponibles para transferencia
- [ ] Hash del bloque de minado capturado
- [ ] Transferencia al wallet del prestamista ejecutada
- [ ] Hash de la transferencia capturado
- [ ] Certificado de origen del nodo proporcionado al prestamista
