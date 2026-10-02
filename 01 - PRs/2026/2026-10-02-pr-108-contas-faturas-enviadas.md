---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 108
url: https://github.com/VictorNascimento14/Vitalbank/pull/108
branch: feat/contas-faturas-enviadas
tags: [pr, contas]
status: aberto
---

# PR #108 — feat(contas): Faturas enviadas com tempo relativo

## 🎯 Contexto

Contas, item 5 — fecha a tela. Fecha a issue #107.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/faturas.ts}`; `src/telas/contas/FaturasEnviadas.tsx` + teste; `src/app/(painel)/contas/page.tsx`.

## 🧠 Decisões técnicas

- **`hoje` por prop (opcional)**: o teste fixa a data; a tela usa a do relógio.

## ⚠️ Armadilhas e aprendizados

- `Intl.RelativeTimeFormat("pt-BR", { numeric: "auto" })` diz **"anteontem"** para −2 dias (não "há 2 dias"). Português correto, e o teste foi corrigido para isso.

## 🧪 Como testar

1. Captura da tela inteira.

## 📎 Documentação afetada

- [[Contas]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
