---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 130
url: https://github.com/VictorNascimento14/Vitalbank/pull/130
branch: ui/campo-de-selecao
tags: [pr, design, primitivos, acessibilidade]
status: merged
---

# PR #130 — ui(primitivos): CampoDeSelecao, o select nativo com a cara do Campo

## 🎯 Contexto

Primitivos. Fecha a issue #129.

## 🔧 Mudanças

- `src/ui/base/CampoDeSelecao.tsx` + teste; exportado em `@/ui`.

## 🧠 Decisões técnicas

- **Nativo, não lista própria**: com 2 a 6 opções, uma lista desenhada à mão só traria trabalho de acessibilidade (setas, Esc, rolagem) que o navegador já faz.
- **Seta fora do `<select>`**, com `pointer-events-none`: o clique passa para o select.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Primitivos]]
- [[2026]] (changelog)
