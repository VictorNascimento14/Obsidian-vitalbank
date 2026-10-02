---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 46
url: https://github.com/VictorNascimento14/Vitalbank/pull/46
branch: ui/layout-do-painel
tags: [pr, design, casca, navegacao, animacao, acessibilidade]
status: aberto
---

# PR #46 — ui(casca): layout do painel com coluna fixa e gaveta no celular

## 🎯 Contexto

Casca, item 4. Fecha a issue #45.

## 🔧 Mudanças

- `src/ui/casca/{Casca,EmBreve}.tsx`; exportados em `@/ui`.
- `src/app/(painel)/layout.tsx`, `(painel)/page.tsx` (+ teste) e as 8 páginas provisórias.
- `src/ui/casca/{navegacao.ts, ColunaLateral.tsx}` — rótulo "Cartões" e item sem quebra.

## 🧠 Decisões técnicas

- **Grupo de rotas `(painel)`** em vez de pôr a casca no layout raiz: telas sem casca (404, futura tela de entrada) ficam fora sem condicional.
- **Gaveta como `role="dialog"` + `aria-modal`**, com Esc, foco inicial e retorno de foco. Sem armadilha de foco completa: a gaveta só tem links, e o véu fecha ao clicar fora.
- **Breakpoint `lg` (1024 px)**: o kit desenha a coluna visível no tablet de 1024.
- **O véu e a gaveta são `fixed` fora de qualquer bloco com `transform`**: dentro de um ancestral transformado, `fixed` passaria a medir o ancestral, não a tela.

## ⚠️ Armadilhas e aprendizados

- A captura da gaveta revelou o bug do gradiente da marca, corrigido antes em [[2026-10-02-pr-044-fix-gradiente-da-marca]].
- Rótulo em português é ~30% mais longo que o do kit: "Cartões de crédito" e "Meus privilégios" quebravam linha em 250 px.

## 🧪 Como testar

1. Capturas em 1440 px (`/cartoes`) e 375 px com a gaveta aberta (`/privilegios`): coluna sem quebra, marcador no item certo, símbolo completo.

## 📎 Documentação afetada

- [[Casca]]
- [[ColunaLateral]]
- [[2026]] (changelog)
