# SDK de préstamos eco-sostenibles y eco-fraternos

> Framework documental para estructurar préstamos fraternos de bienes con cadena
> ética — desde la comisión del activo hasta su seguimiento y resolución legal.
> Raíz de la rama `main`. Los mods específicos residen en sus propias ramas (`mods/*`).

**Exordio — por qué existe este SDK:** [`sdk/lore.md`](sdk/lore.md)

---

## El doble eje

Todo préstamo instanciado desde este SDK se sostiene sobre dos principios que no son decorativos: son la razón de que el préstamo exista con esta forma y no con otra.

**Eco-sostenible.** El préstamo activa la economía con cuidado de la cadena completa. El activo que se presta no se adquiere por el canal más barato: pasa primero por las manos de un proveedor que trabaja en condiciones dignas, con materiales de cadena ética certificada, y genera trabajo real y tributable en el proceso. El dinero circula antes de llegar al receptor: toca tierra, genera impacto, deja huella documental. La eco-sostenibilidad no es un adjetivo del activo: es la arquitectura del encargo.

**Eco-fraterno.** El préstamo ofrece suelo económico fraterno. El activo que llega al receptor no lleva un contador de intereses ni una fecha de vencimiento perentoria: llega como infraestructura de agencia — algo que puede conservarse, custodiarse, o emplearse según lo exija la vida, sin que ninguna de esas decisiones active penalización ni genere vergüenza legal. El contrato formaliza ante la administración tributaria lo que en el fondo es un acto de fe: que el prestamista presta lo que está dispuesto a no recuperar, y que el receptor recibe algo que le pertenece de verdad aunque deba devolverlo si puede.

Para el desarrollo conceptual completo: `sdk/concepto.md`.

---

## La estructura del SDK

```
sdk/
  lore.md                           ← Exordio editorial desde escrivivir.co
  concepto.md                       ← El doble eje fundamentado
  framework-5-fases.md              ← Las 5 fases operativas genéricas
  escenarios.md                     ← Los 4 escenarios de devolución
  roles/
    proveedor.template.md           ← Plantilla: artesano/proveedor
    prestamista.template.md         ← Plantilla: prestamista
    receptor.template.md            ← Plantilla: receptor
  plantillas/
    bitacora-fase.template.md       ← Plantilla genérica de bitácora (×5)
    contrato-prestamo.template.md   ← Contrato con las 4 cláusulas base
    anexo-tecnico.template.md       ← Tabla de módulos y valoración
    registro-devoluciones.template.md ← Registro de retornos
  legal/
    estructura-fiscal.md            ← Triángulo fiscal genérico
    clausulas-base.md               ← Las 4 cláusulas: su razón de ser
  cadena-etica/
    criterios.md                    ← Qué significa "cadena ética" para cualquier activo
    certificaciones-tipo.md         ← Fairmined, FSC, GOTS, Fairtrade y equivalentes
  config.template.md                ← Plantilla de proyecto.config para cada mod
```

---

## Las cinco fases

Todo préstamo eco-sostenible y eco-fraterno recorre cinco fases desde el encargo hasta el seguimiento:

| Fase | Nombre genérico | Qué produce |
|------|----------------|-------------|
| **1** | Comisionar el activo | Encargo al proveedor con especificaciones éticas |
| **2** | Documentar el activo | Factura, certificado de trazabilidad, anexo técnico |
| **3** | Formalizar el préstamo | Contrato con 4 cláusulas, documentación del receptor |
| **4** | Acto de entrega | Entrega física, acta firmada, cuadernillo al receptor |
| **5** | Registro y seguimiento | Presentación fiscal, archivo, registro de retornos |

Para el detalle operativo de cada fase: `sdk/framework-5-fases.md`.

---

## Las cuatro cláusulas base

Ningún contrato instanciado desde este SDK es válido sin las cuatro:

1. **Interés 0%** — El tiempo no penaliza al receptor.
2. **Revalorización invertida** — La plusvalía del activo beneficia al receptor; el riesgo de mercado lo absorbe el prestamista.
3. **Condición-umbral de solvencia** — La obligación de devolución solo se activa si el receptor supera la insolvencia documentada.
4. **Devolución parcial en especie** — Módulo a módulo, sin calendario, sin penalización por discontinuidad.

Para la justificación de cada cláusula: `sdk/legal/clausulas-base.md`.

---

## Los cuatro escenarios de devolución

Una vez entregado el activo, cualquiera de estos desenlaces es legítimo y está previsto por el contrato:

