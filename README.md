# Site Pessoal — Arthur Gomes de Jesus

Site pessoal/portfólio desenvolvido na disciplina de **Desenvolvimento Front-end para Web** do curso de **Análise e Desenvolvimento de Sistemas** do Centro Universitário Braz Cubas.

🔗 **Site publicado:** https://devarthur-cyber.github.io/meu-portfolio-cp4/
📦 **Versão de entrega:** tag `cp4-entrega`

---

## Páginas

| Página | Arquivo | Conteúdo |
|--------|---------|----------|
| Início | `index.html` | Apresentação, sobre mim e resumo de interesses |
| Currículo | `curriculo.html` | Formação, projetos, habilidades técnicas e informações adicionais |
| Contato | `formulario.html` | Formulário com validação em JavaScript e rascunho salvo |
| Multimídia | `multimidia.html` | Vídeo, áudio e conteúdo incorporado (iframe) |
| Gráficos | `graficos.html` | Animação em `<canvas>` e ícone em SVG estilizado com CSS |

## Funcionalidades em JavaScript

Todas ficam em `js/scripts.js`, sem bibliotecas externas.

- **Tema claro/escuro** — o botão alterna o tema e a escolha é salva no `localStorage` (chave `arthur:tema`), sobrevivendo ao F5 e valendo em todas as páginas.
- **Rascunho do formulário** — o que o visitante digita no formulário é salvo no `localStorage` (chave `arthur:rascunho`) e restaurado ao recarregar, com opção de descartar.
- **Validação do formulário** — mensagens de erro exibidas abaixo de cada campo e aviso de status ao enviar.
- **Saudação personalizada** — o site pergunta o nome do visitante e o guarda no navegador.
- **Animação em canvas** — rede de nós conectados desenhada ponto a ponto.

## Tecnologias

- HTML5 semântico
- CSS3 (variáveis, Flexbox, Grid, mobile-first com `@media`)
- JavaScript (ES6+)
- [Bootstrap 5.3.3](https://getbootstrap.com/) via CDN
- Git e GitHub Pages (HTTPS)

## Bootstrap

O Bootstrap é carregado antes do `css/estilos.css`, que complementa o visual. Classes usadas:

- `row`, `g-3`, `col-12`, `col-md-6`, `col-xl-4` e `h-100` — grade responsiva dos cartões de projetos (`curriculo.html`)
- `table-responsive` — tabela de habilidades com rolagem em telas pequenas (`curriculo.html`)
- `ratio` e `ratio-16x9` — proporção do vídeo incorporado (`multimidia.html`)
- `visually-hidden-focusable` — link "Pular para o conteúdo", visível apenas ao receber foco (todas as páginas)

A classe própria `.card` foi renomeada para `.painel` para não conflitar com a `.card` do Bootstrap.

## Acessibilidade

- Atributo `lang="pt-br"` e `viewport` em todas as páginas
- Texto alternativo (`alt`) na foto; `aria-label` no canvas e no SVG
- Link "Pular para o conteúdo" para navegação por teclado
- Foco visível (`:focus-visible`) em links, botões e campos
- Todos os campos do formulário com `label` associado e erros ligados por `aria-describedby`; status do envio com `aria-live`
- Menu identificado com `aria-label` e página atual com `aria-current`
- Contraste do texto principal acima de 14:1 nos dois temas
- Respeito à preferência `prefers-reduced-motion`

## Estrutura do projeto

```
meu-portfolio-cp4/
├── index.html
├── curriculo.html
├── formulario.html
├── multimidia.html
├── graficos.html
├── css/
│   └── estilos.css
├── js/
│   └── scripts.js
├── img/
│   ├── foto-arthur.jpg
│   └── avatar.svg
├── .gitignore
└── README.md
```

## Evolução do projeto

- **CP1 e CP2** — estrutura em HTML e estilização em CSS do site pessoal.
- **CP3** — versionamento com Git, publicação com HTTPS, interatividade em JavaScript, formulário com validação e uso do `localStorage`.
- **CP4** — integração do Bootstrap, ajustes finais de acessibilidade, foto de perfil, versão consolidada e vídeo de apresentação.

## Como executar localmente

1. Clone o repositório:
   ```bash
   git clone https://github.com/devarthur-cyber/meu-portfolio-cp4.git
   ```
2. Abra o `index.html` no navegador (ou use a extensão Live Server do VS Code).
3. É necessária conexão com a internet para carregar o Bootstrap, os vídeos e as fontes externas.

## Autor

**Arthur Gomes de Jesus**
Estudante de Análise e Desenvolvimento de Sistemas — Centro Universitário Braz Cubas
GitHub: [@devarthur-cyber](https://github.com/devarthur-cyber)
