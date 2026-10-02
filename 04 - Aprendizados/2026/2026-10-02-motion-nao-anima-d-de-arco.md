---
tipo: aprendizado
data: 2026-10-02
contexto: GraficoDeRosca
tags: [aprendizado, svg, motion]
---

# O motion não anima o `d` de um arco SVG

`<motion.path animate={{ d }}>` interpola o caminho **número a número**. Num comando de arco
(`A rx,ry rot grande varredura x,y`), `grande` e `varredura` são **flags** — só 0 ou 1. No meio da
animação viram 0,0887…, e o navegador recusa o caminho inteiro:

> Error: <path> attribute d: Expected arc flag ('0' or '1')

E se o `d` inicial não existe, ele parte de zeros.

**Regra:** para destacar um arco, anime `transform` (`scale` com origem no centro) e deixe o `d` fixo.
Animação de forma de verdade (morph) só entre caminhos sem arcos, ou com a mesma estrutura e flags.

Achado em [[2026-10-02-pr-124-grafico-de-rosca]].
