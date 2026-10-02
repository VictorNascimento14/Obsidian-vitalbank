---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 176
url: https://github.com/VictorNascimento14/Vitalbank/pull/176
branch: feat/tema-alternancia
tags: [pr, tema, animacao, acessibilidade]
status: aberto
---

# PR #176 — feat(tema): alternar claro e escuro com transição em círculo e sem piscar

## 🎯 Contexto

Sistema, item 7 (parte 2). Usa [[2026-10-02-pr-174-paleta-escura]]. Fecha a issue #175.

## 🔧 Mudanças

- `src/ui/tema/{tema.ts, AlternadorDeTema.tsx}` + teste; `src/ui/casca/Cabecalho.tsx`; `src/ui/index.ts`; `src/app/layout.tsx`; `src/app/globals.css`.

## 🕵️ Dado sensível

O `localStorage` guarda só "claro"/"escuro" — conveniência deste navegador, não dado da conta.

## 🧠 Decisões técnicas

- **Script no `<head>`**, não `useEffect`: o efeito roda depois da pintura, e a página abriria clara para depois escurecer.
- **`useSyncExternalStore`** para ler o tema: a fonte de verdade é o `<html>`; o botão acompanha até mudança feita fora dele. O `useEffect` + `setState` da primeira versão foi barrado pelo lint do React 19 (`set-state-in-effect`).
- **View Transitions com origem no clique** (`--vt-x/--vt-y`): só anima `clip-path` da captura nova; o navegador cuida do resto.

## 🧪 Como testar

1. Captura após o clique (1440 px); teste do `data-tema` e do `localStorage`.

## 📎 Documentação afetada

- [[Tema]]
- [[Cabecalho]]
- [[2026]] (changelog)
