---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 22
url: https://github.com/VictorNascimento14/Vitalbank/pull/22
branch: ui/numero-animado
tags: [pr, design, animacao, acessibilidade]
status: merged
---

# PR #22 — ui(movimento): número que conta até o valor, com leitura acessível

## 🎯 Contexto

Movimento, item 3. Base em [[2026-10-02-pr-018-movimento-base]]. Fecha a issue #21.

## 🔧 Mudanças

- `src/ui/movimento/NumeroAnimado.tsx` + teste; exportado no índice do movimento.

## 🧠 Decisões técnicas

- **`animate()` escrevendo no `textContent`**, não `useState`: 60 renders por segundo de um componente React por número na tela custam caro; mexer num nó de texto não custa nada.
- **O SSR já sai com o valor final.** Sem JavaScript, ou antes da hidratação, o número certo está lá; a contagem é enfeite.
- **Formato por nome (`"moeda"`), não por função.** Página do App Router é componente de servidor e não serializa função para o cliente.
- **Percentual em pontos-base** (inteiro), coerente com dinheiro em centavos.

## ⚠️ Armadilhas e aprendizados

- O Testing Library normaliza espaço — inclusive o não separável do Intl — antes de comparar texto. Nos testes de componente, escreva "R$ 12.750,00" com espaço comum; nos testes de função pura (`toBe`), o NBSP precisa estar lá.

## 🧪 Como testar

1. `pnpm test`.

## 📎 Documentação afetada

- [[Movimento]]
- [[2026]] (changelog)
