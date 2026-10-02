---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 2
url: https://github.com/VictorNascimento14/Vitalbank/pull/2
branch: chore/scaffolding
tags: [pr, fundacao]
status: merged
---

# PR #2 — chore: scaffolding Next.js + TypeScript + Tailwind 4 + pnpm

## 🎯 Contexto

Fundação, item 1 do [[2026-10-02-plano-da-v1]]. Decisão de stack em [[ADR-001-frontend-primeiro-com-dados-mock]]. Fecha a issue #1.

## 🔧 Mudanças

- `package.json` — Next 16, React 19, Tailwind 4, ESLint 9; scripts `lint` e `type-check`.
- `src/app/layout.tsx` — `lang="pt-BR"`, título e descrição do produto.
- `src/app/page.tsx` — página provisória.
- Sai o boilerplate (fontes Geist, SVGs de exemplo).

## 🧠 Decisões técnicas

- **`type-check` = `next typegen && tsc --noEmit`.** O Next 16 gera tipos globais (`LayoutProps`, `PageProps`) por rota; numa clonagem limpa, `tsc` sozinho reprova o `layout.tsx` com `Cannot find name 'LayoutProps'`.
- **pnpm**, com `pnpm-workspace.yaml` ignorando build de `sharp` e `unrs-resolver` (o app não otimiza imagem no servidor: o export é estático).

## ⚠️ Armadilhas e aprendizados

- O Next 16 escreve um `AGENTS.md` avisando que a API mudou e apontando para `node_modules/next/dist/docs/`. O `CLAUDE.md` do repositório importa esse arquivo.

## 🧪 Como testar

1. `pnpm dev` → "Vitalbank" no centro da tela.
2. `rm -rf .next && pnpm type-check` passa.

## 📎 Documentação afetada

- [[vitalbank-frontend]]
- [[2026]] (changelog)
