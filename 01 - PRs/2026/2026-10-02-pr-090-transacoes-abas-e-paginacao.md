---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 90
url: https://github.com/VictorNascimento14/Vitalbank/pull/90
branch: feat/transacoes-abas-e-paginacao
tags: [pr, transacoes, abas, paginacao]
status: merged
---

# PR #90 — feat(transacoes): filtrar o extrato por entradas e saídas e paginar de 5 em 5

## 🎯 Contexto

Transações, item 3. Usa [[2026-10-02-pr-034-abas]] e [[2026-10-02-pr-088-paginacao]]. Fecha a issue #89.

## 🔧 Mudanças

- `src/telas/transacoes/Extrato.tsx` + teste; `src/app/(painel)/transacoes/page.tsx`.

## 🧠 Decisões técnicas

- **Filtro e paginação no cliente**: 20 itens fictícios cabem na página. Com backend, `listarTransacoes` ganha `filtro` e `pagina`, e o bloco passa a pedir em vez de cortar.
- **`key` da tabela com aba e página**: força a remontagem, e a cascata de entrada repete — o olho percebe que a lista mudou.
- **`atual = min(pagina, total)`**: se a aba nova tiver menos páginas, a paginação não aponta para uma página vazia.

## ⚠️ Armadilhas e aprendizados

- No teste, o painel novo das `Abas` só aparece depois da animação de saída do anterior (`AnimatePresence mode="wait"`); o teste espera com `waitFor`.

## 🧪 Como testar

1. Captura (1440 px) na página 2.

## 📎 Documentação afetada

- [[Transacoes]]
- [[2026]] (changelog)
