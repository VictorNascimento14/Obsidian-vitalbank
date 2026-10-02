---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 190
url: https://github.com/VictorNascimento14/Vitalbank/pull/190
branch: feat/botao-ocultar-valores
tags: [pr, privacidade, animacao, acessibilidade]
status: merged
---

# PR #190 — feat(privacidade): botão de olho para ocultar valores, lembrado entre visitas

## 🎯 Contexto

Robustez, item 3 (parte 2). Usa [[2026-10-02-pr-188-valores-sensiveis]]. Fecha a issue #189.

## 🔧 Mudanças

- `src/ui/privacidade/{ocultar.ts, BotaoOcultarValores.tsx}` + teste; `src/ui/casca/Cabecalho.tsx`; `src/ui/index.ts`; `src/app/layout.tsx`.

## 🧠 Decisões técnicas

- **Mesmo desenho do tema** ([[Tema]]): atributo no `<html>` como fonte de verdade, `useSyncExternalStore` para o botão, script no `<head>` para não piscar.
- **`aria-pressed` com rótulo fixo** ("Ocultar valores"): o leitor de tela diz "pressionado"/"não pressionado", em vez de o nome do botão mudar.

## 🧪 Como testar

1. Captura com valores ocultos (1440 px) e o olho no celular (375 px).

## 📎 Documentação afetada

- [[OcultarValores]]
- [[Cabecalho]]
- [[2026]] (changelog)
