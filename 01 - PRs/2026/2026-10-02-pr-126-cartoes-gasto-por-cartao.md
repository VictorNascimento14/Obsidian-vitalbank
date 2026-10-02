---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 126
url: https://github.com/VictorNascimento14/Vitalbank/pull/126
branch: feat/cartoes-gasto-por-cartao
tags: [pr, cartoes, graficos]
status: aberto
---

# PR #126 — feat(cartoes): Gasto por cartão calculado das transações

## 🎯 Contexto

Cartões, item 2. Usa [[2026-10-02-pr-124-grafico-de-rosca]]. Fecha a issue #125.

## 🔧 Mudanças

- `src/telas/cartoes/GastoPorCartao.tsx` + teste; `src/app/(painel)/cartoes/page.tsx`.

## 🧠 Decisões técnicas

- **Derivado, não semeado**: soma de `valor < 0` por `cartao`. Com backend, vira uma consulta agregada; a tela continua igual.
- **Legenda pelo final do cartão**, não pelo banco (o kit inventa bancos; aqui todos são Vitalbank).

## 🧪 Como testar

1. Captura (1440 px).

## 📎 Documentação afetada

- [[CartoesDeCredito]]
- [[2026]] (changelog)
