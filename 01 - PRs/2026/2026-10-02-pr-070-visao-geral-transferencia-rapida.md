---
tipo: pr
data: 2026-10-02
autor: VictorNascimento14
projeto: Vitalbank
pr: 70
url: https://github.com/VictorNascimento14/Vitalbank/pull/70
branch: feat/visao-geral-transferencia-rapida
tags: [pr, visao-geral, transferencia, animacao, acessibilidade]
status: merged
---

# PR #70 — feat(visao-geral): Transferência rápida com fila de contatos e envio animado

## 🎯 Contexto

Visão geral, item 5. Regra de "nada sai da conta" em [[ADR-001-frontend-primeiro-com-dados-mock]]. Fecha a issue #69.

## 🔧 Mudanças

- `src/dados/{tipos.ts, index.ts, sementes/contatos.ts}`.
- `src/telas/visao-geral/TransferenciaRapida.tsx` + teste.
- `src/app/(painel)/page.tsx` — última linha da grade.

## 🧠 Decisões técnicas

- **Valor lido por `paraCentavos`** ([[Dinheiro]]): "525,50", "1.000" e "R$ 10" valem; "abc" e "1,234" não.
- **Confirmação em `role="status"`**: o leitor de tela anuncia o envio sem roubar o foco.
- **Item que sai da fila fica `aria-hidden` + `inert`** (`useIsPresent`): durante a animação de saída ele ainda está no DOM com as props antigas, e seria anunciado como "pressionado".

## ⚠️ Armadilhas e aprendizados

- **Bug pego pela captura de tela:** ao avançar a fila, o contato escolhido saía da vista mas continuava escolhido — a pessoa enviaria para alguém que não está vendo. Agora a escolha passa ao primeiro visível. Teste: "quem é enviado está sempre à vista".
- **No jsdom a animação de saída não termina**, então o teste viu dois botões "pressionados". Em vez de esperar no teste, o item que sai ficou inerte — o teste tinha achado um problema real de acessibilidade.

## 🧪 Como testar

1. Capturas antes e depois da correção (1440 px): após avançar e enviar, o anel e a mensagem apontam para a mesma pessoa.

## 📎 Documentação afetada

- [[VisaoGeral]]
- [[CamadaDeDados]]
- [[2026]] (changelog)
