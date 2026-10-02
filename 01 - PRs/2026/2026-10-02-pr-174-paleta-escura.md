---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 174
url: https://github.com/VictorNascimento14/Vitalbank/pull/174
branch: ui/paleta-escura
tags: [pr, design, tema, acessibilidade]
status: merged
---

# PR #174 — ui(tema): paleta escura nos tokens, seguindo o sistema

## 🎯 Contexto

Sistema, item 7 (parte 1). Promessa do [[ADR-002-design-system-bankdash]] (cor só por token) cobrada. Fecha a issue #173.

## 🔧 Mudanças

- `src/app/globals.css`; `src/telas/visao-geral/EstatisticaDeDespesas.tsx` (fatia em `marinho`).

## 🧠 Decisões técnicas

- **Bloco repetido** na `@media` e no `[data-tema="escuro"]`: CSS não tem "ou" entre media query e seletor sem duplicar; o bloco é curto e fica lado a lado.
- **`:not([data-tema="claro"])`**: quem escolheu claro num sistema escuro continua no claro.
- **Primária mais clara no escuro**: `#1814F3` sobre `#171A2E` não passa no contraste para texto (link, item ativo).

## ⚠️ Armadilhas e aprendizados

- O token `tinta` tinha dois papéis: texto de título e cor de fatia. No escuro, o texto precisa clarear e a fatia não. Papel diferente, token diferente (`marinho`).

## 🧪 Como testar

1. Capturas em modo escuro.

## 📎 Documentação afetada

- [[linguagem-visual]]
- [[ADR-002-design-system-bankdash]]
- [[2026]] (changelog)
