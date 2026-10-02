---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 68
url: https://github.com/VictorNascimento14/Vitalbank/pull/68
branch: feat/visao-geral-estatistica-de-despesas
tags: [pr, visao-geral, graficos]
status: merged
---

# PR #68 — feat(visao-geral): bloco Estatística de despesas

## 🎯 Contexto

Visão geral, item 4. Usa [[2026-10-02-pr-066-grafico-de-pizza]]. Fecha a issue #67.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/despesas.ts}`; `src/telas/visao-geral/EstatisticaDeDespesas.tsx` + teste; `src/app/(painel)/page.tsx`; `src/app/globals.css`.

## 🧠 Decisões técnicas

- **A semente traz totais em centavos**, não percentuais: o percentual é conta da tela, e o dia em que vier do backend, vem como valor.
- **Cor e raio por posição** (tabela `ESTILO`): o kit desenha cada fatia com um raio, e a maior fatia (Outros, 35%) não é a mais longa.
- **Dois tokens novos** em vez de reaproveitar `rosa`/`laranja`: a pizza do kit usa tons mais saturados, e trocar mudaria a cara do gráfico.

## 🧪 Como testar

1. Captura do bloco.

## 📎 Documentação afetada

- [[VisaoGeral]]
- [[linguagem-visual]]
- [[2026]] (changelog)
