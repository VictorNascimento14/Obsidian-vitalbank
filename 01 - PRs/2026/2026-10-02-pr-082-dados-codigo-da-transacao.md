---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 82
url: https://github.com/VictorNascimento14/Vitalbank/pull/82
branch: feat/dados-codigo-da-transacao
tags: [pr, dados, transacoes]
status: merged
---

# PR #82 — feat(dados): código de extrato nas transações e semente de dois meses

## 🎯 Contexto

Preparação da tabela de Transações. Fecha a issue #81.

## 🔧 Mudanças

- `src/dados/{tipos.ts, sementes/transacoes.ts, dados.test.ts}`.

## 🕵️ Dado sensível

O código é do extrato fictício, não de conta. 8 dígitos ficam longe da faixa de 13–19 que o teste de Luhn varre.

## 🧠 Decisões técnicas

- **Código como campo, não derivado do `id`**: no backend ele vem pronto do extrato, e a tela não deve saber como é gerado.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[CamadaDeDados]]
- [[2026]] (changelog)
