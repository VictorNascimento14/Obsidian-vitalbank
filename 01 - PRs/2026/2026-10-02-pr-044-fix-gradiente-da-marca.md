---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 44
url: https://github.com/VictorNascimento14/Vitalbank/pull/44
branch: fix/gradiente-da-marca
tags: [pr, bug, marca, svg]
status: merged
---

# PR #44 — fix(marca): dar id único ao gradiente do símbolo

## 🎯 Contexto

Bug do [[2026-10-02-pr-038-marca]], achado ao verificar a casca no celular. Fecha a issue #43.

## 🔧 Mudanças

- `src/ui/casca/Marca.tsx` — `useId()` no id do gradiente; `"use client"`.
- `src/ui/casca/Marca.test.tsx` — teste de duas marcas na mesma página.

## 🧠 Decisões técnicas

- **`useId` e não contador global:** estável entre servidor e cliente, sem descasar na hidratação. Os `:` que ele gera são tirados porque, em `url(#...)`, exigiriam escape.
- **Componente cliente** só por causa do hook; o custo é o SVG ir no bundle, que é pequeno.

## ⚠️ Armadilhas e aprendizados

- `id` dentro de SVG é global no documento. Componente que desenha `<defs>` precisa de id por instância. Ver [[2026-10-02-gradiente-de-svg-com-id-repetido]].

## 🧪 Como testar

1. Captura em 375 px com a gaveta aberta.

## 📎 Documentação afetada

- [[Marca]]
- [[2026-10-02-gradiente-de-svg-com-id-repetido]]
- [[2026]] (changelog)
