---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 16
url: https://github.com/VictorNascimento14/Vitalbank/pull/16
branch: feat/dominio-cartao
tags: [pr, dominio, cartao, seguranca]
status: merged
---

# PR #16 — feat(dominio): mascarar cartão e validar número e validade digitados

## 🎯 Contexto

Domínio, máscara de cartão. Regra em [[ADR-001-frontend-primeiro-com-dados-mock]] (item 4). Fecha a issue #15.

## 🔧 Mudanças

- `src/dominio/cartao.ts` — máscara para tela e lista; agrupamento, Luhn e validade para o formulário.
- `src/dominio/cartao.test.ts`.

## 🕵️ Dado sensível

O PR não guarda nada. Define a regra de que a tela recebe só o final (`ultimos4`) e, no formulário, o número digitado vira final assim que valida.

## 🧠 Decisões técnicas

- **Luhn diz "foi digitado certo", não "o cartão existe".** O texto do formulário (PR futuro) deixa isso claro: na v1 nada é enviado a lugar nenhum.
- **`validadeEmDia` vale até o fim do mês impresso**: "10/26" ainda vale em 02/10/2026.
- **O teste gera o número** (`comVerificador`) em vez de usar um "número de teste" famoso: número fixo com Luhn válido é exatamente o que a regra proíbe.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[CartaoMascarado]]
- [[vitalbank-frontend]]
- [[2026]] (changelog)
