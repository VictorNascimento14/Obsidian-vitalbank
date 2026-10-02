---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 40
url: https://github.com/VictorNascimento14/Vitalbank/pull/40
branch: ui/coluna-lateral
tags: [pr, design, casca, navegacao, animacao]
status: merged
---

# PR #40 — ui(casca): coluna lateral com o marcador deslizando até a tela aberta

## 🎯 Contexto

Casca, item 2. Fecha a issue #39.

## 🔧 Mudanças

- `src/ui/casca/{navegacao.ts, ColunaLateral.tsx}` + testes; exportados em `@/ui`.

## 🧠 Decisões técnicas

- **Rotas em português** (`/transacoes`, `/cartoes`…), como o resto da interface.
- **"Meus privilégios" entra no menu** porque está no kit, mesmo sem tela desenhada; a tela dela será pensada à parte.
- **A barra desliza com `layoutId`**, e funciona porque a coluna fica no layout (não remonta ao navegar). Se cada página montasse a própria coluna, não haveria "de onde" deslizar.
- **`itemAtivo` puro e testado** fora do componente: a regra "`/` só exato" é o tipo de coisa que quebra em silêncio.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[ColunaLateral]]
- [[2026]] (changelog)
