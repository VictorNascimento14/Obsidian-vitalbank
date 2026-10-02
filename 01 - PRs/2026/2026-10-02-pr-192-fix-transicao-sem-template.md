---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 192
url: https://github.com/VictorNascimento14/Vitalbank/pull/192
branch: fix/transicao-sem-template
tags: [pr, bug, nextjs, casca]
status: merged
---

# PR #192 — fix(casca): transição entre telas na casca, sem o aviso de key do template

## 🎯 Contexto

Aviso introduzido pela soma de [[2026-10-02-pr-158-transicao-entre-telas]] com [[2026-10-02-pr-184-sistema-tela-de-erro]]. Achado ao capturar o botão de ocultar valores, com o console lido pelo Playwright. Fecha a issue #191.

## 🔧 Mudanças

- `src/app/(painel)/template.tsx` (removido) + teste; `src/ui/casca/Casca.tsx`; `src/ui/casca/Casca.test.tsx` (novo).

## 🧠 Decisões técnicas

- **`key={rota}` no miolo**, dentro da casca: mesmo efeito do template (remonta só o conteúdo), sem depender da combinação que dispara o aviso.

## ⚠️ Armadilhas e aprendizados

- Bisseção por arquivo achou a combinação em três rodadas: sem `template` → 0 avisos; sem `error` → 0; sem `loading` → 1. Ver [[2026-10-02-template-e-error-juntos-avisam-key]].
- O script de captura imprime erros de console da página — foi o que mostrou o aviso. Vale olhar o console em toda captura, não só a imagem.

## 🧪 Como testar

1. Console limpo em `/contas` (duas medições).

## 📎 Documentação afetada

- [[Casca]]
- [[2026-10-02-template-e-error-juntos-avisam-key]]
- [[2026]] (changelog)
