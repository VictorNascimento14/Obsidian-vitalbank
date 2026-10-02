---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 78
url: https://github.com/VictorNascimento14/Vitalbank/pull/78
branch: feat/grafico-de-colunas
tags: [pr, graficos, animacao]
status: merged
---

# PR #78 — feat(graficos): colunas com destaque que segue o mouse

## 🎯 Contexto

Gráficos, item 6. Fecha a issue #77.

## 🔧 Mudanças

- `src/ui/graficos/GraficoDeColunas.tsx` + teste; exportado em `@/ui`.

## 🧠 Decisões técnicas

- **Cor animada pelo motion (`animate={{ fill }}`)** com transições separadas por propriedade: o `scaleY` da entrada não espera a troca de cor, e vice-versa.
- **Um único `<text>` de valor com `key` na coluna ativa**: o `AnimatePresence` faz o valor sair de uma coluna e entrar na outra, em vez de seis rótulos escondidos.

## 🧪 Como testar

1. Captura do bloco.

## 📎 Documentação afetada

- [[Graficos]]
- [[2026]] (changelog)
