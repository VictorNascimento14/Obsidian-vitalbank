---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 102
url: https://github.com/VictorNascimento14/Vitalbank/pull/102
branch: feat/contas-ultima-transacao
tags: [pr, contas, transacoes]
status: merged
---

# PR #102 — feat(contas): bloco Última transação com tipo, cartão e situação

## 🎯 Contexto

Contas, item 2. Usa [[2026-10-02-pr-100-categoria-comum]]. Fecha a issue #101.

## 🔧 Mudanças

- `src/telas/contas/UltimaTransacao.tsx` + teste; `src/app/(painel)/contas/page.tsx`.

## 🧠 Decisões técnicas

- **Uma grade por linha com trilhas fixas**, em vez de `<table>`: o bloco é uma lista de três itens, não dados tabulares para comparar; e no celular a linha se reorganiza sem esconder colunas de tabela.
- **Filtro na página** (sem salário e depósito): "última transação" na Contas é o que a pessoa confere — gastos e transferências.

## ⚠️ Armadilhas e aprendizados

- A primeira captura mostrou colunas tortas: com `1fr`/`auto`, cada linha (grade própria) dimensiona pelas próprias palavras. `minmax(0, Nfr)` e valor com largura fixa alinham.

## 🧪 Como testar

1. Capturas antes/depois do ajuste (1440 px).

## 📎 Documentação afetada

- [[Contas]]
- [[2026]] (changelog)
