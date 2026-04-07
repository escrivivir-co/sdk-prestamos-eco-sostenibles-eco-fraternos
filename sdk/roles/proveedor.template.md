# Cuadernillo para el {{PROVEEDOR}} — plantilla

> Documento dirigido al artesano, productor, o proveedor que fabricará o
> suministrará el {{ACTIVO}}. Instanciar este template para el mod específico:
> reemplazar {{PROVEEDOR}}, {{ACTIVO}}, {{PIEZA}}, {{CERTIFICACION}},
> {{PROVEEDOR_MATERIA}}, y los demás marcadores de sección.
>
> Las secciones marcadas con `<!-- MOD: ... -->` requieren contenido específico del mod.

---

## Qué es este proyecto

<!-- MOD: Explicar quién encarga, qué es el {{ACTIVO}}, para qué sirve, quién lo recibirá. Concretamente: la relación entre el prestamista y el {{PROVEEDOR}}, la naturaleza del encargo, el contexto fraterno del préstamo. -->

Tu papel en este proyecto tiene tres caras:

1. **Artesano/Productor.** Diseñas y fabricas el {{ACTIVO}} con los materiales y la calidad que tu oficio exige.
2. **Eslabón ético.** Los materiales que uses deben tener trazabilidad certificada — específicamente, `{{CERTIFICACION}}`. No es un capricho: es la columna vertebral del eje eco-sostenible del proyecto.
3. **Tercero fiscal.** Aunque puede existir vínculo personal entre tú y el prestamista, para la administración tributaria eres un tercero comercial. Facturas con el impuesto indirecto que corresponda, declaras en tus modelos tributarios periódicos, y tu relación con el encargo es mercantil.

---

## Especificaciones del encargo

### El {{ACTIVO}}

<!-- MOD: Descripción técnica del {{ACTIVO}} — tipo de objeto, número de módulos/piezas si aplica, valor objetivo por unidad, requisito funcional de modularidad si aplica, libertad de diseño dentro de las restricciones funcionales. -->

- **Tipo:** `{{TIPO_OBJETO}}`
- **Módulos/piezas:** `{{N_MODULOS}}`, cada uno independiente si aplica
- **Valor objetivo por módulo:** `{{VALOR_MODULO}}` (orientativo)
- **Requisito funcional:** <!-- MOD: Describir qué tiene que poder hacer el receptor con cada pieza/módulo -->
- **Diseño:** Libertad creativa dentro de las restricciones funcionales. Lo que importa es que la funcionalidad de separabilidad esté garantizada si aplica.

### Los materiales

- **Certificación exigida:** `{{CERTIFICACION}}`
- **Proveedor recomendado:** `{{PROVEEDOR_MATERIA_RECOMENDADO}}`
- **Alternativas:** <!-- MOD: listar alternativas de proveedores con certificación equivalente -->
- **Formato:** A criterio del {{PROVEEDOR}} según su técnica
- **Se pedirá:** Certificado de trazabilidad de los materiales utilizados

> El pack completo de proveedores, certificaciones y cadena de suministro está en `{{MOD_PATH}}/cadena-etica/{{REFERENCIA_CADENA}}`.

---

## Facturación y obligaciones fiscales

Aunque exista relación personal entre tú y el prestamista, la operación es mercantil a todos los efectos:

### Lo que debes facturar

Factura completa con:
- Base imponible desglosada: materia prima (con trazabilidad) + mano de obra
- Impuesto indirecto al tipo que corresponda según jurisdicción (`{{TIPO_IVA_O_EQUIVALENTE}}`)
- Total
- Tus datos fiscales completos
- Datos del comprador
- Número de factura y fecha

### Lo que debes declarar

- Declaración periódica del impuesto indirecto (`{{MODELO_TRIMESTRAL}}`)
- Declaración anual (`{{MODELO_ANUAL}}`)
- IRPF o equivalente: los ingresos de esta factura son como cualquier otro ingreso de tu actividad

### Lo que NO te corresponde

- No eres parte del contrato de préstamo entre prestamista y receptor. Fabricas y facturas un bien; lo que hagan con él después es asunto del prestamista y el receptor.
- No tienes obligación respecto al impuesto sobre transmisiones gratuitas. Eso es entre ellos y la administración tributaria.
- Si alguien de la administración te pregunta, tu posición es: "Fabriqué y facturé el bien `{{ACTIVO}}` por encargo."

---

## Documentación que se te pedirá

1. **Factura** con desglose completo (materia prima / mano de obra / impuesto indirecto)
2. **Certificado de trazabilidad** de los materiales utilizados — lo proporciona el `{{PROVEEDOR_MATERIA}}`
3. **Registro visual** del {{ACTIVO}} y sus módulos/piezas (fotografías o equivalente) para el anexo técnico
4. **Pesos o medidas** de cada módulo si aplica
5. **Composición** de cada módulo (materiales, aleaciones, elementos si aplica)

Todo esto se archivará en la carpeta del proyecto y formará parte de la documentación que el prestamista presentará ante la administración tributaria. Tu nombre aparecerá en la factura; tu oficio, en el {{ACTIVO}}.

---

## Plazos

<!-- MOD: Personalizar si hay plazos relevantes para el mod. -->

Los plazos los marcas tú. El proyecto no tiene prisa — tiene rigor. Lo que sí necesitamos es:

- Una **fecha estimada de entrega** para coordinar las fases siguientes
- **Comunicación** si hay retrasos, cambios en el diseño, o incidencias con el proveedor de materiales

---

## Referencia

- Este cuadernillo forma parte del framework SDK de préstamos eco-sostenibles y eco-fraternos
- La documentación completa del mod está en `{{MOD_PATH}}/`
- Cualquier duda sobre el contexto del proyecto, pregúntale al prestamista. Él tiene el relato completo.
