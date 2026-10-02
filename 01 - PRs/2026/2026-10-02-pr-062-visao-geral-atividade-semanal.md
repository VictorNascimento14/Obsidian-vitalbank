---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 62
url: https://github.com/VictorNascimento14/Vitalbank/pull/62
branch: feat/visao-geral-atividade-semanal
tags: [pr, visao-geral, graficos]
status: aberto
---

# PR #62 — feat(visao-geral): bloco Atividade semanal

## 🎯 Contexto

Visão geral, item 3. Usa [[2026-10-02-pr-060-grafico-de-barras]]. Fecha a issue #61.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/atividade.ts, dados.test.ts}`.
- `src/telas/visao-geral/AtividadeSemanal.tsx` + teste.
- `src/app/(painel)/page.tsx`.

## 🧠 Decisões técnicas

- **"Entradas/Saídas"** em vez de "Depósito/Saque" do kit: são os termos do resto do app (transação com sinal).
- **O rótulo do dia sai da data** (`diaDaSemanaCurto`), não de texto fixo na semente: quando o dado for real, a semana anda sozinha.

## 🧪 Como testar

1. Captura do bloco (1440 px) e teste da tabela.

## 📎 Documentação afetada

- [[VisaoGeral]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
