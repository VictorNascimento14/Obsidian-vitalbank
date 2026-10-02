---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 114
url: https://github.com/VictorNascimento14/Vitalbank/pull/114
branch: feat/investimentos-anual
tags: [pr, investimentos, graficos]
status: merged
---

# PR #114 — feat(investimentos): gráfico do investimento anual

## 🎯 Contexto

Investimentos, item 2. Reusa [[2026-10-02-pr-072-grafico-de-linha]]. Fecha a issue #113.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/investimentos.ts}`; `src/telas/investimentos/InvestimentoAnual.tsx` + teste; `src/app/(painel)/investimentos/page.tsx`.

## 🧠 Decisões técnicas

- **Segmentos retos**, como no kit: ano a ano são seis medidas isoladas; uma curva sugeriria valores no meio do ano que não existem.

## 🧪 Como testar

1. Captura (1440 px).

## 📎 Documentação afetada

- [[Investimentos]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
