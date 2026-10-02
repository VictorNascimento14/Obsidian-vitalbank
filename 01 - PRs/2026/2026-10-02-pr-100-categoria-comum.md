---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 100
url: https://github.com/VictorNascimento14/Vitalbank/pull/100
branch: refactor/categoria-comum
tags: [pr, refactor, transacoes]
status: merged
---

# PR #100 — refactor(telas): rótulo e ícone da categoria num módulo comum

## 🎯 Contexto

Preparação de Contas. Fecha a issue #99.

## 🔧 Mudanças

- `src/telas/comum/categoria.tsx` (novo); `src/telas/transacoes/{TabelaDeTransacoes,BaixarRecibo}.tsx`.

## 🧠 Decisões técnicas

- **Tela não importa de outra tela**; o que duas telas usam mora em `src/telas/comum/`.
- **Ícone por categoria** (assinatura → nota musical, compra → sacola, serviço → ferramenta…) num mapa só: a mesma transação tem a mesma cara em qualquer lista.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Transacoes]]
- [[2026]] (changelog)
