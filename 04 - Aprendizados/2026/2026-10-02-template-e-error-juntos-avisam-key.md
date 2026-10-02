---
tipo: aprendizado
data: 2026-10-02
contexto: casca do painel, Next 16
tags: [aprendizado, nextjs]
---

# `template.tsx` + `error.tsx` no mesmo segmento: aviso de key no Next 16

Em desenvolvimento, com os dois arquivos em `src/app/(painel)/`, toda página logava:

> Each child in a list should have a unique "key" prop. Check the render method of `OuterLayoutRouter`.

Bisseção (duas medições cada, console lido pelo Playwright):

| Arquivos no segmento | Avisos |
|---|---|
| template + error + loading | 1 |
| sem template | 0 |
| sem error | 0 |
| sem loading | 1 |

**Contorno:** a animação de entrada que o template fazia virou um `motion.div` com `key={usePathname()}`
dentro da casca. Mesmo efeito, e o `error.tsx` fica.

Achado em [[2026-10-02-pr-192-fix-transicao-sem-template]].
