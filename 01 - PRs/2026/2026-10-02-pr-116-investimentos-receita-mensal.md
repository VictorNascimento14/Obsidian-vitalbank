---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 116
url: https://github.com/VictorNascimento14/Vitalbank/pull/116
branch: feat/investimentos-receita-mensal
tags: [pr, investimentos, graficos]
status: merged
---

# PR #116 — feat(investimentos): gráfico da receita mensal

## 🎯 Contexto

Investimentos, item 3. Fecha a issue #115.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/investimentos.ts}`; `src/telas/investimentos/ReceitaMensal.tsx` + teste; `src/app/(painel)/investimentos/page.tsx`.

## 🧠 Decisões técnicas

- **Curva monotônica** ([[2026-10-02-pr-058-graficos-escala]]): a receita de outubro (R$ 38,1 mil) é o topo e a curva não passa dele.
- **Dois degradês na mesma página**: a lição do id por instância já está no `GraficoDeLinha`.

## 🧪 Como testar

1. Captura (1440 px).

## 📎 Documentação afetada

- [[Investimentos]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
