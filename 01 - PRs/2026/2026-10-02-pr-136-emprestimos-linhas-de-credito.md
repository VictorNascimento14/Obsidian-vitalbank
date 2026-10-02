---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 136
url: https://github.com/VictorNascimento14/Vitalbank/pull/136
branch: feat/emprestimos-linhas-de-credito
tags: [pr, emprestimos]
status: aberto
---

# PR #136 — feat(emprestimos): linhas de crédito pessoal, empresarial, negócios e personalizada

## 🎯 Contexto

Empréstimos, item 1. Usa [[2026-10-02-pr-096-cartao-de-resumo]]. Fecha a issue #135.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/emprestimos.ts}`; `src/telas/emprestimos/LinhasDeCredito.tsx` + teste; `src/app/(painel)/emprestimos/page.tsx`.

## 🧠 Decisões técnicas

- **"Personalizado" usa a prop `texto`** do `CartaoDeResumo`: o kit escreve "Choose Money" no lugar do número.

## 🧪 Como testar

1. Teste e largura em 375 px.

## 📎 Documentação afetada

- [[Emprestimos]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
