# Registro de retornos — plantilla

> Documento de seguimiento continuo de los retornos del préstamo fraterno.
> Se abre en la Fase 5 y permanece activo mientras haya préstamo vigente.
> Se actualiza en el momento exacto de cada retorno — nunca retroactivamente.
> Instanciar: reemplazar {{ACTIVO}}, {{N_MODULOS}}, {{MONEDA}}, {{REF_CONTRATO}}.

---

## Datos del préstamo

- **Referencia del contrato:** `{{REF_CONTRATO}}`
- **Prestamista:** `{{NOMBRE_PRESTAMISTA}}`
- **Receptor:** `{{NOMBRE_RECEPTOR}}`
- **Fecha de entrega (Fase 4):** `____-__-__`
- **Activo prestado:** `{{ACTIVO_DESCRIPTION}}`
- **Número de módulos prestados:** `{{N_MODULOS}}`
- **Valor total nominal del préstamo:** `{{VALOR_TOTAL_PRESTAMO}} {{MONEDA}}`

---

## Estado actual del préstamo

- **Escenario activo:** `[ ] A — Intacto` / `[ ] B — Devolución gradual` / `[ ] C — Liquidación` / `[ ] D — Rebote`
- **Fecha de última actualización:** `____-__-__`
- **Módulos devueltos acumulados:** `__ / {{N_MODULOS}}`
- **Valor devuelto acumulado (nominal):** `______ {{MONEDA}}`
- **Saldo pendiente (nominal):** `______ {{MONEDA}}`

---

## Registro de retornos

> Cada fila registra un retorno parcial. Firmar en el momento. No completar a posteriori.

| # | Fecha | Módulo(s) ref. | Forma | Valor nominal ({{MONEDA}}) | Firma receptor | Firma prestamista |
|---|-------|---------------|-------|--------------------------|----------------|-------------------|
| 1 | | | `[ ] Especie` / `[ ] Moneda` | | | |
| 2 | | | `[ ] Especie` / `[ ] Moneda` | | | |
| 3 | | | `[ ] Especie` / `[ ] Moneda` | | | |
| 4 | | | `[ ] Especie` / `[ ] Moneda` | | | |
| 5 | | | `[ ] Especie` / `[ ] Moneda` | | | |
| 6 | | | `[ ] Especie` / `[ ] Moneda` | | | |
| 7 | | | `[ ] Especie` / `[ ] Moneda` | | | |
| 8 | | | `[ ] Especie` / `[ ] Moneda` | | | |

---

## Incidencias y suspensiones

> Registrar cualquier variación del escenario activo, suspensión del préstamo
> por nueva insolvencia del receptor, reconducción de escenario, o condiciones especiales.

| Fecha | Tipo de incidencia | Detalle | Firma receptor | Firma prestamista |
|-------|-------------------|---------|----------------|-------------------|
| | `[ ] Suspensión` / `[ ] Reanudación` / `[ ] Cambio escenario` / `[ ] Otra` | | | |
| | | | | |

---

## Cierre del préstamo (si aplica)

- **Fecha de cierre:** `____-__-__`
- **Motivo de cierre:**
  - `[ ] Devolución completa (Escenario B o D finalizado)`
  - `[ ] Condonación del saldo — acta firmada adjunta`
  - `[ ] Vencimiento del plazo máximo del contrato`
  - `[ ] Otro: ________`
- **Saldo final devuelto:** `______ {{MONEDA}}`
- **Saldo condonado (si aplica):** `______ {{MONEDA}}`

**Firma del prestamista:** ____________________  Fecha: ____-__-__

**Firma del receptor:** ____________________  Fecha: ____-__-__

---

*Este registro forma parte de la Bitácora Fase 5 del préstamo `{{REF_CONTRATO}}`.*
