---
tipo: aprendizado
data: 2026-10-02
contexto: resumo de Investimentos
tags: [aprendizado, nextjs, rsc]
---

# Função de módulo `"use client"` não roda no servidor

Tudo que um arquivo `"use client"` exporta vira, para os componentes de servidor, uma **referência de
cliente**: dá para renderizar como componente ou passar como prop a outro componente cliente, mas não
para **chamar**. O `formatarNumero` morava em `NumeroAnimado.tsx` (cliente) e, chamado pelo resumo de
Investimentos (servidor), derrubou a página:

> Attempted to call formatarNumero() from the server but formatarNumero is on the client.

**O teste não pega:** o Vitest com jsdom roda tudo junto. Quem pega é o SSR (página 500) ou o `next build`.

**Regra:** função pura vai para `src/dominio/` (sem diretiva); o módulo cliente só importa. E índice
que reexporta não reexporta do arquivo cliente.

Achado em [[2026-10-02-pr-110-formatar-numero-no-dominio]].