| Escenario | Qué pasa |
|-----------|----------|
| **A: Intacto** | El receptor conserva el activo. El umbral no se supera. Préstamo en suspenso indefinido. |
| **B: Gradual** | El receptor devuelve módulo a módulo según puede, al valor nominal del préstamo. |
| **C: Liquidación** | El receptor vende módulos para necesidades vitales. El activo desaparece. No hay devolución. |
| **D: Rebote** | El receptor usa módulos como capital semilla, prospera, activa la devolución. |

Para el desarrollo de cada escenario: `sdk/escenarios.md`.

---

## Los tres roles

Cada préstamo instanciado desde el SDK tiene tres agentes activos:

- **Proveedor** — Artesano, fabricante, o productor que crea el activo con materiales de cadena ética. Tercero comercial: factura, tributa, no es parte del contrato de préstamo.
- **Prestamista** — Motor del circuito. Financia, coordina, formaliza ante la administración tributaria. Asume el riesgo del activo.
- **Receptor** — Portador del activo. Cuatro opciones legítimas de uso. Su agencia es el objeto del préstamo.

Para las plantillas de cuadernillo de cada rol: `sdk/roles/`.

---

## Cómo crear un mod

Un mod es una instanciación del SDK para un activo, jurisdicción, y circunstancia específicos. Reside en su propia rama (`mods/{nombre-mod}`) y añade un directorio `mod-{nombre}/` encima de la base del SDK.

**Pasos:**

1. **Crear rama** desde `main`: `git checkout -b mods/{nombre-mod}`
2. **Copiar y completar** `sdk/config.template.md` → `mod-{nombre}/proyecto.config.md`, rellenando todos los `{{PLACEHOLDERS}}`
3. **Instanciar las plantillas de roles** (`sdk/roles/`) para el activo concreto → `mod-{nombre}/roles/`
4. **Crear las 5 bitácoras** a partir de `sdk/plantillas/bitacora-fase.template.md` → `mod-{nombre}/bitacoras/bitacora-fase-{1-5}.md`
5. **Completar contrato y anexo técnico** (`sdk/plantillas/`) con los valores concretos
6. **Crear referencia de cadena ética** del activo específico → `mod-{nombre}/cadena-etica/`
7. **Escribir el README del mod** → `mod-{nombre}/README.md`, documentando los dos ejes, los entregables, y cómo este activo instancia el SDK

**Estructura de la rama `mods/{nombre-mod}`:**

```
README.md         ← Portada SDK (este fichero, sin cambios)
sdk/              ← Base SDK (sin cambios)
mod-{nombre}/
  README.md       ← Portada del mod
  proyecto.config.md
  cadena-etica/   ← Referencia de certificación para el activo del mod
  roles/          ← Cuadernillos instanciados para las partes concretas
  bitacoras/      ← 5 bitácoras con los nombres y checkpoints del mod
  fuente/         ← Material fuente del mod (sesiones, notas de origen)
  output/         ← Piezas literarias o documentales derivadas
```

**Merge de actualizaciones del SDK:** Las mejoras al SDK en `main` se incorporan al mod mediante `git merge main`. Los ficheros de `mod-{nombre}/` son exclusivos de la rama y no generan conflictos.

---

## Mods disponibles

| Rama | Activo | Estado |
|------|--------|--------|
| `mods/oro` | Oro ecoresponsable (Fairmined/Fairtrade) | Activo — ver `mod-oro/README.md` |

---

## Referencia de cadena ética

El activo de cualquier mod debe cumplir cuatro criterios de cadena ética: trazabilidad del origen, trabajo digno en el nodo artesanal, impacto positivo documentado en los productores primarios, e impacto ambiental mínimo verificable.

Para los criterios detallados: `sdk/cadena-etica/criterios.md`.
Para las certificaciones por tipo de activo (Fairmined, FSC, GOTS, Fairtrade, RJC): `sdk/cadena-etica/certificaciones-tipo.md`.

---

## Nota sobre el nombre del repositorio

El nombre `sdk-prestamos-eco-sostenibles-eco-fraternos` describe lo que la rama `main` contiene: el framework genérico. Los mods — cada instanciación concreta — residen en sus propias ramas y añaden lo específico sin modificar la base. El activo que inspiró el SDK es el oro ecoresponsable (`mods/oro`); el concepto que lo generó es el que subyace a cualquier economía que necesite, al mismo tiempo, activar cadenas de producción éticas y ofrecer suelo económico a quienes están por debajo del umbral de solvencia.
