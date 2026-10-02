---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 184
url: https://github.com/VictorNascimento14/Vitalbank/pull/184
branch: feat/sistema-tela-de-erro
tags: [pr, sistema, robustez, acessibilidade]
status: aberto
---

# PR #184 — feat(sistema): tela de erro com tentar de novo, sem derrubar a casca

## 🎯 Contexto

Robustez, item 1 (seção 10 do [[2026-10-02-plano-da-v1]]). Fecha a issue #183.

## 🔧 Mudanças

- `src/app/(painel)/error.tsx` + teste.

## 🧠 Decisões técnicas

- **Dentro do `(painel)`**: o limite de erro fica abaixo do layout, então a casca sobrevive.
- **`retry`, não `reset`**: no Next 16 a prop mudou de nome. Conferido em `node_modules/next/dist/docs/…/error.md` antes de escrever — exatamente o que o `AGENTS.md` pede.

## ⚠️ Armadilhas e aprendizados

- Exemplos da internet (e a memória de quem já usou Next 13–15) dizem `reset`. Com `reset`, o botão chamaria `undefined`.

## 🧪 Como testar

1. Captura com página que lança erro.

## 📎 Documentação afetada

- [[PaginasDeSistema]]
- [[2026]] (changelog)
