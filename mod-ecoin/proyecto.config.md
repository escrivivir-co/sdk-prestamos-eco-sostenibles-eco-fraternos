# Configuración del mod: ECOin — préstamo fraterno en moneda de economía solar

> Préstamo al 0 % de criptomoneda ECOin (SCRYPT, POW+POS+POT, ~225M supply)
> sobre la red distribuida Oasis de SolarNET.HuB. El activo no es materia
> sino energía social cristalizada en un ledger borrable.
>
> Basado en `sdk/config.template.md`.

---

## Identidad

```yaml
extends: "sdk/config.template.md"
nombre: "ECOin — préstamo fraterno en moneda de economía solar"
mod: "ecoin"
sdk-base: "main"
descripcion: |
  Instanciación del SDK de préstamos eco-sostenibles y eco-fraternos
  para el activo ECOin, la criptomoneda solarpunk del proyecto
  SolarNET.HuB (SNH).
  
  Activo: ECOin (ECO) — criptomoneda SCRYPT con triple minado (POW/POS/POT)
  Proveedor: Nodo SNH — operador de SNH-KIT alimentado con energía solar
  Receptor: Wallet Oasis — persona dentro de la red social distribuida Oasis
  Certificación: Código fuente GPLv3 + blockchain explorer público
  
  Dos ejes (heredados del SDK):
  (a) Eco-sostenible: la cadena ética es energética (solar) y computacional
      (hardware libre, software libre, red federada). Cada ECO trazable
      desde el bloque de minado hasta la transacción de préstamo.
  (b) Eco-fraterno: el préstamo de ECO entrega suelo digital dentro de un
      ecosistema con UBI, marketplace, gobernanza y justicia distribuida.
      El receptor opera dentro de la red, no necesita volver al circuito fiat.
      Escenario límite: la moneda es borrable (el ledger puede disolverse).
  
  Tres entregables: (1) contrato civil + smart-contract Oasis,
  (2) documentación on-chain (hashes, block explorer), (3) cuadernillos.
  
  Operativamente, 5 fases según el framework del SDK.
  4 escenarios de devolución: (A) conservar + staking, (B) devolución gradual
  vía transfers, (C) liquidación en marketplace Oasis, (D) inversión y rebote.
  
  Cláusula clave: interés 0% con revalorización invertida (heredada del SDK).
  
  Portada y relato operativo: mod-ecoin/README.md
idioma: "es"
fecha_inicio: "2026-04"
jurisdiccion: "Variable — el préstamo civil se formaliza según la jurisdicción del prestamista. La operación on-chain es transjurisdiccional."
origen: |
  ECOin nace en 2014 como proyecto de criptomoneda solarpunk. Mencionado
  en Mr Robot (2015). Integrado en SolarNET.HuB (2024). Desplegado como
  paquete para Android y AMD64 (2026). Oasis opera con IA, gobierno,
  justicia y UBI. El mod-ecoin conecta el circuito fraterno de Oasis
  con el marco legal civil del SDK.
```

---

## La Voz (configuración del protagonista)

```yaml
nombre: "Consejo Asesor del mod-ecoin"
posicion: "Dentro de la red, mirando hacia fuera"
biografia: |
  Colectivo de personas familiarizadas con el ecosistema SolarNET.HuB,
  la economía de ECOin, y los mecanismos de gobernanza de Oasis.
  Nescientes en derecho tributario convencional (como el equipo de
  escrivivir.co en el mod oro), pero duchos en los protocolos de
  la red distribuida. La tensión es la inversa: saben de tecnología
  alternativa pero deben aprender a formalizar ante el Estado.
ejes:
  - nombre: "Soberanía digital"
    posicion: "La infraestructura debe ser libre, solar, y borrable"
    expresion: "Your data. Our future."
  - nombre: "Suelo fraterno distribuido"
    posicion: "El préstamo es una función de la red, no del banco"
    expresion: "We are not the emergency architects, because the emergency was always there…"
influencias:
  - categoria: "Tecnología"
    nombres: ["SolarNET.HuB", "epsylon/ecoin (GPLv3)"]
  - categoria: "Economía"
    nombres: ["Renta básica universal", "Economía P2P"]
  - categoria: "Filosofía"
    nombres: ["Anarquismo hacker", "Solarpunk"]
  - categoria: "Ficción"
    nombres: ["Mr Robot (ecoin / fsociety)", "L.A.R.P de Oasis"]
paradojas: |
  El préstamo al 0 % en el mundo fiat necesita un contrato civil que
  lo haga visible ante Hacienda. Pero ECOin vive en una red diseñada
  precisamente para ser invisible a Hacienda. El mod-ecoin formaliza
  con un pie en cada mundo: contrato civil para la jurisdicción local,
  smart-contract para la red distribuida. La paradoja: para que el
  préstamo fraterno sea legalmente válido hay que sacarlo parcialmente
  del territorio de soberanía digital donde vive.
puntos-ciegos:
  - "Fiscalidad de criptomonedas: régimen en evolución, varía por jurisdicción"
  - "Volatilidad del ECO frente a moneda fiat: la revalorización invertida aplica pero el valor de referencia es inestable"
  - "Borrado del ledger: escenario filosófico, pero técnicamente posible — ¿qué pasa con la deuda si la moneda deja de existir?"
```

