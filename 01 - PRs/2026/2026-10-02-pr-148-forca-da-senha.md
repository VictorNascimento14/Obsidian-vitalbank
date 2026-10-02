---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 148
url: https://github.com/VictorNascimento14/Vitalbank/pull/148
branch: feat/dominio-forca-da-senha
tags: [pr, dominio, seguranca]
status: aberto
---

# PR #148 — feat(dominio): força da senha e regra mínima de troca

## 🎯 Contexto

Configurações, item 3 (parte 1). Fecha a issue #147.

## 🔧 Mudanças

- `src/dominio/senha.ts` + teste.

## 🕵️ Dado sensível

Nenhuma senha sai da função; a lista de senhas comuns é pública (topo de qualquer vazamento) e serve só para pontuar zero.

## 🧠 Decisões técnicas

- **Lista de senhas inteiras, não prefixos.** A primeira versão zerava qualquer senha que *começasse* com "abcd" ou "1234" — e punia senhas boas como "abcd-Rio-2026!". Ficou a comparação exata com uma lista curta.
- **Força ≠ aceitável**: a pessoa pode salvar uma senha "Média" que cumpre o mínimo; o medidor informa, não proíbe.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[ForcaDaSenha]]
- [[2026]] (changelog)
