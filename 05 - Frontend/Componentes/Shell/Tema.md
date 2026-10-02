---
tipo: componente
camada: ui
arquivo: src/ui/tema/
ultima_atualizacao: 2026-10-02
tags: [tema]
---

# Tema

- **Paleta**: variáveis redefinidas em `globals.css` — ver [[linguagem-visual]] e [[2026-10-02-pr-174-paleta-escura]].
- **Escolha**: `data-tema` no `<html>` (`claro`/`escuro`); sem escolha, vale o sistema.
- **Sem piscar**: `SCRIPT_DO_TEMA` no `<head>` aplica a escolha guardada antes da primeira pintura.
- **Botão**: `AlternadorDeTema` no [[Cabecalho]]; troca com View Transitions em círculo a partir do clique.

Introduzido em [[2026-10-02-pr-176-tema-alternancia]].
