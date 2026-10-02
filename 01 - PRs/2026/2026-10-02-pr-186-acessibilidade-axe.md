---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 186
url: https://github.com/VictorNascimento14/Vitalbank/pull/186
branch: test/acessibilidade-axe
tags: [pr, testes, acessibilidade]
status: aberto
---

# PR #186 — test(a11y): axe nas nove telas, com controle negativo

## 🎯 Contexto

Robustez, item 2. Fecha a issue #185.

## 🔧 Mudanças

- `package.json` (`axe-core`); `src/teste/acessibilidade.test.tsx`.

## 🧠 Decisões técnicas

- **`axe-core` direto**, sem `jest-axe`/`vitest-axe`: um `axe.run(container)` e a lista de violações como texto legível no diff do teste.
- **Página inteira, não componente**: o axe pega problema de composição (dois `main`, título pulando nível, `id` repetido) que teste de componente não vê.
- **Controle negativo** no mesmo arquivo: verde sem controle pode ser regra desligada, import errado ou container vazio.

## ⚠️ Armadilhas e aprendizados

- Contraste não roda no jsdom. Se um dia o tema mudar de paleta, contraste precisa de verificação no navegador (Playwright + axe).

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[vitalbank-frontend]]
- [[2026]] (changelog)
