---
tipo: aprendizado
data: 2026-10-02
contexto: celular, Visão geral e Transações
tags: [aprendizado, css, grid, responsivo]
---

# Grade sem `minmax(0, …)` alarga a página por causa de rolagem interna

Uma `div.grid` sem `grid-template-columns` tem **uma coluna implícita `auto`**. O tamanho mínimo de `auto`
é o conteúdo mínimo dos itens — e isso inclui um filho com `overflow-x: auto`: a fila de cartões rola por
dentro, mas o mínimo dela continua sendo a soma dos cartões.

Resultado: em 375 px a coluna ficava com ~560 px e a página inteira rolava para o lado.

**Regra:** grade de página declara a coluna desde o celular — `grid-cols-1`, que no Tailwind é
`repeat(1, minmax(0, 1fr))`. Para conferir: `document.documentElement.scrollWidth === innerWidth`.

Achado em [[2026-10-02-pr-084-fix-estouro-horizontal]].
