---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 122
url: https://github.com/VictorNascimento14/Vitalbank/pull/122
branch: feat/cartoes-meus-cartoes
tags: [pr, cartoes]
status: aberto
---

# PR #122 — feat(cartoes): os três cartões no topo da tela de Cartões

## 🎯 Contexto

Cartões, item 1. Fecha a issue #121.

## 🔧 Mudanças

- `src/telas/comum/MeusCartoes.tsx` + teste; `src/app/(painel)/cartoes/page.tsx`.

## 🧠 Decisões técnicas

- **`acao` passa a ser opcional** (antes, em [[2026-10-02-pr-076-meus-cartoes-compartilhado]], era obrigatória): na própria tela de Cartões, "Ver todos" apontaria para ela mesma.

## 🧪 Como testar

1. Captura (1440 px) e largura sem estouro em 375 px.

## 📎 Documentação afetada

- [[CartoesDeCredito]]
- [[2026]] (changelog)
