---
tipo: adr
numero: 4
data: 2026-10-02
status: aceito
tags: [adr, graficos, design]
---

# ADR-004 — Gráficos próprios em SVG, animados com motion

## Contexto

O kit tem seis tipos de gráfico: barras agrupadas (Atividade semanal, Débito e crédito), barras com
destaque (Minhas despesas), pizza "explodida" (Estatística de despesas), rosca (Gasto por cartão), área
(Histórico de saldo) e linha (Investimentos). Bibliotecas de gráfico entregam o tipo, mas não o visual:
barra com canto arredondado só em cima, grade tracejada, fatia afastada do centro com rótulo dentro.

## Decisão

1. **Gráficos em SVG próprio**, em `src/ui/graficos/`, com a matemática separada (`escala.ts`, testada).
2. **Animação de entrada com motion**: barras crescem da base, fatias abrem, linha se desenha
   (`pathLength`) — tudo respeitando o movimento reduzido ([[ADR-003-movimento-com-motion]]).
3. **Curva monotônica** em linha e área: nunca passa do pico.
4. Cada gráfico tem **tabela equivalente para leitor de tela** (`sr-only`), porque SVG de dados é
   mudo para quem não vê.

## Consequências

- Mais código nosso (~100 linhas por tipo) e nenhuma dependência de gráfico.
- Interação (dica ao passar o mouse) também é nossa — e fica no mesmo estilo do app.
