---
tipo: aprendizado
data: 2026-10-02
contexto: formatarMoeda compacto
tags: [aprendizado, intl, dinheiro]
---

# O Intl compacto de moeda deixa um ",0" sobrando

`new Intl.NumberFormat("pt-BR", { style: "currency", currency: "BRL", notation: "compact", maximumFractionDigits: 1 })`
formata 150000 como **"R$ 150,0 mil"**: a moeda traz `minimumFractionDigits` próprio, e o `maximum` sozinho não o derruba.

**Correção:** declarar `minimumFractionDigits: 0` junto. Aí sai "R$ 150 mil" e "R$ 1,2 mil".

Achado em [[2026-10-02-pr-012-dinheiro]]. Ver [[Dinheiro]].
