# Anexo Técnico del activo — plantilla

> Documento que describe el {{ACTIVO}} en detalle a efectos del contrato de préstamo.
> Se elabora en la Fase 2 (Documentar el activo) y se adjunta al contrato.
> Instanciar: reemplazar {{ACTIVO}}, {{PROVEEDOR}}, {{MATERIAL}}, {{CERTIFICACION}},
> y adaptar la tabla de módulos a la naturaleza del activo del mod.

---

## Identificación del Anexo

- **Nº de Anexo Técnico:** `{{NUM_ANEXO}}`
- **Asociado al contrato de préstamo:** `{{REF_CONTRATO}}`
- **Fecha de elaboración:** `____-__-__`
- **Elaborado por:** `{{NOMBRE_PRESTAMISTA}}`

---

## 1. Descripción del activo

- **Denominación:** `{{NOMBRE_ACTIVO}}`
- **Tipo de objeto:** `{{TIPO_OBJETO}}`
- **Descripción física:** <!-- Breve descripción del objeto: forma, dimensiones, características generales -->
- **Número de módulos/piezas:** `{{N_MODULOS}}`
- **Modularidad:** `[ ] Sí — piezas individuales independientes` / `[ ] No — objeto único`
- **Fabricado por:** `{{NOMBRE_PROVEEDOR}}`
- **Fecha de fabricación/adquisición:** `____-__-__`
- **Número de factura:** `{{NUM_FACTURA}}`

---

## 2. Materiales y certificación ética

- **Material principal:** `{{MATERIAL_PRINCIPAL}}`
- **Composición:** <!-- Especificar aleación, pureza, mezcla, u otros datos de composición -->
- **Certificación ética:** `{{CERTIFICACION}}`
- **Proveedor del material certificado:** `{{PROVEEDOR_MATERIAL}}`
- **País/región de origen del material:** `{{PAIS_ORIGEN}}`
- **Número o referencia del certificado de trazabilidad:** `{{REF_CERTIFICADO}}`
- **Fecha del certificado:** `____-__-__`

---

## 3. Tabla de módulos/piezas

> Si el activo es un objeto único (no modular), usar una sola fila y omitir la columna "Módulo".
> Si es modular, listar cada módulo con su peso/medida, composición, y valor.

| Módulo # | Descripción | Peso / Medida | Material / Composición | Valor nominal ({{MONEDA}}) | Observaciones |
|---------|-------------|---------------|----------------------|--------------------------|---------------|
| 1 | | | | | |
| 2 | | | | | |
| 3 | | | | | |
| 4 | | | | | |
| 5 | | | | | |
| ... | | | | | |
| **Total** | | | | **`______ {{MONEDA}}`** | |

---

## 4. Valoración

- **Valor total de adquisición (según factura):** `{{VALOR_FACTURA}} {{MONEDA}}`
  - del cual, materia prima: `{{VALOR_MATERIA_PRIMA}} {{MONEDA}}`
  - del cual, mano de obra: `{{VALOR_MANO_OBRA}} {{MONEDA}}`
  - del cual, impuesto indirecto (`{{TIPO_IMPUESTO}}`): `{{VALOR_IMPUESTO}} {{MONEDA}}`
- **Valor de referencia para el préstamo (base imponible sin impuesto):** `{{VALOR_PRESTAMO}} {{MONEDA}}`
- **Tasación independiente:** `[ ] Realizada` / `[ ] No realizada`
  - Si realizada — entidad tasadora: `________` / fecha: `____-__-__` / valor tasado: `______ {{MONEDA}}`

---

## 5. Registro visual (fotografías / documentación técnica)

| Archivo | Descripción | Fecha |
|---------|-------------|-------|
| `foto_conjunto_01.jpg` | Vista general del {{ACTIVO}} completo | |
| `foto_modulo_XX.jpg` | Vista individual módulo XX | |
| ... | | |

- **Número total de archivos adjuntos:** `__`
- **Almacenados en:** `{{RUTA_FOTOS}}`

---

## 6. Firmas

El presente Anexo Técnico ha sido revisado y aceptado por ambas partes como descripción fiel y precisa del bien prestado:

**El prestamista:** ____________________  Fecha: ____-__-__

**El receptor:** ____________________  Fecha: ____-__-__

---

*Este Anexo forma parte inseparable del Contrato de Préstamo `{{REF_CONTRATO}}`.*
