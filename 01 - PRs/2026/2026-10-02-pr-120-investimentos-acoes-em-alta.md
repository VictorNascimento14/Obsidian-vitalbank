---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 120
url: https://github.com/VictorNascimento14/Vitalbank/pull/120
branch: feat/investimentos-acoes-em-alta
tags: [pr, investimentos, tabela]
status: merged
---

# PR #120 — feat(investimentos): tabela de ações em alta

## 🎯 Contexto

Investimentos, item 5 — fecha a tela. Fecha a issue #119.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/investimentos.ts}`; `src/telas/investimentos/AcoesEmAlta.tsx` + teste; `src/app/(painel)/investimentos/page.tsx`.

## 🧠 Decisões técnicas

- **Nome como `<th scope="row">`**: o leitor de tela anuncia "Trívia" ao percorrer preço e variação da linha.
- **`retornoComSinal`** reaproveitado de Meus investimentos: o mesmo formato de variação nos dois blocos.

## 🧪 Como testar

1. Captura da tela inteira.

## 📎 Documentação afetada

- [[Investimentos]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
