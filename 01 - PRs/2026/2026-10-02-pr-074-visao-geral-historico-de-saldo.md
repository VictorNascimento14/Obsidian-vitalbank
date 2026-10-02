---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 74
url: https://github.com/VictorNascimento14/Vitalbank/pull/74
branch: feat/visao-geral-historico-de-saldo
tags: [pr, visao-geral, graficos]
status: aberto
---

# PR #74 — feat(visao-geral): bloco Histórico de saldo

## 🎯 Contexto

Visão geral, item 6 — fecha a tela. Usa [[2026-10-02-pr-072-grafico-de-linha]]. Fecha a issue #73.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/saldo.ts}`; `src/telas/visao-geral/HistoricoDeSaldo.tsx` + teste; `src/app/(painel)/page.tsx`.

## 🧠 Decisões técnicas

- **Mês como `AAAA-MM-01`** na semente e rótulo por `mesCurto`: o eixo segue a data, não um texto fixo.
- **`primaria-viva`** (`#2D60FF`) como no kit: a área do saldo é um azul mais claro que o das barras.

## 🧪 Como testar

1. Captura (1440 px) da última linha da grade.

## 📎 Documentação afetada

- [[VisaoGeral]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
