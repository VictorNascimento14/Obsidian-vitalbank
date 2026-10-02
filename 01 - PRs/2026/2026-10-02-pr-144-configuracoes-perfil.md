---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 144
url: https://github.com/VictorNascimento14/Vitalbank/pull/144
branch: feat/configuracoes-perfil
tags: [pr, configuracoes, formulario, privacidade]
status: aberto
---

# PR #144 — feat(configuracoes): aba Editar perfil com prévia local da foto

## 🎯 Contexto

Configurações, item 1. Fecha a issue #143.

## 🔧 Mudanças

- `src/dados/{index.ts, sementes/perfil.ts}`; `src/telas/configuracoes/{EditarPerfil,Configuracoes}.tsx` + teste; `src/app/(painel)/configuracoes/page.tsx`.

## 🕵️ Dado sensível

- A foto escolhida nunca sai do navegador: vira um endereço `blob:` local, revogado quando troca ou a tela fecha.
- O perfil usa os exemplos estáveis do `CLAUDE.md`; o CEP é `00000-000`.

## 🧠 Decisões técnicas

- **`<img>` em vez de `next/image`** para a prévia: `blob:` não passa pelo otimizador (e o export é estático).
- **Senha fora do perfil**: misturar troca de senha com dados de cadastro faz a pessoa salvar uma coisa achando que salvou a outra.

## 🧪 Como testar

1. Captura (1440 px) e testes.

## 📎 Documentação afetada

- [[Configuracoes]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
