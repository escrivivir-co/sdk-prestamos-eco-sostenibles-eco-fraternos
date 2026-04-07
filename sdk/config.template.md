# Configuración del mod — plantilla

> Plantilla de configuración para instanciar el SDK de préstamos eco-sostenibles
> y eco-fraternos en un mod específico. Reemplazar todos los {{PLACEHOLDERS}}
> con los valores concretos del mod. Esta configuración es el contrato de identidad
> del mod: define la voz, los antagonistas, el corpus, el vocabulario, y el estilo
> que distinguen esta instanciación del SDK de cualquier otra.
>
> Basada en la estructura de `proyecto.config.md` del mod Plan Oro.
> Campo `extends: sdk/config.template.md` documenta la herencia conceptual.

---

# Configuración del mod: {{NOMBRE_MOD}}

> {{SUBTITULO_MOD}}

---

## Identidad

```yaml
extends: "sdk/config.template.md"
nombre: "{{NOMBRE_MOD}}"
mod: "{{SLUG_MOD}}"
sdk-base: "main"
descripcion: |
  {{DESCRIPCION_COMPLETA_MOD}}
  
  Activo: {{ACTIVO}} — {{DESCRIPCION_ACTIVO}}
  Proveedor: {{PROVEEDOR}} — {{DESCRIPCION_PROVEEDOR}}
  Receptor: {{RECEPTOR}} — {{DESCRIPCION_RECEPTOR}}
  Certificación: {{CERTIFICACION}}
  
  Dos ejes (heredados del SDK):
  (a) Eco-sostenible: {{DESCRIPCION_EJE_ECO_SOSTENIBLE_PARA_ESTE_ACTIVO}}
  (b) Eco-fraterno: {{DESCRIPCION_EJE_ECO_FRATERNO_PARA_ESTE_PRESTAMO}}
  
  Tres entregables: (1) {{ENTREGABLE_1}}, (2) {{ENTREGABLE_2}}, (3) {{ENTREGABLE_3}}.
  
  Operativamente, 5 fases según el framework del SDK.
  4 escenarios de devolución: (A) intacto, (B) devolución gradual,
  (C) liquidación corriente, (D) rebote e inversión.
  
  Cláusula clave: interés 0% con revalorización invertida (heredada del SDK).
  
  Portada y relato operativo: mod-{{SLUG_MOD}}/README.md
idioma: "{{IDIOMA}}"
fecha_inicio: "{{FECHA_INICIO}}"
jurisdiccion: "{{JURISDICCION}}"
origen: "{{DESCRIPCION_ORIGEN_DEL_PROYECTO}}"
```

---

## La Voz (configuración del protagonista)

```yaml
nombre: "{{NOMBRE_VOZ}}"
posicion: "{{POSICION_VOZ}}"
biografia: |
  {{BIOGRAFIA_VOZ}}
ejes:
  - nombre: "{{EJE_1_NOMBRE}}"
    posicion: "{{EJE_1_POSICION}}"
    expresion: "{{EJE_1_EXPRESION_CARACTERISTICA}}"
  - nombre: "{{EJE_2_NOMBRE}}"
    posicion: "{{EJE_2_POSICION}}"
    expresion: "{{EJE_2_EXPRESION_CARACTERISTICA}}"
influencias:
  - categoria: "Economía"
    nombres: ["{{INFLUENCIA_ECONOMIA_1}}", "{{INFLUENCIA_ECONOMIA_2}}"]
  - categoria: "Derecho"
    nombres: ["{{INFLUENCIA_DERECHO_1}}", "{{INFLUENCIA_DERECHO_2}}"]
  - categoria: "Filosofía"
    nombres: ["{{INFLUENCIA_FILOSOFIA_1}}", "{{INFLUENCIA_FILOSOFIA_2}}"]
paradojas: |
  {{PARADOJAS_DEL_MOD}}
puntos-ciegos:
  - "{{PUNTO_CIEGO_1}}"
  - "{{PUNTO_CIEGO_2}}"
  - "{{PUNTO_CIEGO_3}}"
```

---

## Antagonistas

> Los antagonistas no se inventan: se descubren. Son las voces que ya existen en la
> cabeza del prestamista, del receptor, y de cualquier lector externo que mire el proyecto
> con escepticismo legítimo. Nombrarlos es la mejor forma de responderles.

### El racionalista fiscal

```yaml
modelo: "{{RACIONALISTA_MODELO}}"
desafio-central: "{{RACIONALISTA_DESAFIO}}"
tensiones:
  - tema: "{{TENSION_1_TEMA}}"
    la-voz-dice: "{{TENSION_1_VOZ}}"
    el-antagonista-responde: "{{TENSION_1_ANTAGONISTA}}"
  - tema: "{{TENSION_2_TEMA}}"
    la-voz-dice: "{{TENSION_2_VOZ}}"
    el-antagonista-responde: "{{TENSION_2_ANTAGONISTA}}"
```

### El escéptico relacional

```yaml
modelo: "{{ESCEPTICO_MODELO}}"
desafio-central: "{{ESCEPTICO_DESAFIO}}"
tensiones:
  - tema: "{{ESCEPTICO_TENSION_1_TEMA}}"
    la-voz-dice: "{{ESCEPTICO_TENSION_1_VOZ}}"
    el-antagonista-responde: "{{ESCEPTICO_TENSION_1_ANTAGONISTA}}"
```

### {{ANTAGONISTA_3_NOMBRE}} (opcional — añadir según el mod)

