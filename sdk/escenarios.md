# Los cuatro escenarios de devolución

> Documento de referencia del SDK. Describe los cuatro desenlaces posibles
> de un préstamo eco-fraterno una vez que el {{ACTIVO}} ha sido entregado
> al receptor. Los cuatro son legítimos. El contrato los prevé todos.
> El prestamista los acepta todos antes de firmar.

---

## Por qué el contrato prevé todos los escenarios antes de que ocurran

La diferencia entre un préstamo fraterno y un préstamo bancario no es el interés: es la actitud ante el futuro. Un banco presta lo que espera recuperar; calcula el riesgo y lo carga en el tipo de interés, de modo que si el prestatario no paga, el banco ya habrá cobrado antes por esa eventualidad. Un prestamista fraterno presta lo que está dispuesto a no recuperar — y esa disposición tiene que estar en el contrato desde el principio, porque si no está, el contrato no es un contrato fraterno sino un contrato bancario sin intereses, que es una generosidad pero no es lo mismo.

Los cuatro escenarios que siguen no son contisngencias a gestionar: son posibilidades igualmente válidas que el contrato reconoce y ampara. Cuando el prestamista firma, no está apostando por el escenario D (el mejor) ni temiendo el escenario C (el que parece una pérdida): está aceptando que cualquiera de los cuatro es un resultado correcto del proceso.

---

## Escenario A: Intacto

**Qué pasa:** El receptor conserva el {{ACTIVO}} completo. No lo vende, no lo devuelve, no lo transforma. Su situación económica no supera el umbral de solvencia pactado en el contrato. El préstamo queda en suspenso indefinido.

**Qué significa esto:** De facto, el {{ACTIVO}} es del receptor para siempre. El contrato sigue siendo técnicamente un préstamo — porque el prestamista no lo ha condonado formalmente —, pero la condición de devolución nunca se activa. Desde el punto de vista del receptor, el {{ACTIVO}} funciona como un patrimonio latente: no lo gasta, pero lo tiene.

**Lo que el prestamista acepta:** Que el {{ACTIVO}} no regrese. Que la inversión haya producido algo diferente a un retorno económico: la tranquilidad del receptor de saber que tiene algo detrás suyo, por pequeño que sea.

**Lo que el receptor tiene:** Un {{ACTIVO}} que no le cuesta nada conservar, que se revaloriza o deprecia según el mercado, y que en ningún momento genera presión de devolución porque el contrato establece que la obligación no existe mientras la situación económica esté por debajo del umbral.

---

## Escenario B: Devolución gradual

**Qué pasa:** El receptor supera progresivamente el umbral de solvencia — o lo transita intermitentemente — y va devolviendo partes del {{ACTIVO}} cuando puede. Devolución a devolución, sin calendario prefijado, al valor nominal del momento del préstamo según lo establece la cláusula de revalorización invertida.

**Qué significa esto:** El circuito cierra de modo limpio y simétrico. Cada devolución se registra en el registro de retornos (bitácora Fase 5) con firma de ambas partes. Si el receptor vuelve a caer por debajo del umbral entre devoluciones, el préstamo se vuelve a suspender y se reanuda cuando proceda.

**Lo que el prestamista acepta:** Que el horizonte de la devolución es indefinido, que puede durar años, y que no puede exigir aceleración.

**Lo que el receptor tiene:** Un mecanismo de devolución que respeta sus tiempos y no lo penaliza por ser discontinuo.

---

## Escenario C: Liquidación corriente

**Qué pasa:** El receptor vende partes del {{ACTIVO}} para cubrir necesidades vitales inmediatas — alquiler, alimentación, deuda urgente, gasto médico. El {{ACTIVO}} se adelgaza o desaparece por completo. El dinero se gasta. El préstamo no se devuelve.

**Qué significa esto:** El {{ACTIVO}} ha cumplido su función primordial: convertirse en liquidez cuando la necesidad lo exigió. Esto no es un fracaso del préstamo: es el escenario para el que el préstamo fraterno existe. Si el {{ACTIVO}} no pudiera convertirse en liquidez en el momento de necesidad, no sería suelo económico; sería un adorno.

**Lo que el prestamista acepta:** La pérdida total del {{ACTIVO}}. El préstamo no se devuelve. Eso estaba previsto.

**Lo que el receptor tiene:** La libertad de actuar sobre el {{ACTIVO}} sin pedir permiso, sin explicaciones, y sin consecuencias legales o relacionales más allá de lo que el contrato establece — que en este escenario, si el receptor no supera el umbral, es ninguna.

> **Nota sobre las implicaciones fiscales del receptor:** Si el receptor vende el {{ACTIVO}} a precio superior al valor nominal del préstamo, puede existir una ganancia patrimonial sujeta a declaración. El cuadernillo del receptor (ver `roles/receptor.template.md`) debe detallar esto para la jurisdicción del mod.

---

## Escenario D: Rebote e inversión

**Qué pasa:** El receptor usa partes del {{ACTIVO}} como capital semilla — lo vende, invierte el producto en medios de producción, actividad laboral, formación, o cualquier otra forma de generación de renta — y logra estabilizarse por encima del umbral de solvencia. En ese momento, se activa la cláusula de devolución del contrato y el receptor comienza a devolver según su capacidad (escenario B, a partir de ese punto).

**Qué significa esto:** El préstamo ha funcionado como la infraestructura de agencia que pretendía ser. El {{ACTIVO}} no era solo una reserva de valor: era capital semilla que el receptor usó como herramienta de salida de la insolvencia.

**Lo que el prestamista acepta:** Que el {{ACTIVO}} fue transformado en otra cosa, que ese proceso era válido, y que la devolución que llega es consecuencia de haberlo catalizado.

**Lo que el receptor tiene:** La posibilidad de usar el préstamo como infraestructura activa, no pasiva. La agencia de decidir cuándo actuar y en qué dirección.

---

## La tabla de los cuatro

| Escenario | El {{ACTIVO}}... | El préstamo... | El receptor... |
|-----------|----------------|----------------|----------------|
| **A: Intacto** | se conserva | queda en suspenso | tiene reserva latente |
| **B: Gradual** | se devuelve por partes | se salda progresivamente | supera el umbral e inicia retornos |
| **C: Liquidación** | se gasta por necesidad | no se devuelve | tiene oxígeno financiero |
| **D: Rebote** | se invierte como capital | se activa tras el rebote | sale de la insolvencia |

Los cuatro son previstos por el contrato. Los cuatro son correctos. El quinto escenario — el que no estaba previsto — es el único que el SDK no puede manejar: el que ocurre cuando el contrato no existe o cuando alguna cláusula se omitió.

---

*Este documento es la referencia conceptual. Para las cláusulas que habilitan estos escenarios, ver `legal/clausulas-base.md`. Para el registro de devoluciones en escenarios B y D, ver `plantillas/registro-devoluciones.template.md`.*
