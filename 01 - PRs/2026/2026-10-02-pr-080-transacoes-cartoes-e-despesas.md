---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 80
url: https://github.com/VictorNascimento14/Vitalbank/pull/80
branch: feat/transacoes-cartoes-e-despesas
tags: [pr, transacoes, graficos]
status: merged
---

# PR #80 — feat(transacoes): Meus cartões e Minhas despesas no topo da tela

## 🎯 Contexto

Transações, item 1. Usa [[2026-10-02-pr-076-meus-cartoes-compartilhado]] e [[2026-10-02-pr-078-grafico-de-colunas]]. Fecha a issue #79.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/despesasMensais.ts}`; `src/telas/transacoes/MinhasDespesas.tsx` + teste; `src/app/(painel)/transacoes/page.tsx`.

## 🧠 Decisões técnicas

- **Destaque no mês de maior gasto**, não no mês atual: o kit destaca o pico ("Dec · $12,500"), e é a pergunta que a pessoa traz ao abrir "minhas despesas".
- **"+ Adicionar cartão" leva a `/cartoes#novo-cartao`**: o formulário mora na tela de Cartões (módulo 5); a âncora o abre direto lá.

## 🧪 Como testar

1. Captura (1440 px).

## 📎 Documentação afetada

- [[Transacoes]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