```yaml
modelo: "{{ANTAGONISTA_3_MODELO}}"
desafio-central: "{{ANTAGONISTA_3_DESAFIO}}"
tensiones: []
```

---

## Corpus

```yaml
descripcion: "{{DESCRIPCION_CORPUS}}"
sdk-base:
  - ruta: "sdk/concepto.md"
    nombre: "Concepto: doble eje"
  - ruta: "sdk/framework-5-fases.md"
    nombre: "Framework operativo"
  - ruta: "sdk/escenarios.md"
    nombre: "Cuatro escenarios"
  - ruta: "sdk/legal/clausulas-base.md"
    nombre: "Cuatro cláusulas"
  - ruta: "sdk/legal/estructura-fiscal.md"
    nombre: "Triángulo fiscal"
  - ruta: "sdk/cadena-etica/criterios.md"
    nombre: "Criterios de cadena ética"
mod-especifico:
  - ruta: "mod-{{SLUG_MOD}}/README.md"
    nombre: "Portada y relato operativo del mod"
    descripcion: "{{DESCRIPCION_README_MOD}}"
  - ruta: "mod-{{SLUG_MOD}}/cadena-etica/{{REFERENCIA_CADENA}}"
    nombre: "Referencia de cadena ética del activo"
    descripcion: "{{DESCRIPCION_REFERENCIA_CADENA}}"
  - ruta: "mod-{{SLUG_MOD}}/roles/{{CUADERNILLO_PROVEEDOR}}"
    nombre: "Cuadernillo del proveedor"
    descripcion: "{{DESCRIPCION_CUADERNILLO_PROVEEDOR}}"
  - ruta: "mod-{{SLUG_MOD}}/roles/{{CUADERNILLO_PRESTAMISTA}}"
    nombre: "Cuadernillo del prestamista"
    descripcion: "{{DESCRIPCION_CUADERNILLO_PRESTAMISTA}}"
  - ruta: "mod-{{SLUG_MOD}}/roles/{{CUADERNILLO_RECEPTOR}}"
    nombre: "Cuadernillo del receptor"
    descripcion: "{{DESCRIPCION_CUADERNILLO_RECEPTOR}}"
  - ruta: "mod-{{SLUG_MOD}}/bitacoras/"
    nombre: "Bitácoras de las 5 fases"
    descripcion: "Registros operativos de cada fase"
  - ruta: "mod-{{SLUG_MOD}}/fuente/"
    nombre: "Material fuente del mod"
    descripcion: "{{DESCRIPCION_MATERIAL_FUENTE}}"
output:
  ruta: "mod-{{SLUG_MOD}}/output/"
  convencion: "{{CONVENCION_NOMENCLATURA_OUTPUT}}"
```

---

## Vocabulario

### Términos del SDK (heredados — no modificar)

```yaml
terminos-sdk:
  - termino: "Eco-sostenible"
    definicion: "Eje del préstamo: el {{ACTIVO}} como motor ético de riqueza a través del {{PROVEEDOR}}. El dinero circula, toca tierra, genera trabajo digno."
  - termino: "Eco-fraterno"
    definicion: "Eje del préstamo: el {{ACTIVO}} como reserva de riqueza que el receptor puede ignorar, custodiar, o emplear."
  - termino: "Cota-umbral-de-solvencia"
    definicion: "Condición contractual que define cuándo se activa la obligación de devolución."
  - termino: "Préstamo a fondo perdido"
    definicion: "Préstamo a interés 0% condicionado a recuperación financiera. Ficción jurídica que preserva la simetría entre prestamista y receptor."
  - termino: "Revalorización invertida"
    definicion: "Si el activo sube, se devuelve al valor del momento del préstamo. Si baja, el receptor conserva el beneficio."
```

### Términos específicos del mod

```yaml
terminos-mod:
  - termino: "{{TERMINO_MOD_1}}"
    definicion: "{{DEFINICION_MOD_1}}"
  - termino: "{{TERMINO_MOD_2}}"
    definicion: "{{DEFINICION_MOD_2}}"
```

### Personajes

```yaml
personajes:
  - nombre: "{{NOMBRE_PRESTAMISTA}}"
    funcion: "Prestamista. Motor del circuito."
  - nombre: "{{NOMBRE_RECEPTOR}}"
    funcion: "Receptor. Portador del {{ACTIVO}}."
  - nombre: "{{NOMBRE_PROVEEDOR}}"
    funcion: "Proveedor/artesano. Eslabón entre lo legal, lo material, y la cadena ética."
```

---

## Estilo

```yaml
voz: |
  {{DESCRIPCION_VOZ_ESTILO}}
  
  # Herencia del SDK: voz de ensayista que no distingue entre lo práctico y lo
  # filosófico. Frases largas con subordinadas que se abren como matrioskas.
  # Tono de sobremesa larga con alguien que sabe de leyes y de filosofía a partes iguales.
parrafo-modelo: |
  {{PARRAFO_MODELO_DEL_MOD}}
patrones-prohibidos:
  # Heredados del SDK — no eliminar:
  - "En resumen"
  - "Es importante destacar"
  - "Paso a paso"
  - Listas de viñetas como estructura principal
  - Separar lo legal de lo ensayístico
  - Tono de consultoría fiscal
  - Emojis
  # Específicos del mod:
  - "{{PATRON_PROHIBIDO_MOD_1}}"
```

---

## Para invocar al agente sobre este mod

```
@{agente} MOD-{{SLUG_MOD}} {tema}
```
