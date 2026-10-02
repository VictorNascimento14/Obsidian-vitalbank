---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 76
url: https://github.com/VictorNascimento14/Vitalbank/pull/76
branch: refactor/meus-cartoes-compartilhado
tags: [pr, refactor, cartao]
status: merged
---

# PR #76 — refactor(telas): Meus cartões compartilhado entre telas, com ação configurável

## 🎯 Contexto

Preparação da tela de Transações. Fecha a issue #75.

## 🔧 Mudanças

- `src/telas/comum/MeusCartoes.tsx` (movido) + teste; `src/app/(painel)/page.tsx`.

## 🧠 Decisões técnicas

- **`src/telas/comum/`** para bloco usado por 2+ telas — espelha `Componentes/Comuns/` do cofre.
- **`acao` obrigatória**: cada tela decide explicitamente o que oferecer ao lado do título.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[VisaoGeral]]
- [[2026]] (changelog)
