📌 Janela Modal com jQuery

Projeto de estudo desenvolvido para praticar a criação de uma janela modal interativa utilizando jQuery, com foco em eventos, manipulação do DOM e experiência do usuário.

🎯 Objetivo do Projeto

Este projeto tem como objetivo treinar:

Abertura e fechamento de modais
Manipulação de eventos com jQuery
Controle de propagação de eventos (stopPropagation)
Interação do usuário com a interface
Estruturação de formulários simples
🖥️ Demonstração

A aplicação consiste em:

Um botão "Entrar em contato"
Ao clicar, uma janela modal é exibida
A modal contém um formulário com campos:
Nome
Telefone
E-mail
A modal pode ser fechada ao clicar fora dela
⚙️ Tecnologias Utilizadas
HTML5
CSS3
jQuery
📁 Estrutura do Projeto
📦 projeto-modal-jquery
 ┣ 📂 css
 ┃ ┗ style.css
 ┣ 📂 js
 ┃ ┣ jquery.js
 ┃ ┗ functions.js
 ┗ index.html
🧠 Funcionamento do Código
🔹 Inicialização
$(function(){
Garante que o código será executado apenas quando o DOM estiver totalmente carregado.
🔹 Abrir Modal
$('.btn').click(function(e){
    e.stopPropagation();
    $('.bg').fadeIn();
});
Ao clicar no botão .btn, a modal (.bg) aparece com efeito fadeIn()
stopPropagation() evita que o clique seja interpretado pelo body
🔹 Fechar Modal
var el = $('body, .closeBtn');

el.click(function(){
    $('.bg').fadeOut();
});
Ao clicar fora da modal (ou em .closeBtn), ela é fechada com fadeOut()
🔹 Evitar Fechamento ao Clicar Dentro
$('.form').click(function(e){
    e.stopPropagation();
});
Impede que cliques dentro do formulário fechem a modal
🚀 Como Executar
Clone o repositório:
git clone https://github.com/seu-usuario/seu-repositorio.git
Acesse a pasta do projeto
Abra o arquivo index.html no navegador
💡 Melhorias Futuras

Algumas melhorias que podem elevar o projeto para nível profissional:

Adicionar botão de fechar (X)
Animações mais suaves com CSS
Validação de formulário
Responsividade para mobile
Acessibilidade (ARIA roles)
Fechar modal com tecla ESC
Transição com fade + scale
🧪 Possível Evolução

Transformar este projeto em:

Sistema de login modal
Captura de leads
Integração com API (envio de formulário)
Componente reutilizável
📚 Aprendizados

Com este projeto foi possível entender na prática:

Como funciona a propagação de eventos no JavaScript
Como controlar interações do usuário
Como criar componentes reutilizáveis com jQuery
📝 Licença

Este projeto é apenas para fins de estudo.
