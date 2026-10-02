---
tipo: aprendizado
data: 2026-10-02
contexto: marca na gaveta do celular
tags: [aprendizado, svg, bug]
---

# Gradiente de SVG com id repetido some quando a primeira cópia está escondida

`id` dentro de SVG inline é **global no documento**. Com duas marcas na página, as duas desenham
`<linearGradient id="vb-frente">` e `fill="url(#vb-frente)"` resolve para **o primeiro** do documento.

Enquanto os dois estão visíveis, ninguém nota. Quando o primeiro mora numa subárvore com
`display: none` (a coluna do desktop, escondida no celular), o gradiente não é renderizado — e a
cópia visível (a da gaveta) pinta **nada**.

**Regra:** componente que desenha `<defs>` gera o id por instância (`useId()`), e o teste monta duas
cópias e confere que cada uma aponta para o próprio gradiente.

Achado em [[2026-10-02-pr-044-fix-gradiente-da-marca]].
