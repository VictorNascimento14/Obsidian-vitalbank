---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 110
url: https://github.com/VictorNascimento14/Vitalbank/pull/110
branch: refactor/formatar-numero-no-dominio
tags: [pr, refactor, dominio, nextjs]
status: merged
---

# PR #110 — refactor(dominio): formatarNumero sai do módulo cliente para servir ao servidor

## 🎯 Contexto

Bug latente achado ao montar Investimentos. Fecha a issue #109.

## 🔧 Mudanças

- `src/dominio/numero.ts` (novo); `src/ui/movimento/{NumeroAnimado.tsx, index.ts, NumeroAnimado.test.tsx}`; `src/ui/graficos/{GraficoDeBarras,GraficoDeLinha,GraficoDeColunas}.tsx`; `src/ui/base/CartaoDeResumo.tsx`.

## 🧠 Decisões técnicas

- **Reexportar do domínio, não do módulo cliente.** `export { formatarNumero } from "./NumeroAnimado"` manteria a referência de cliente; o índice aponta para `@/dominio/numero`.

## ⚠️ Armadilhas e aprendizados

- O Vitest com jsdom executa tudo no mesmo lugar, então não vê a fronteira servidor/cliente. Só o Next acusa (no SSR ou no `build`). Ver [[2026-10-02-funcao-de-modulo-cliente-nao-roda-no-servidor]].

## 🧪 Como testar

1. `pnpm build`.

## 📎 Documentação afetada

- [[Movimento]]
- [[2026-10-02-funcao-de-modulo-cliente-nao-roda-no-servidor]]
- [[2026]] (changelog)