---

## Antagonistas

### El racionalista fiscal

```yaml
modelo: "Inspector de Hacienda con competencia en criptoactivos"
desafio-central: "ECOin no tiene curso legal — ¿cómo se declara un préstamo de algo que no es dinero oficial?"
tensiones:
  - tema: "Base imponible"
    la-voz-dice: "ECOin tiene un valor de mercado rastreable en su blockchain. El préstamo se autodeclara al valor fiat del momento de la transferencia."
    el-antagonista-responde: "El valor de una criptomoneda sin listing en exchanges estándar es indemostrable. Hacienda podría impugnar la valoración."
  - tema: "Donación encubierta"
    la-voz-dice: "Hay contrato civil con las 4 cláusulas. Hay hash verificable. Hay blockchain explorer. No es una donación: es un préstamo condicional con trazabilidad superior a la del efectivo."
    el-antagonista-responde: "Un préstamo al 0 % en algo que no tiene valor oficial sigue pareciendo una donación. El ISD podría aplicar."
```

### El escéptico relacional

```yaml
modelo: "Receptor que desconfía de la promesa tecnológica"
desafio-central: "¿De qué me sirven unos tokens si no puedo comprar pan con ellos?"
tensiones:
  - tema: "Utilidad real"
    la-voz-dice: "ECOin opera dentro de Oasis: marketplace de bienes y servicios, intercambio P2P, proyectos de crowdfunding. No es un token vacío: es una moneda de una economía con gobierno, justicia, y renta básica."
    el-antagonista-responde: "Esa economía tiene cientos de usuarios, no millones. La liquidez es micro. No puedes pagar el alquiler con ECO."
```

### El maximalista cripto

```yaml
modelo: "Holder de BTC/ETH que mira ECOin como un juguete"
desafio-central: "225 millones de supply, SCRYPT, sin listing — esto no escala."
tensiones:
  - tema: "Escala"
    la-voz-dice: "El SDK no busca escala: busca formalizar préstamos fraternos en una economía que ya existe. Si la red crece, el mod escala con ella. Si no crece, el préstamo sigue siendo válido entre sus participantes."
    el-antagonista-responde: "Una moneda que puede borrarse no es reserva de valor."
```

---

## Corpus

```yaml
descripcion: "Documentación completa del mod-ecoin: préstamo fraterno en ECOin"
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
  - ruta: "mod-ecoin/README.md"
    nombre: "Portada y relato operativo del mod"
    descripcion: "Circuito ECOin, doble eje instanciado, 5 fases, 4 escenarios, índice de ficheros"
  - ruta: "mod-ecoin/cadena-etica/ecoin-cadena-energetica.md"
    nombre: "Cadena ética: energía solar + software libre"
    descripcion: "Los 4 criterios del SDK aplicados a la cadena energética/computacional de ECOin"
  - ruta: "mod-ecoin/roles/cuadernillo-nodo-snh.md"
    nombre: "Cuadernillo del proveedor (nodo SNH)"
    descripcion: "Guía para el operador del SNH-KIT que mina y provee ECO"
  - ruta: "mod-ecoin/roles/cuadernillo-prestamista.md"
    nombre: "Cuadernillo del prestamista"
    descripcion: "Guía para quien posee ECO y formaliza el préstamo"
  - ruta: "mod-ecoin/roles/cuaderno-receptor.md"
    nombre: "Cuadernillo del receptor"
    descripcion: "Guía para quien recibe ECO en su wallet Oasis"
  - ruta: "mod-ecoin/bitacoras/"
    nombre: "Bitácoras de las 5 fases"
    descripcion: "Registros operativos de cada fase"
  - ruta: "mod-ecoin/fuente/"
    nombre: "Material fuente del mod"
    descripcion: "Timeline SNH, documentación de referencia, capturas de blockchain"
output:
  ruta: "mod-ecoin/output/"
  convencion: "{tipo}_{fecha}_{tema}.md"
```

