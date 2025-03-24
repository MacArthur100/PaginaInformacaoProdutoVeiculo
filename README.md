Exercício de Prática de Desing 2º semestre Sistemas para Internet - FATEC 

Aqui está a explicação linha por linha do código:
________________________________________
1. Definição do tipo de documento
<!DOCTYPE html>
•	Declara que este é um documento HTML5.
________________________________________
2. Abertura da tag HTML e definição do idioma
<html lang="pt-BR">
•	Indica que o documento está escrito em português do Brasil.
________________________________________
3. Cabeçalho do documento (<head>)
<head>
•	Contém metadados e configurações do documento.
________________________________________
4. Definição de caracteres
<meta charset="UTF-8">
•	Define a codificação de caracteres como UTF-8, permitindo acentos e caracteres especiais.
________________________________________
5. Configuração da exibição em dispositivos móveis
<meta name="viewport" content="width=device-width, initial-scale=1.0">
•	Ajusta a largura da página para se adaptar ao tamanho da tela do dispositivo.
________________________________________
6. Definição do título da página
<title>Veículo - Detalhes</title>
•	Define o título exibido na aba do navegador.
________________________________________
7. Título principal da página
<h1>CHEVROLET TRAX - 2025</h1>
•	Exibe um título grande no topo da página.
________________________________________
8. Estilos CSS
<style>
•	Início da seção de estilos.
________________________________________
9. Estilização do corpo (<body>)
body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}
•	Define a fonte como Arial.
•	Centraliza o conteúdo.
•	Remove margens e preenchimentos padrão.
•	Define um fundo cinza claro.
________________________________________
10. Container do veículo
.vehicle-container {
    position: relative;
    margin-top: 50px;
}
•	Define um contêiner com position: relative para posicionamento dos elementos dentro dele.
•	Adiciona uma margem superior de 50 pixels.
________________________________________
11. Estilização da imagem do veículo
.vehicle-image {
    width: 60%;
    opacity: 0;
    animation: slideIn 2s forwards;
}
•	Define que a imagem ocupará 60% da largura da tela.
•	Começa invisível (opacity: 0).
•	Usa a animação slideIn para aparecer deslizando.
________________________________________
12. Estilização da descrição
.description {
    font-size: 1.2rem;
    margin-top: 20px;
    opacity: 0;
    animation: fadeIn 2s 2s forwards;
}
•	Define o tamanho da fonte.
•	Adiciona uma margem superior.
•	Inicialmente invisível (opacity: 0).
•	Usa a animação fadeIn para aparecer 2 segundos após a imagem.
________________________________________
13. Animação para deslizar a imagem
@keyframes slideIn {
    0% {
        transform: translateX(-100%);
        opacity: 0;
    }
    100% {
        transform: translateX(0);
        opacity: 1;
    }
}
•	Move a imagem da esquerda para a posição inicial.
•	Faz a imagem aparecer gradualmente.
________________________________________
14. Animação para exibir a descrição
@keyframes fadeIn {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}
•	Aumenta a opacidade de 0 para 1 (efeito de fade-in).
________________________________________
15. Estilização do contêiner dos botões
.button-container {
    margin-top: 30px;
}
•	Adiciona espaçamento acima dos botões.
________________________________________
16. Estilização dos botões
button {
    padding: 10px 20px;
    font-size: 1rem;
    margin: 10px;
    cursor: pointer;
    border: none;
    background-color: #4CAF50;
    color: white;
    border-radius: 5px;
    transition: background-color 0.3s;
}
•	Adiciona preenchimento para tornar o botão maior.
•	Define o tamanho da fonte.
•	Remove a borda.
•	Define a cor verde como fundo.
•	Faz a transição de cor suave ao passar o mouse.
________________________________________
17. Mudança de cor ao passar o mouse
button:hover {
    background-color: blue;
}
•	Altera a cor para azul quando o cursor estiver sobre o botão.
________________________________________
18. Classe oculta (hidden)
.hidden {
    display: none;
}
•	Esconde elementos que não devem aparecer inicialmente.
________________________________________
19. Estilização da área de informações extras
.extra-info {
    margin-top: 20px;
    font-size: 1.1rem;
}
•	Adiciona espaçamento superior e define o tamanho da fonte.
________________________________________
20. Estilização das imagens extras
.extra-info img {
    width: 50%;
    margin-top: 20px;
    display: block;
    margin-left: auto;
    margin-right: auto;
}
•	Define a largura como 50% da tela.
•	Centraliza horizontalmente.
________________________________________
21. Fechamento do <head>
</head>
•	Finaliza a seção de cabeçalho.
________________________________________
22. Corpo da página (<body>)
<body>
•	Inicia a parte visível da página.
________________________________________
23. Contêiner do veículo
<div class="vehicle-container">
•	Agrupa a imagem e a descrição do veículo.
________________________________________
24. Imagem do veículo
<img id="vehicle-image" class="vehicle-image" src="IMG/download png.png" alt="Veículo">
•	Adiciona uma imagem com ID vehicle-image.
________________________________________
25. Descrição do veículo
<div id="vehicle-description" class="description">
•	Cria um bloco de texto com informações sobre o veículo.
________________________________________
26. Botões de informações
<div class="button-container">
    <button onclick="showExtraInfo(1)">Saiba mais - Segurança</button>
    <button onclick="showExtraInfo(2)">Saiba mais - Economia</button>
    <button onclick="showExtraInfo(3)">Saiba mais - Design</button>
</div>
•	Três botões que, ao serem clicados, chamam a função showExtraInfo().
________________________________________
27. Informações adicionais escondidas
<div id="extra-info-1" class="extra-info hidden">
•	Parágrafo e imagem escondidos inicialmente.
•	Exibidos quando o botão correspondente é clicado.
________________________________________
28. Script JavaScript
<script>
•	Início da programação JavaScript.
________________________________________
29. Função showExtraInfo
function showExtraInfo(infoType) {
    document.getElementById('extra-info-1').classList.add('hidden');
    document.getElementById('extra-info-2').classList.add('hidden');
    document.getElementById('extra-info-3').classList.add('hidden');
•	Esconde todas as seções de informações extras.
________________________________________
30. Exibe a informação escolhida
if (infoType === 1) {
    document.getElementById('extra-info-1').classList.remove('hidden');
} else if (infoType === 2) {
    document.getElementById('extra-info-2').classList.remove('hidden');
} else if (infoType === 3) {
    document.getElementById('extra-info-3').classList.remove('hidden');
}
•	Mostra apenas a informação correspondente ao botão clicado.
________________________________________
31. Fechamento das tags
</script>
</body>
</html>
•	Finaliza o script e o documento.
________________________________________
Esse código cria uma página interativa onde um carro aparece com animação e informações extras são exibidas ao clicar nos botões.

