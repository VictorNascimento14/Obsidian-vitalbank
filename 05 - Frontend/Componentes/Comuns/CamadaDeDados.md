---
tipo: componente
camada: dados
arquivo: src/dados/
ultima_atualizacao: 2026-10-02
tags: [dados]
---

# Camada de dados

A fronteira do [[ADR-001-frontend-primeiro-com-dados-mock]]: as telas leem **só** por `src/dados/index.ts`.

| Função | Devolve |
|---|---|
| `listarCartoes()` | cartões (início, final, titular, validade, saldo, variante) |
| `listarTransacoes({ limite? })` | movimentos do mais recente ao mais antigo; valor com sinal |
| `atividadeSemanal()` | 7 dias com entradas e saídas |
| `despesasPorCategoria()` | total do mês por categoria |
| `listarContatos()` | contatos frequentes da transferência |
| `historicoDeSaldo()` | saldo de fim de mês, 12 meses |
| `despesasMensais()` | gasto por mês, 6 meses |
| `resumoDaConta()` | saldo, receitas, despesas, poupança |
| `debitoECredito()` | débito e crédito por dia, 7 dias |
| `faturasEnviadas()` | cobranças enviadas |
| `resumoDosInvestimentos()` | total, quantidade, retorno (pontos-base) |
| `investimentoAnual()` | total por ano, 6 anos |
| `receitaMensal()` | receita por mês, 12 meses |
| `listarCarteira()` | aplicações (empresas fictícias) |
| `acoesEmAlta()` | ações do dia (nomes fictícios) |
| `linhasDeCredito()` | limites pré-aprovados |

- Funções `async`: a assinatura já é a de quando houver backend.
- Sementes em `src/dados/sementes/`, titular "Cliente Exemplo".
- `dados.test.ts` reprova sequência de 13–19 dígitos que passe no Luhn.

Introduzido em [[2026-10-02-pr-048-dados-base]].
