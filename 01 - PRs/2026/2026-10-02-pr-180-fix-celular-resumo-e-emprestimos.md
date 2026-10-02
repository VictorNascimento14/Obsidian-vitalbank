---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 180
url: https://github.com/VictorNascimento14/Vitalbank/pull/180
branch: fix/celular-resumo-e-emprestimos
tags: [pr, bug, responsivo]
status: merged
---

# PR #180 — fix(celular): cartões de resumo e tabela de empréstimos cabem em 375 px

## 🎯 Contexto

Bug de celular em [[2026-10-02-pr-096-cartao-de-resumo]] (valores longos) e [[2026-10-02-pr-138-emprestimos-ativos]] (tabela). Fecha a issue #179.

## 🔧 Mudanças

- `src/ui/base/CartaoDeResumo.tsx`; `src/telas/emprestimos/EmprestimosAtivos.tsx`.

## ⚠️ Armadilhas e aprendizados

- A primeira tentativa (estreitar células e botão) não mudou nada: a medida continuava 344 px. O culpado era o `min-w-[320px]` da tabela, que vale independentemente do conteúdo. **Medir o `scrollWidth` do contêiner** achou em um passo o que três ajustes no escuro não achariam.
- O `CartaoDeResumo` foi testado com "R$ 12.750,00" (Contas) e passou; o pior caso era "R$ 500.000,00" (Empréstimos). Ao criar um primitivo, testar com o maior valor que as telas vão usar.

## 🧪 Como testar

1. Capturas em 375 px e `scrollWidth` = `clientWidth`.

## 📎 Documentação afetada

- [[Primitivos]]
- [[Emprestimos]]
- [[2026]] (changelog)
