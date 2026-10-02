---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 196
url: https://github.com/VictorNascimento14/Vitalbank/pull/196
branch: chore/ci-formatacao
tags: [pr, ci, qualidade]
status: merged
---

# PR #196 — chore(ci): checar a formatação no PR e pular o commit de estilo no blame

## 🎯 Contexto

Robustez, item 4 (parte 2). Segue [[2026-10-02-pr-194-prettier]]. Fecha a issue #195.

## 🔧 Mudanças

- `.github/workflows/ci.yml`; `.git-blame-ignore-revs` (novo); `CLAUDE.md`.

## 🧠 Decisões técnicas

- **Formatação primeiro** no CI: é o check mais barato; PR desformatado falha em segundos.
- **`.git-blame-ignore-revs`**: o GitHub lê o arquivo sozinho; o blame de qualquer linha mostra quem escreveu a lógica, não o commit que mudou a indentação.

## 🧪 Como testar

1. CI deste PR.

## 📎 Documentação afetada

- [[vitalbank-frontend]]
- [[2026]] (changelog)