---

## Vocabulario

### Términos del SDK (heredados — no modificar)

```yaml
terminos-sdk:
  - termino: "Eco-sostenible"
    definicion: "Eje del préstamo: ECOin como moneda de cadena ética energética (solar, hardware libre, software libre). La riqueza circula por infraestructura documentada y verificable."
  - termino: "Eco-fraterno"
    definicion: "Eje del préstamo: ECOin como suelo digital dentro de la red Oasis — marketplace, UBI, gobernanza. El receptor opera sin depender del circuito fiat."
  - termino: "Cota-umbral-de-solvencia"
    definicion: "Capacidad de operación autónoma del receptor dentro de la red Oasis. No se mide solo en fiat: se mide en agencia dentro del ecosistema distribuido."
  - termino: "Préstamo a fondo perdido"
    definicion: "Préstamo a interés 0% condicionado a recuperación. El prestamista acepta que si el receptor no desarrolla autonomía en la red, la deuda no se activa."
  - termino: "Revalorización invertida"
    definicion: "Si ECO sube de valor respecto a fiat, se devuelve al valor nominal del préstamo. La plusvalía es del receptor."
```

### Términos específicos del mod

```yaml
terminos-mod:
  - termino: "ECOin (ECO)"
    definicion: "Criptomoneda SCRYPT con triple minado (POW/POS/POT). Supply estimado ~225M ECO. Código fuente GPLv3. Integrada en SNH-OS y Oasis."
  - termino: "SNH-KIT"
    definicion: "Kit de hardware libre solar de SolarNET.HuB. Incluye wallet ECOin, eMiner, y acceso a la red Oasis. Carcasa DIY imprimible en 3D."
  - termino: "Oasis"
    definicion: "Red social distribuida, cifrada y federada de SolarNET.HuB. Módulos: Wallet, Market, Transfers, UBI, Parliament, Courts, Tribes, Projects, entre otros."
  - termino: "UBI (Universal Basic Income)"
    definicion: "Asignación semanal de ECOin dentro de Oasis, basada en participación y buen uso de la herramienta. Renta básica universal de la red."
  - termino: "Transfer"
    definicion: "Smart-contract de Oasis para transferencia de ECOin entre wallets. Funciona como el mecanismo de ejecución del préstamo y de las devoluciones."
  - termino: "eMiner"
    definicion: "Aplicación de minado incluida en SNH-KIT. Permite generar ECO usando energía solar."
  - termino: "Borrado del ledger"
    definicion: "Posibilidad técnica y filosófica de ECOin: al no tener soporte material, destruir los nodos anula toda la deuda acumulada. Escenario límite del eje eco-fraterno."
  - termino: "42"
    definicion: "IA integrada en Oasis (desde v.0.3.7). LLM accesible como módulo de la red."
```

---

## Estilo

```yaml
estilo:
  escritura: |
    Mismo registro ensayístico del SDK. Oraciones subordinadas extensas
    que no separan lo técnico de lo filosófico. La blockchain no se explica
    como un manual: se narra como el entramado que es, con sus nudos y
    sus grietas. La voz del lore de escrivivir.co (Animus Iocandi) opera
    incluso en territorio anarco-hacker. El humor es seco y la ironía,
    estructural.
  prohibiciones:
    - Separar "lo técnico" de "lo político" — en ECOin son lo mismo
    - Bullet-points como estructura principal de un documento
    - Jerga cripto-bro sin contexto (no "HODL", no "to the moon")
    - Promesas de revalorización — esto es un préstamo fraterno, no una inversión
```

---

## Invocación

```
@{agente} MOD-ECOIN {tema}
```
