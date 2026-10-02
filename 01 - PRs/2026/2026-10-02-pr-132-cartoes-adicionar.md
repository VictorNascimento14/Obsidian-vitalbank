---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 132
url: https://github.com/VictorNascimento14/Vitalbank/pull/132
branch: feat/cartoes-adicionar
tags: [pr, cartoes, formulario, seguranca]
status: merged
---

# PR #132 — feat(cartoes): formulário de novo cartão com máscara, Luhn e validade

## 🎯 Contexto

Cartões, item 4. Usa o domínio de [[CartaoMascarado]]. Fecha a issue #131.

## 🔧 Mudanças

- `src/telas/cartoes/AdicionarCartao.tsx` + teste; `src/app/(painel)/cartoes/page.tsx`.

## 🕵️ Dado sensível

O número digitado vive só no estado do campo enquanto a pessoa digita. Ao validar, o estado é limpo e só os 4 últimos dígitos vão para a confirmação. Nada é enviado nem guardado ([[ADR-001-frontend-primeiro-com-dados-mock]]). `autoComplete="off"` nos campos do cartão.

## 🧠 Decisões técnicas

- **Validação ao enviar, não a cada tecla**: mensagem de erro aparecendo enquanto a pessoa ainda digita o número é ruído.
- **Mensagem diferente para vazio e para errado**: "Informe o número" diz o que fazer; "algum dígito parece trocado" só faz sentido com algo digitado.
- **Funções puras exportadas** (`mascararValidade`, `validarNovoCartao`) com teste próprio.

## 🧪 Como testar

1. Captura com os erros (1440 px); testes do fluxo de sucesso.

## 📎 Documentação afetada

- [[CartoesDeCredito]]
- [[CartaoMascarado]]
- [[2026]] (changelog)
