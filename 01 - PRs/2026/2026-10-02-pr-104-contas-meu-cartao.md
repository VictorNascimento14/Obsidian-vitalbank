---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 104
url: https://github.com/VictorNascimento14/Vitalbank/pull/104
branch: feat/contas-meu-cartao
tags: [pr, contas, cartao]
status: aberto
---

# PR #104 — feat(contas): bloco Meu cartão com o cartão azul em destaque

## 🎯 Contexto

Contas, item 3. Fecha a issue #103.

## 🔧 Mudanças

- `src/telas/contas/MeuCartao.tsx` + teste; `src/app/(painel)/contas/page.tsx`.

## 🧠 Decisões técnicas

- **A escolha do cartão fica na página** (face azul, como no kit), e o bloco só desenha o que recebe — quando houver "cartão preferido" no backend, muda uma linha.

## 🧪 Como testar

1. Captura (1440 px).

## 📎 Documentação afetada

- [[Contas]]
- [[2026]] (changelog)
