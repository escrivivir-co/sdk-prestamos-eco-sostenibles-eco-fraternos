# Cuadernillo para el prestamista — plantilla

> Documento dirigido a quien financia, organiza y formaliza el préstamo.
> Instanciar este template para el mod específico: reemplazar {{PRESTAMISTA}},
> {{RECEPTOR}}, {{PROVEEDOR}}, {{ACTIVO}}, {{PIEZA}}, {{N_MODULOS}},
> {{JURISDICCION}}, {{PLAZO_PRESENTACION}}, {{VENTANA_INSPECCION}}.
>
> Las secciones marcadas con `<!-- MOD: ... -->` requieren contenido específico del mod.

---

## Tu papel en este proyecto

Eres el motor del circuito. Pones los recursos, coordinas a las partes, formalizas ante la administración tributaria, y asumes el riesgo de que el préstamo no se devuelva nunca. Eso ya lo sabes. Este cuadernillo es tu guía operativa para que nada se quede sin hacer, sin firmar, o sin archivar.

---

## Las 5 fases — resumen operativo

| Fase | Qué hacer | Documento de registro |
|------|-----------|----------------------|
| **1. Comisionar el activo** | Hablar con el {{PROVEEDOR}}, definir encargo, elegir materiales certificados, acordar precio y plazo | `bitacora-fase-1.md` |
| **2. Documentar el activo** | Recibir factura, elaborar anexo técnico, registrar visualmente el {{ACTIVO}}, tasación opcional | `bitacora-fase-2.md` |
| **3. Formalizar el préstamo** | Redactar contrato con 4 cláusulas base, reunir documentación del receptor, firmar | `bitacora-fase-3.md` |
| **4. Acto de entrega** | Entregar {{ACTIVO}} + contrato + cuadernillo del receptor, registrar el acto | `bitacora-fase-4.md` |
| **5. Registro y seguimiento** | Presentar ante la administración tributaria en plazo, archivar todo, registrar retornos | `bitacora-fase-5.md` |

Cada fase tiene su bitácora con puntos preparados para rellenar sobre la marcha. No dejes la documentación para después: documenta en el momento.

---

## Tus obligaciones fiscales

### Lo que NO pagas

<!-- MOD: Especificar para la jurisdicción del mod qué impuestos no aplican en este tipo de préstamo a interés 0%. -->

- **Impuesto sobre transmisiones gratuitas:** No aplica porque no es donación. Es préstamo a interés 0%.
- **Impuesto sobre rendimientos del préstamo:** No hay rendimientos porque el interés es 0%.

### Lo que SÍ debes hacer

1. **Formalizar el préstamo** ante la administración tributaria como préstamo entre particulares a interés 0%
2. **Presentar documentación** en `{{JURISDICCION}}` dentro del plazo legal (`{{PLAZO_PRESENTACION}}` — verificar para tu jurisdicción concreta)
3. **Conservar toda la documentación** durante al menos `{{VENTANA_INSPECCION}}` (verificar ventana de inspección en tu jurisdicción)

### Documentación a presentar

<!-- MOD: Completar con los modelos y formularios específicos de la jurisdicción. -->

- Contrato de préstamo firmado (o escritura notarial)
- Factura del {{PROVEEDOR}} con desglose y impuesto indirecto
- Anexo técnico del {{ACTIVO}} con registros y valoración
- Documentación acreditativa de la situación económica del receptor
- Datos fiscales de ambas partes
- Certificado de trazabilidad / certificación ética de los materiales

---

## Las 4 cláusulas clave — lo que firmaste

Repaso para que las tengas presentes en todo momento:

### 1. Interés 0%
No se generan intereses. La justificación: préstamo fraterno, receptor en situación de insolvencia documentada, contrato firmado con intención documentada de devolución.

### 2. Revalorización invertida
Si el {{ACTIVO}} sube de valor entre la fecha del préstamo y la devolución, el receptor devuelve al **valor del momento del préstamo**, no al de mercado. Si baja, el receptor conserva el beneficio. Tú asumes el riesgo del activo porque tú elegiste el vehículo.

### 3. Condición-umbral-de-solvencia
La devolución solo se activa si el receptor supera la situación de insolvencia definida en el contrato. Mientras esté por debajo del umbral, el préstamo queda en suspenso. Si nunca supera el umbral, nunca devuelve.

### 4. Devolución parcial en especie
Módulo a módulo. Sin orden, sin calendario, sin penalización. Cada devolución se registra con firma o acta en la bitácora de Fase 5.

---

## Los 4 escenarios posibles

Una vez entregado el {{ACTIVO}}, pueden pasar cuatro cosas. Las cuatro son legítimas — ver `sdk/escenarios.md` para el detalle de cada una.

| Escenario | Qué pasa | Tu posición |
|-----------|----------|-------------|
| **A: Intacto** | Conserva el {{ACTIVO}} para siempre. No supera el umbral. | El préstamo queda en suspenso perpetuo. De facto, es un regalo. |
| **B: Gradual** | Devuelve módulo a módulo según puede. | Registra cada devolución. El valor es el del momento del préstamo. |
| **C: Liquidación** | Vende módulos para gastos vitales. El {{ACTIVO}} desaparece. | Cumplió su función. No hay devolución. |
| **D: Rebote** | Usa módulos como capital semilla, se estabiliza, devuelve. | El mejor escenario. Registra y celebra. |

---

## Registro de devoluciones

> Este registro se mantiene también en `bitacora-fase-5.md`.
> Aquí tienes una copia para tu control personal.

| # | Fecha | Módulo(s) | Forma (especie/moneda) | Valor préstamo | Firma |
|---|-------|-----------|----------------------|---------------|-------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |

- **Módulos devueltos:** `__ / {{N_MODULOS}}`
- **Valor devuelto (nominal préstamo):** `______ {{MONEDA}}`

---

## Documentación que debes conservar (mínimo `{{VENTANA_INSPECCION}}`)

- `[ ]` Contrato de préstamo firmado (original)
- `[ ]` Factura del {{PROVEEDOR}}
- `[ ]` Anexo técnico del {{ACTIVO}}
- `[ ]` Certificado de trazabilidad / certificación ética
- `[ ]` Documentación de la situación económica del receptor
- `[ ]` Justificante de presentación ante la administración tributaria
- `[ ]` Registro visual del {{ACTIVO}}
- `[ ]` Tasación independiente (si se hizo)
- `[ ]` Copia del cuadernillo del receptor entregado
- `[ ]` Registro de devoluciones (actualizado)
- `[ ]` Bitácoras de las 5 fases (completadas)

---

## Referencia rápida

<!-- MOD: Actualizar con las rutas de carpeta del mod específico. -->

- Carpeta del mod: `{{MOD_PATH}}/`
- Portada general: `{{MOD_PATH}}/README.md`
- Referencia de cadena ética: `{{MOD_PATH}}/cadena-etica/`
- Cuadernillo del receptor: `{{MOD_PATH}}/roles/{{CUADERNILLO_RECEPTOR}}`
