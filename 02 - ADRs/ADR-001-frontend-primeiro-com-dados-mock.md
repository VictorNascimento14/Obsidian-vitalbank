---
tipo: adr
numero: 1
data: 2026-10-02
status: aceito
tags: [adr, arquitetura, dados]
---

# ADR-001 — Front-end primeiro, com dados fictícios atrás de uma fronteira

## Contexto

O Vitalbank desenha saldo, cartão, extrato e investimento. Guardar isso num servidor exige autenticação,
controle de acesso e cuidado com dado financeiro — decisões que a v1 não precisa tomar para validar o
que importa agora: as telas, os fluxos e a sensação de usar o produto. Ver [[visao-de-produto]].

## Decisão

1. **A v1 é só front-end**: Next.js com export estático, sem backend, sem banco e sem login. A demo sai
   no GitHub Pages.
2. **Os dados são fictícios e moram em `src/dados/`** — tipos, sementes e funções de leitura. A tela
   nunca importa semente direto: lê pelas funções, que são o ponto onde o backend vai entrar.
3. **Dinheiro é inteiro em centavos** do começo ao fim. Soma de float de reais erra centavo, e o erro
   aparece justamente no saldo.
4. **Cartão só existe mascarado.** A semente guarda os quatro últimos dígitos, não o número.
5. Ações que "mexeriam no dinheiro" (transferir, adicionar cartão, salvar configurações) mudam só o
   estado da página e dizem isso a quem usa.

## Consequências

- O backend entra trocando o miolo das funções de `src/dados/`, sem mexer em tela.
- Recarregar a página volta a demonstração ao estado inicial — aceitável numa demo.
