# Certificaciones éticas por tipo de activo

> Taxonomía de referencia del SDK. Mapea los tipos de activos más comunes
> en préstamos eco-sostenibles con sus certificaciones de cadena ética
> correspondientes. Cada mod seleccionará la columna pertinente para su activo.
> Esta tabla no es exhaustiva: nuevas certificaciones aparecen regularmente.
> Verificar vigencia antes de usarla.

---

## Por qué una taxonomía y no una guía única

El SDK es agnóstico respecto al tipo de activo: puede ser oro, textil, madera, café, piedras preciosas, o cualquier otro bien con cadena de producción y valor de mercado estable. La certificación ética varía radicalmente según el tipo de activo porque los problemas que certifica son diferentes: la minería artesanal tiene problemas de mercurio y trabajo de menores; el textil tiene problemas de agroquímicos y condiciones laborales; la madera tiene problemas de tala ilegal y deforestación. No existe una certificación universal.

Lo que esta taxonomía ofrece es la puerta de entrada correcta para cada categoría de activo: el organismo que certifica, el premium o mecanismo de impacto, y el distribuidor europeo más accesible para el mod. Un prestamista que trabaje con un activo no listado aquí debe aplicar los cuatro criterios de `cadena-etica/criterios.md` para evaluar la certificación disponible.

---

## Tabla de certificaciones por tipo de activo

### Metales preciosos (Oro, Plata, Platino)

| Elemento | Detalle |
|----------|---------|
| **Certificación principal** | **Fairmined** (Alliance for Responsible Mining, ARM, 2007) |
| **Organismo** | ARM, Colombia |
| **Premium al productor** | USD 4–6/g para oro; USD 6/g para Fairmined ECO (sin mercurio) |
| **Cobertura geográfica** | Colombia, Perú, Mongolia, Ecuador, Bolivia |
| **Auditoría** | Anual, tercera parte independiente |
| **Alternativa** | **Fairtrade Gold** (Fairtrade International) — USD 2.000/kg premium; 6,2+ toneladas exportadas en 10 años |
| **Distribuidor europeo principal** | Fairever (Alemania) — granalla, hilo, chapa, lingote. Envío a España. `fairever.com` |
| **Alternativas europeas** | C·HAFNER (DE), Valcambi (CH), Argor-Heraeus (CH) |
| **Alternativa reciclado** | **RJC Chain of Custody** (Responsible Jewellery Council) para oro reciclado con trazabilidad |
| **Referencia para el mod** | `mod-oro/cadena-etica/oro-ecoresponsable-referencia.md` |

---

### Textil (Algodón, Lino, Lana, Fibras naturales)

| Elemento | Detalle |
|----------|---------|
| **Certificación principal** | **GOTS** (Global Organic Textile Standard) |
| **Organismo** | GOTS consortium (DE/ES/UK) |
| **Alcance** | Producción orgánica + condiciones de trabajo en toda la cadena textil |
| **Premium** | No premium fijo; exige precio justo verificable |
| **Auditoría** | Anual, tercera parte acreditada |
| **Alternativa** | **Fairtrade Textiles** — textil especialmente algodón con premium fijo y auditoría social |
| **Alternativa complementaria** | **OEKO-TEX Standard 100** — ausencia de sustancias nocivas (no cubre lo social) |
| **Distribuidor tipo** | Tiendas de tejidos orgánicos con certificado GOTS; verificar en `oeko-tex.com/gots` |

---

### Madera y productos forestales

| Elemento | Detalle |
|----------|---------|
| **Certificación principal** | **FSC** (Forest Stewardship Council) |
| **Organismo** | FSC International, Bonn |
| **Alcance** | Gestión forestal sostenible + cadena de custodia desde el bosque |
| **Premium** | Variable según mercado; exige precio mínimo a productores forestales certificados |
| **Auditoría** | Periódica, tercera parte acreditada por FSC |
| **Alternativa** | **PEFC** (Programme for the Endorsement of Forest Certification) — reconocido equivalente |
| **Uso en préstamos** | Mobiliario artesanal, instrumentos musicales, objetos tallados, herramientas con mango |

---

### Alimentos y bebidas (Café, Cacao, Miel, Aceite de oliva)

| Elemento | Detalle |
|----------|---------|
| **Certificación principal** | **Fairtrade International** (productos agronómicos) |
| **Organismo** | Fairtrade International / Fairtrade España |
| **Premium** | Variable por producto — café: USD 0,20/lb sobre precio de mercado; cacao: USD 240/t |
| **Cobertura** | África, Latinoamérica, Asia |
| **Auditoría** | Anual, FLOCERT (tercera parte independiente) |
| **Alternativa** | **Rainforest Alliance** — cobertura ambiental más amplia, impacto social parcial |
| **Uso en préstamos** | Activos-alimentos con alta tasa de rotación o como capital semilla (p.ej., stock de cacao para pequeño comerciante) |

---

### Piedras preciosas y semipreciosas

| Elemento | Detalle |
|----------|---------|
| **Certificación principal** | **Process Kimberley** (diamantes) + **RJC** (Responsible Jewellery Council) |
| **Organismo** | Proceso Kimberley: intergubernamental; RJC: organismo privado sectorial |
| **Alcance Kimberley** | Solo diamantes, solo conflicto armado (no cubre condiciones laborales ni medioambiente) |
| **Alcance RJC** | Cadena completa: metales + gemas; criterios sociales, ambientales y de derechos humanos |
| **Limitación importante** | No existe para gemas de color (rubíes, zafiros, esmeraldas) un estándar tan consolidado como Fairmined; usar RJC o verificar certificados de origen país por país |
| **Referencia** | `www.responsiblejewellery.com` |

---

### Artesanía y bienes manufacturados complejos

| Elemento | Detalle |
|----------|---------|
| **Criterio aplicable** | Los criterios del SDK + Fair Trade Federation (FTF) o WFTO (World Fair Trade Organization) para el taller/cooperativa productora |
| **Organismo** | WFTO (World Fair Trade Organization), `wfto.com` |
| **Alcance** | Organizaciones de comercio justo en su totalidad — no solo un producto sino toda la organización productora |
| **Premium** | No estandarizado; exige verificación de que el precio pagado al productor cubre costes reales y margen digno |
| **Uso** | Bienes artesanales complejos (instrumentos, objetos decorativos, herramientas especializadas) de talleres de artesanos autónomos |

---

## Cómo elegir la certificación correcta para un mod

1. **Identificar el tipo de activo** — ¿es un metal precioso, un textil, una madera, un alimento, una piedra, o un bien artesanal complejo?
2. **Verificar si existe una certificación de tercera parte reconocida** para ese tipo de activo en el mercado europeo (la columna "Certificación principal" de la tabla)
3. **Confirmar que el proveedor de la materia prima puede suministrar con esa certificación** — si no puede, explorar alternativas o reciclado certificado
4. **Verificar que la certificación incluye mecanismo de premium y auditoría** — si solo cubre ausencia de daño pero no impacto positivo, complementar con otro criterio
5. **Archivar el certificado** en el anexo técnico del mod (ver `sdk/plantillas/anexo-tecnico.template.md`)

---

*Para los criterios generales que debe cumplir cualquier certificación, ver `cadena-etica/criterios.md`. Para la referencia específica del mod Plan Oro, ver `mod-oro/cadena-etica/oro-ecoresponsable-referencia.md`.*
