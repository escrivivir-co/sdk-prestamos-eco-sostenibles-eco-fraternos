# El triángulo fiscal del préstamo fraterno

> Documento de referencia del SDK. Describe la estructura fiscal de tres nodos
> — proveedor, prestamista, receptor — y su relación con la administración
> tributaria en el marco de un préstamo eco-sostenible y eco-fraterno.
> Cada mod debe verificar y completar este esquema para su jurisdicción concreta.

---

## Por qué el triángulo y no la línea recta

La intuición popular sobre los regalos entre familiares es que son invisibles para el Estado — que lo que circula entre parientes no tiene nombre fiscal ni casilla de autoliquidación. Esa intuición es sistémicamente falsa: la mayoría de las legislaciones contempla el impuesto sobre transmisiones gratuitas precisamente para capturar las transferencias de riqueza que se producen por vínculo familiar sin contraprestación. Y la mayoría de los estados también tiene mecanismos para detectar préstamos encubiertos como donaciones, porque un préstamo entre parientes a interés 0% con probabilidad cero de devolución se parece mucho, desde fuera, a una donación con papeles.

El SDK no diseña para evadir esa fiscalidad: diseña para que la estructura del préstamo sea lo que dice ser — un préstamo, no una donación — y pueda demostrarlo con documentos. El triángulo fiscal es la representación de las tres relaciones que existen en este modelo y que la administración tributaria puede analizar por separado o en conjunto.

---

## Los tres nodos del triángulo

```
          ADMINISTRACIÓN TRIBUTARIA
                    │
         ┌──────────┼──────────┐
         │          │          │
         ▼          ▼          ▼
    PROVEEDOR  PRESTAMISTA  RECEPTOR
         │                    │
         └────────────────────┘
              (no hay relación
               directa fiscal)
```

**Proveedor → Administración:** El proveedor mantiene una relación mercantil ordinaria con la administración tributaria. Factura el {{ACTIVO}} con el impuesto indirecto que le corresponde, lo declara en sus modelos periódicos, y declara los ingresos en su impuesto sobre la renta. Su participación en el proyecto empieza y termina con la factura. No tiene relación directa con el receptor a efectos fiscales.

**Prestamista → Administración:** El prestamista formaliza el préstamo ante la administración tributaria en el plazo establecido por la jurisdicción del mod. Presenta la documentación del triángulo completo (factura del proveedor + contrato de préstamo + documentación del receptor). No paga el impuesto sobre transmisiones gratuitas porque no hay transmisión gratuita: hay préstamo. No paga impuesto sobre rendimientos del capital porque el interés es 0%.

**Receptor → Administración:** El receptor recibe el bien bajo contrato de préstamo, no como donación, lo que le exime del impuesto sobre transmisiones gratuitas en el momento de la entrega. Si en un momento posterior vende módulos del {{ACTIVO}} a precio superior al valor nominal del préstamo, puede existir una ganancia patrimonial sujeta a declaración. El contrato documenta el valor de adquisición del receptor (el valor nominal del préstamo) a efectos de calcular esa ganancia.

---

## Lo que el triángulo necesita para sostenerse

El triángulo no es solo una descripción conceptual: es la razón por la que la documentación del SDK existe. Cada lado del triángulo necesita sus documentos:

**Lado proveedor–prestamista:**
- Factura del proveedor con desglose completo (materia prima + mano de obra + impuesto indirecto)
- Certificado de trazabilidad / certificación ética de los materiales

**Lado prestamista–receptor:**
- Contrato de préstamo con las 4 cláusulas base
- Anexo técnico del activo prestado
- Documentación de la situación económica del receptor (que motiva la condición-umbral)
- Acta de entrega

**Lado prestamista–administración:**
- Justificante de presentación del préstamo ante la administración tributaria
- Copia de toda la documentación anterior, archivada durante la ventana de inspección

---

## Gestión del impuesto sobre transmisiones gratuitas

El impuesto sobre transmisiones gratuitas — en España, el ISD (Impuesto sobre Sucesiones y Donaciones); en otras jurisdicciones, equivalentes como el *gift tax* anglosajón o el *droits de donation* francés — grava las transmisiones patrimoniales sin contraprestación. Un préstamo no es una transmisión sin contraprestación: es una transmisión con contraprestación diferida (la devolución).

La defensa del mod ante la administración tributaria tiene dos pilares:

1. **El contrato de préstamo existe.** Hay un documento firmado que establece la obligación de devolución, aunque sea condicional. La obligación no es cero: es condicional. Un préstamo condicional continúa siendo un préstamo.

2. **Las cuatro cláusulas son coherentes entre sí.** El interés 0% no transforma el préstamo en donación: existe jurisprudencia en múltiples jurisdicciones que admite préstamos a interés 0% entre particulares, especialmente cuando existen circunstancias documentadas que los justifican (insolvencia del receptor, vínculo familiar, intención de recuperación). La clave es que las circunstancias estén documentadas.

<!-- MOD: Completar con el análisis específico de la jurisdicción del mod — 
     nombre del impuesto en cuestión, umbral de exención por parentesco,
     modelo de autoliquidación, plazo de presentación, y referencia legal. -->

---

## La ventana de inspección

La administración tributaria puede inspeccionar las operaciones realizadas en un período determinado desde la fecha de la operación — la "ventana de inspección". Durante ese período, toda la documentación del triángulo debe estar accesible y en condiciones de ser presentada on demand.

<!-- MOD: Especificar la ventana de inspección de la jurisdicción del mod.
     Por ejemplo, en España son 4 años para la mayoría de tributos. -->

**Criterio práctico:** archivar toda la documentación del préstamo durante al menos `{{VENTANA_INSPECCION}}` desde la fecha de formalización (Fase 5), con acceso inmediato. No es necesario que sea un archivo sofisticado: es necesario que exista y que sea completo.

---

## El rol de la administración como tercer actor racional

Hay una tensión explícita en este modelo que vale la pena nombrar: la administración tributaria no es un antagonista del préstamo fraterno — es un actor racional que intenta clasificar operaciones para aplicar las normas que el sistema ha establecido. El SDK no combate esa clasificación: proporciona los documentos que permiten que la clasificación correcta sea la que el prestamista y el receptor quieren que sea, que es "préstamo", no "donación encubierta".

Como decía el inspector de Hacienda: "Marque la casilla. Modelo de declaración correspondiente o contrato de préstamo. No hay casilla para 'fraternidad'." El SDK acepta ese marco y contesta: tiene razón, use el contrato de préstamo — aquí tiene todas las piezas.

---

*Para las cláusulas específicas que sostienen esta estructura, ver `legal/clausulas-base.md`. Para el registro y seguimiento de la Fase 5, ver `plantillas/registro-devoluciones.template.md`.*
