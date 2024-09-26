# Front-end Style Guide

## Layout

The designs were created to the following widths:

- Mobile: 375px
- Desktop: 1440px

> 💡 These are just the design sizes. Ensure content is responsive and meets WCAG requirements by testing the full range of screen sizes from 320px to large screens.

## Colors

- Green: hsl(75, 94%, 57%)

- White: hsl(0, 0%, 100%)

- Grey 700: hsl(0, 0%, 20%)
- Grey 800: hsl(0, 0%, 12%)
- Grey 900: hsl(0, 0%, 8%)

## Typography

### Body Copy

- Font size (paragraph): 14px

### Font

- Family: [Inter](https://fonts.google.com/specimen/Inter)
- Weights: 400, 600, 700

> 💎 [Upgrade to Pro](https://www.frontendmentor.io/pro?ref=style-guide) for design file access to see all design details and get hands-on experience using a professional workflow with tools like Figma. The design file for this challenge also includes a basic design system to help you build a more accurate solution faster.

<!-- @import url("http://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap");

/* Reseta as margens e o preenchimento de todos os elementos */
*,
*::before,
*::after {
  margin: 0; /*remove a margem padrao*/
  padding: 0; /* remove o preenchimento padrao*/
  box-sizing: border-box; /*inclui bordas e preenchimentos no calculo da largura e altura dos elementos*/
}

/* Definições de variáveis CSS para cores e pesos de fonte */
:root {
  --clr-green: hsl(75, 94%, 57%); /*verde*/
  --clr-white: hsl(0, 0%, 100%); /*branco*/
  --clr-grey-700: hsl(0, 0%, 22%); /*cinza escuro */
  --clr-grey-dark-800: hsl(0, 0%, 14%); /*cinza ainda mais escuro*/
  --clr-black-off-900: hsl(0, 33%, 1%); /*preto quase absoluto*/
  --fw-normal: 400; /*peso do fundo normal */
  --fw-semi-bold: 600; /*peso da fonte semi-negrito*/
  --fw-bold: 700; /*peso da fonte negrito*/
}

/* Define o tamanho da fonte base para o documento */
html {
  font-size: 62.5%; /* reduz o tamanho padrao de fonte para 10px, facilitando o uso do rem*/
}

/* Estilo do corpo da página */
body {
  font-family: "Inter", sans-serif; /*define a fonte do corpo*/
  font-size: 1.4rem; /*define o tamanho da fonte do corpo com 1.4rem a fonte bade 10px*/
  font-weight: var(--fw-normal);
  /*define o peso da fonte usando a variavel definida anteriormente*/
  background-color: var(--clr-black-off-900); /*define a cor do fundo do corpo*/
  min-height: 100vh; /*garante que o corpo ocupe no minimo a altura toral da viewport*/
  display: grid; /*ultiliza o modelo do grid css*/
  place-content: center; /*centraliza o conteudo no grid*/
}

/* Estilo para listas não ordenadas */
ul {
  list-style: none; /*remover os marcadores da lista*/
}

/* Estilo para links */
a {
  display: block; /*faz com que o link ocupe toda a largura disponivel*/
  text-decoration: none; /*remove p sublinhado padrao dos links*/
}

/* Estilo para um contêiner genérico */
.container {
  padding-inline: 15rem; /*adicionar o preenchimento nas lateriais (esqueda e direita)*/
  margin: 9rem auto 0; /*define margens para container*/
}

/* Estilo para o perfil */
.profile {
  background-color: var(--clr-grey-dark-800);
  /*define a cor de fundo do perfil*/
  width: 40rem; /*define uma largura fixa para o perfil*/
  padding: 1.8rem; /*adicionar preenchimento interno*/
  border-radius: 0.8rem; /*arredonda os cantos*/
  text-align: center; /* centraliza o texto dentro do perfil*/
}

/* Estilo para a imagem do perfil */
.profile .profile-img {
  width: 9rem; /*define uma largura fixa para a imagem*/
  aspect-ratio: 1; /*mantem a proporção 1:1 (quadrado)*/
  margin: 0 auto; /*centraliza a imagem horizontalmente*/
}

/* Estilo para a imagem dentro do perfil */
.profile .profile-img img {
  display: inherit; /*herdar o comportamento do elemento pai*/
  max-width: 100%; /*garante que a img nao ultrapasse a largura do elemnto pai*/
  border-radius: 50%; /*faz a imagem ficar circular*/
}

/* Estilo para o título do perfil */
.profile .profile-title {
  margin-top: 3rem; /*adicina margem superior titulo*/
}

/* Estilo para o h1 do título do perfil */
.profile .profile-title h1 {
  color: var(--clr-white); /*definme a cor do texto como branco */
  font-size: 2.3rem; /*define o tamanho da fonte pata titulo*/
  font-weight: var(--fw-bold); /*usa peso de fonte negrito*/
}

/* Estilo para o h2 do título do perfil */
.profile .profile-title h2 {
  color: var(--clr-green); /*define a cor do texto como verde*/
  font-size: 1.4rem; /*define o tamanho da fonte para subtitulo*/
  margin-top: 1rem; /*margem superioe*/
  margin-bottom: 3rem; /*margem inferior*/
}

/* Estilo para parágrafos no cabeçalho do perfil */
.profile .profile-header p {
  color: var(--clr-white); /*define a cor do texto como branco*/
}

/* Estilo para a seção de mídias sociais */
.profile .social-media {
  display: flex; /*ultiliza o modelo flexbox*/
  flex-direction: column; /* alinha os itens verticalmente*/
  align-items: center; /*alinha os itens horizontalmente*/
  margin-top: 3rem; /* adicionar margem superior*/
}

/* Estilo para os itens da lista de mídias sociais */
.profile .social-media li {
  width: 100%; /*faz com que os itens ocupem toda a largura disponivel*/
}

/* Estilo para os links dentro da lista de mídias sociais */
.profile .social-media li a {
  background-color: var(--clr-grey-700); /* define a cor de fundo do link*/
  color: var(--clr-white); /*define a cor do texto como branco */
  padding: 1.6rem 0; /*adicionar preenchimento vertical*/
  border-radius: 1rem; /*adicionar os cantos */
  margin-bottom: 2rem; /*adicionar margme inferior*/
  font-weight: var(--fw-semi-bold);
  /*define o peso da fonte como semi-negrito*/
  transition: all 0.3s ease-in-out; /*adicionar uma transição suave para as propriedades*/
}

/*efeito ao passar o mouse sobre os links de midias sociais*/
.profile .social-media li:hover a {
  background-color: var(--clr-green);
  /*mudar a cor de fundo para verde ao passar o mouse*/
  color: var(--clr-black-off-900);
  /* mudar a cor do texto para preto ao passar o mouse*/
} -->
