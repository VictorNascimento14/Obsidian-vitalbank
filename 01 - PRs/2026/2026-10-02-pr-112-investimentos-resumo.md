---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 112
url: https://github.com/VictorNascimento14/Vitalbank/pull/112
branch: feat/investimentos-resumo
tags: [pr, investimentos]
status: merged
---

# PR #112 — feat(investimentos): resumo com total investido, aplicações e retorno

## 🎯 Contexto

Investimentos, item 1. Fecha a issue #111. Foi montando este bloco que apareceu o bug de [[2026-10-02-pr-110-formatar-numero-no-dominio]].

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/investimentos.ts}`; `src/telas/investimentos/ResumoDosInvestimentos.tsx` + teste; `src/app/(painel)/investimentos/page.tsx`.

## 🧠 Decisões técnicas

- **Retorno em pontos-base** (inteiro), como dinheiro em centavos: 5,80% é `580`.
- **Retorno como texto** (não conta): número com sinal e vírgula contando de 0 a 5,8 é ruído.

## 🧪 Como testar

1. Captura (1440 px).

## 📎 Documentação afetada

- [[Investimentos]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
