---
tipo: adr
numero: 2
data: 2026-10-02
status: aceito
tags: [adr, design, frontend]
---

# ADR-002 — Sistema visual a partir do UI kit BankDash, em tokens próprios

## Contexto

O visual do Vitalbank parte do arquivo **BankDash — Dashboard UI Kit** da Figma Community: 9 telas em
três tamanhos (1440, 1024 e 375 px), 5 estilos de cor, 9 de texto e 1 de sombra.

## Decisão

1. **Os valores do Figma viram tokens** no bloco `@theme` do Tailwind 4 (`src/app/globals.css`), com
   nomes em português que dizem o papel (`primaria`, `tinta`, `tinta-suave`, `fundo`), não o valor.
   A tabela completa está em [[linguagem-visual]].
2. **Componente nunca usa hex solto.** Cor, raio, sombra e fonte só por token — é o que permite o tema
   escuro e qualquer retonalização sem caçar cor tela por tela.
3. **A marca é Vitalbank, não BankDash.** O logotipo e o nome são nossos; do kit vêm a grade, as cores,
   a tipografia e a composição das telas.
4. **Fotos de pessoa do kit não entram.** O avatar é desenhado com iniciais e gradiente: não há
   licença clara para os retratos, e eles pareceriam dado de cliente real.
5. **Ícones do Remix Icon** (`@remixicon/react`), que tem as versões preenchidas próximas das do kit.

## Consequências

- O Figma é a referência visual, não a fonte de verdade do código: divergência deliberada (marca,
  avatar, textos em português) é registrada na nota do PR que a introduz.
