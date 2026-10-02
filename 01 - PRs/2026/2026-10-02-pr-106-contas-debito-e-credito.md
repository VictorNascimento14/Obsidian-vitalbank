---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 106
url: https://github.com/VictorNascimento14/Vitalbank/pull/106
branch: feat/contas-debito-e-credito
tags: [pr, contas, graficos]
status: merged
---

# PR #106 — feat(contas): Débito e crédito da semana, com o total de cada lado

## 🎯 Contexto

Contas, item 4. Reusa [[2026-10-02-pr-060-grafico-de-barras]]. Fecha a issue #105.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/debitoCredito.ts}`; `src/telas/contas/DebitoECredito.tsx` + teste; `src/app/(painel)/contas/page.tsx`.

## 🧠 Decisões técnicas

- **Total calculado na tela a partir dos dias**, não guardado na semente: a frase nunca discorda do gráfico.

## 🧪 Como testar

1. Captura (1440 px).

## 📎 Documentação afetada

- [[Contas]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
