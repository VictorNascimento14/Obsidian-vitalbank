---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 209
url: https://github.com/VictorNascimento14/Vitalbank/pull/209
branch: fix/documentacao-isenta-dependabot
tags: [pr, ci, deps]
status: merged
---

# PR #209 — fix(ci): não exigir nota do cofre nos PRs do Dependabot

## 🎯 Contexto

Efeito colateral de [[2026-10-02-pr-200-dependabot]] com a regra do 📓. Fecha a issue #208.

## 🔧 Mudanças

- `.github/workflows/pr-documentacao.yml`.

## 🧠 Decisões técnicas

- **Filtro pelo autor do PR** (`pull_request.user.login`), não pelo ator do evento: um rebase pedido por alguém continua sendo PR do robô.
- **Só a nota é dispensada**: formatação, lint, tipos, testes, axe e build continuam valendo para o Dependabot.

## ⚠️ Armadilhas e aprendizados

- Os PRs #201–#205 sobem *major* das Actions (`checkout` 7, `setup-node` 7, `pnpm/action-setup` 6, `upload-pages-artifact` 5, `deploy-pages` 5). Ficam para revisão humana: *major* de Action pode mudar comportamento do deploy.

## 🧪 Como testar

1. Rebase de um PR do Dependabot após o merge.

## 📎 Documentação afetada

- [[vitalbank-frontend]]
- [[2026]] (changelog)
