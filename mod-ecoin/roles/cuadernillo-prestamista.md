# Cuadernillo para el prestamista — mod ECOin

> Documento dirigido a quien posee ECOin y decide prestarlos bajo las
> condiciones del SDK: interés 0 %, revalorización invertida,
> condición-umbral de solvencia, y devolución parcial en especie.

---

## Tu posición en el circuito

Tienes ECO. Los has minado tú mismo con un SNH-KIT solar, o los has adquirido de un nodo proveedor. Ahora vas a prestarlos a alguien que los necesita — no como inversión, no como caridad, sino como suelo fraterno dentro de la red Oasis.

Eres el motor del circuito. Tú:

1. **Financias.** Los ECO son tuyos y los pones a disposición del receptor.
2. **Formalizas.** Dos documentos: (a) un Transfer en Oasis con metadata del préstamo, y (b) un contrato civil en tu jurisdicción que documente las 4 cláusulas del SDK.
3. **Asumes riesgo.** Si el receptor nunca supera el umbral de solvencia, no devuelve. Si ECOin pierde valor, la pérdida es tuya. Si la red desaparece, la deuda se extingue con ella.
4. **Registras.** Documentas la operación para tu declaración fiscal y para el seguimiento del préstamo.

---

## Las 4 cláusulas adaptadas a ECOin

### [01] Interés 0 %

El receptor no paga intereses. Nunca. El staking POS que genera el ECO en su wallet es del receptor, no tuyo. El tiempo no penaliza.

### [02] Revalorización invertida

Si ECO sube de valor respecto a moneda fiat entre el momento del préstamo y el de la devolución, el receptor devuelve al valor nominal del préstamo (cantidad de ECO, no equivalente fiat). La plusvalía fiat es del receptor. Si ECO baja, la pérdida de referencia fiat la absorbes tú.

> Nota: en una economía cerrada como Oasis, la revalorización fiat es secundaria. Lo relevante es la capacidad de operación del receptor dentro de la red.

### [03] Condición-umbral de solvencia

La obligación de devolución solo se activa si el receptor alcanza autonomía operativa dentro de la red Oasis. Definir "autonomía" en el contrato civil: puede ser capacidad de generar ingresos vía marketplace, recibir UBI consistente, o cualquier indicador acordado entre las partes.

### [04] Devolución parcial en especie

El receptor devuelve ECO — no fiat, no servicios, no equivalentes. Transfer por transfer. Sin calendario. Sin penalización por discontinuidad. Cada devolución es un hash verificable.

---

## La doble formalización

### En la red: Transfer Oasis

Ejecutar una transferencia de ECO al wallet del receptor usando el módulo Transfers de Oasis. Incluir en la metadata o en una nota asociada:
- Naturaleza: préstamo al 0 % con condiciones SDK
- Cantidad de ECO
- Valor de referencia fiat en el momento (si aplica)
- Referencia al contrato civil

### Fuera de la red: contrato civil

El préstamo al 0 % necesita existir ante la administración tributaria de tu jurisdicción. El contrato civil debe incluir:
- Las 4 cláusulas del SDK
- Identificación de las partes (con sus direcciones ECOin como referencia adicional)
- Hash de la transacción de préstamo como prueba de entrega
- Valor de referencia fiat al momento del préstamo
- Jurisdicción y legislación aplicable

> Para la plantilla de contrato: `sdk/plantillas/contrato-prestamo.template.md`
> Para la estructura fiscal genérica: `sdk/legal/estructura-fiscal.md`

---

## Obligaciones fiscales

**Esto depende de tu jurisdicción.** Algunos puntos generales:

- En muchas jurisdicciones, la transferencia de criptoactivos a título de préstamo no genera ISD (Impuesto de Sucesiones y Donaciones) si hay contrato que documente la naturaleza de préstamo.
- El préstamo al 0 % en criptoactivos puede ser revisado por la administración tributaria como donación encubierta. Las 4 cláusulas (especialmente la condición-umbral) y el contrato civil son tu defensa.
- El hash de la transacción en el block explorer es tu prueba de trazabilidad.
- Consulta con un asesor fiscal la obligación de declarar la tenencia y transmisión de criptoactivos en tu jurisdicción.

---

## Seguimiento del préstamo

El estado del préstamo se verifica en dos planos:

1. **On-chain:** El block explorer de ECOin (`ecoin.03c8.net/blockexplorer`) muestra el saldo del wallet del receptor y las transacciones. Las devoluciones son transfers de vuelta a tu wallet.
2. **Off-chain:** El registro de retornos del mod (`mod-ecoin/bitacoras/`) documenta cada devolución con fecha, cantidad, hash, y estado del umbral de solvencia.

---

## Tu checklist por fase

### Fase 1 — Comisionar
- [ ] ECO disponibles en tu wallet (minados o adquiridos del nodo proveedor)
- [ ] Documentación de origen (hash de minado, certificado del nodo proveedor)

### Fase 2 — Documentar
- [ ] Captura del block explorer con tu saldo
- [ ] Certificado de cadena ética del proveedor (si aplica)

### Fase 3 — Formalizar
- [ ] Contrato civil redactado con las 4 cláusulas
- [ ] Definición del umbral de solvencia acordada con el receptor
- [ ] Contrato firmado por ambas partes

### Fase 4 — Entregar
- [ ] Transfer ejecutado en Oasis
- [ ] Hash de la transacción capturado
- [ ] Cuaderno-receptor entregado

### Fase 5 — Registrar
- [ ] Presentación fiscal según jurisdicción (si aplica)
- [ ] Registro de retornos iniciado
- [ ] Bitácoras actualizadas
