---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 138
url: https://github.com/VictorNascimento14/Vitalbank/pull/138
branch: feat/emprestimos-ativos
tags: [pr, emprestimos, tabela, animacao]
status: aberto
---

# PR #138 — feat(emprestimos): tabela de empréstimos ativos com pagamento de parcela

## 🎯 Contexto

Empréstimos, item 2 — fecha a tela. Fecha a issue #137.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/emprestimos.ts}`; `src/telas/emprestimos/EmprestimosAtivos.tsx` + teste; `src/app/(painel)/emprestimos/page.tsx`.

## 🧠 Decisões técnicas

- **Estado por id** (`{ e1: 3850000, … }`) inicializado da semente; o total é soma desse estado, então nunca discorda das linhas.
- **Pisca por `key`**: o `motion.span` tem `key` no valor; quando o valor muda, ele remonta e anima o fundo de turquesa até transparente.
- **`<tfoot>` com `th scope="row"`**: "Total" é cabeçalho da linha para o leitor de tela.

## ⚠️ Armadilhas e aprendizados

- O total esperado no teste estava errado na primeira versão (conta de cabeça). O teste reprovou, e o número certo (R$ 543.800,00) foi conferido somando a semente.

## 🧪 Como testar

1. Captura após pagar a linha 01 (1440 px).

## 📎 Documentação afetada

- [[Emprestimos]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
