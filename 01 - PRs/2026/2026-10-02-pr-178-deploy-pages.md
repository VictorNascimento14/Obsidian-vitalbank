---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 178
url: https://github.com/VictorNascimento14/Vitalbank/pull/178
branch: chore/deploy-pages
tags: [pr, deploy, infra]
status: merged
---

# PR #178 — chore(deploy): publicar a demo no GitHub Pages a cada merge na main

## 🎯 Contexto

Sistema, item 8. Decisão de export estático em [[ADR-001-frontend-primeiro-com-dados-mock]]. Fecha a issue #177.

## 🔧 Mudanças

- `next.config.ts`; `.github/workflows/pages.yml`; Pages do repositório com `build_type: workflow`.

## 🧠 Decisões técnicas

- **`basePath` por variável de ambiente**: localmente e no CI de PR o app fica na raiz; só o build do Pages leva `/Vitalbank`. Uma configuração, dois destinos.
- **`trailingSlash: true`**: o Pages serve `/contas/` como `contas/index.html`; sem a barra, `/contas` cairia na 404. O `itemAtivo` da navegação já tolera a barra final.
- **`.nojekyll`**: o Pages, por padrão, passa pelo Jekyll, que ignora pastas começando com `_` — e todo o JavaScript do Next mora em `_next/`.
- Lido em `node_modules/next/dist/docs/…/static-exports.md` (Next 16).

## 🧪 Como testar

1. Export servido localmente em `/Vitalbank/` (200 nas telas, 404 no inexistente, navegação pelo menu).

## 📎 Documentação afetada

- [[DeployPages]]
- [[ADR-001-frontend-primeiro-com-dados-mock]]
- [[2026]] (changelog)
