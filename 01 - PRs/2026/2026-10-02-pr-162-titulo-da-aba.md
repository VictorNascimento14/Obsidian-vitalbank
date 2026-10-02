---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 162
url: https://github.com/VictorNascimento14/Vitalbank/pull/162
branch: feat/sistema-titulo-da-aba
tags: [pr, sistema, acessibilidade, seo]
status: merged
---

# PR #162 — feat(sistema): título da aba do navegador por tela

## 🎯 Contexto

Sistema, item 3. Fecha a issue #161.

## 🔧 Mudanças

- `src/app/layout.tsx`; `src/ui/casca/navegacao.ts` (+ teste); `src/ui/index.ts`; as 9 `page.tsx` do `(painel)`.

## 🧠 Decisões técnicas

- **Título do mapa de navegação**: menu, cabeçalho e aba dizem a mesma coisa porque leem do mesmo lugar.
- **Erro para rota desconhecida**: página nova esquecida no mapa quebra o build, em vez de sair com título errado.
- `metadata` estática (não `generateMetadata`): o export é estático e o título não depende de dado.

## 🧪 Como testar

1. HTML do build.

## 📎 Documentação afetada

- [[ColunaLateral]]
- [[2026]] (changelog)
