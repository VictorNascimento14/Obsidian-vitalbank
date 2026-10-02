---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 56
url: https://github.com/VictorNascimento14/Vitalbank/pull/56
branch: feat/visao-geral-transacoes-recentes
tags: [pr, visao-geral, transacoes]
status: merged
---

# PR #56 — feat(visao-geral): bloco Transações recentes

## 🎯 Contexto

Visão geral, item 2. Usa [[2026-10-02-pr-054-data-media]]. Fecha a issue #55.

## 🔧 Mudanças

- `src/telas/visao-geral/TransacoesRecentes.tsx` + teste.
- `src/app/(painel)/page.tsx` — segunda leitura em paralelo.
- `src/dados/sementes/transacoes.ts` — descrições mais curtas; a primeira vira "Fatura do cartão" (saída).

## 🧠 Decisões técnicas

- **Pastilha pelo meio, não pela categoria**: é o que o kit desenha (cartão, PayPal, moeda).
- **`Promise.all`** na página: as leituras são independentes; quando virarem rede, não vão em fila.

## ⚠️ Armadilhas e aprendizados

- Texto em português na coluna de 350 px: a captura mostrou data em três linhas e descrição cortada. Saiu o formato médio e saíram descrições de até ~16 caracteres na semente.

## 🧪 Como testar

1. Captura 1440 px.

## 📎 Documentação afetada

- [[VisaoGeral]]
- [[2026]] (changelog)
