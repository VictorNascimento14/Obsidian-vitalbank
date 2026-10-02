---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 207
url: https://github.com/VictorNascimento14/Vitalbank/pull/207
branch: feat/sistema-manifesto-e-compartilhamento
tags: [pr, sistema, pwa, seo]
status: aberto
---

# PR #207 — feat(sistema): instalar como app e imagem de compartilhamento do link

## 🎯 Contexto

Robustez, item 7. Fecha a issue #206.

## 🔧 Mudanças

- `src/app/{manifest.ts, apple-icon.png, opengraph-image.png, layout.tsx}`; `public/icone-{192,512}.png`; `.github/workflows/pages.yml`.

## 🧠 Decisões técnicas

- **Convenções de arquivo do App Router** (`manifest.ts`, `apple-icon.png`, `opengraph-image.png`): o Next gera as tags com o `basePath` certo.
- **`manifest.ts` com `dynamic = "force-static"`**: no export estático, sai como arquivo no build.
- **Ícones com fundo e respiro de 19%**: no Android, o ícone *maskable* é recortado em círculo; o símbolo sem respiro perderia as pontas.

## ⚠️ Armadilhas e aprendizados

- Sem `metadataBase`, o Next escreveu `og:image` como `http://localhost:3000/...` — no build do CI, ninguém veria a imagem. O endereço vem de `URL_DO_SITE`, definido só no workflow do Pages.

## 🧪 Como testar

1. Tags no `out/index.html` com as variáveis do Pages.

## 📎 Documentação afetada

- [[DeployPages]]
- [[Marca]]
- [[2026]] (changelog)
