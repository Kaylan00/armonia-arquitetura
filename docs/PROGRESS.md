# PROGRESS — Armonia Arquitetura

Site one-page de estúdio de arquitetura. Origem: HTML "bundled" (auto-desempacotável no browser) recebido do cliente, copiado fiel como `index.html`.

## 2026-06-30
- Criado projeto a partir do `Armonia Arquitetura - site.html` (bundle self-unpacking; `document.documentElement.replaceWith` injeta o template real).
- Ajustes (todos feitos editando o template dentro do bundle, backup em `index.html.bak`):
  - `zoom: 0.85` global no `<head>` do template (página estava parecendo com zoom alto).
  - Seção "O Estúdio": imagens com altura controlada `clamp(220px,24vw,310px)` + `align-items:center` (era `stretch`, ficava gigante).
  - Imagem do hero (21/9) removida (`display:none`).
  - Footer: sem cor de fundo própria (na cor do site), texto escuro, logo verde, borda fina no topo; voltou a ficar contido em 1600px.
  - Removida a faixa verde de números (15+/320+/18/4,9).
  - Loja: botão da sacola removido; botões "Adicionar" viraram "Pedir" -> link `wa.me/5528999087714` com nome do produto.
  - Serviços: "Projetos Comerciais" virou a 1ª opção (swap no `tabsRaw`).
  - Overlay de debug `[bundle] error` neutralizado (vai pro console em vez de renderizar na tela).
- Deploy: GitHub `Kaylan00/armonia-arquitetura` (branch master) + Vercel prod -> https://armonia-arquitetura.vercel.app (200, público).
- Adicionado como 2º card da seção "Alguns trabalhos" da proposta em portfolio-clientes (`proposta/tem-yyah`), substituindo o Nterio. Thumb: `armonia.jpg` 1200x900.

## Pendências
- 3 recursos externos do bundle não carregam (`[bundle]` no console) — não afeta render; investigar se necessário.
