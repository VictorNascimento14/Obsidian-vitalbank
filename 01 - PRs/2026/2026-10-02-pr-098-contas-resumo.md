---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 98
url: https://github.com/VictorNascimento14/Vitalbank/pull/98
branch: feat/contas-resumo
tags: [pr, contas]
status: aberto
---

# PR #98 — feat(contas): resumo com saldo, receitas, despesas e poupança

## 🎯 Contexto

Contas, item 1. Usa [[2026-10-02-pr-096-cartao-de-resumo]]. Fecha a issue #97.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/conta.ts}`; `src/telas/contas/ResumoDaConta.tsx` + teste; `src/app/(painel)/contas/page.tsx`.

## 🧠 Decisões técnicas

- **Resumo como objeto, não lista**: são quatro números com papéis fixos; a tela decide rótulo, cor e ícone.

## 🧪 Como testar

1. Capturas 1440 / 375 px.

## 📎 Documentação afetada

- [[Contas]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
