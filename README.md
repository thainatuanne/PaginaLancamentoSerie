# Projeto: O Senhor dos Anéis: Os Anéis do Poder

## Descrição
Este projeto é uma página interativa que apresenta informações detalhadas sobre a série **"O Senhor dos Anéis: Os Anéis do Poder"**, disponível no Prime Video. A página inclui uma sinopse, um trailer oficial, uma lista de elenco, personagens principais, e um link para assistir à série. O layout é enriquecido com animações em CSS para criar uma experiência visual imersiva para o usuário.

## Funcionalidades
- **Poster de entrada**: Exibição de uma imagem inicial que aparece ao carregar a página, com um botão para fechar e iniciar a navegação na página.
- **Menu de navegação**: Links que facilitam a navegação entre as seções da página.
- **Trailer oficial**: Um vídeo incorporado com animações sutis para destacar o conteúdo.
- **Elenco e Personagens**: Listas informativas sobre os atores e seus personagens, com destaque interativo.
- **Animações em CSS**: Uso de keyframes para criar efeitos visuais que melhoram a experiência do usuário.

## Tecnologias Utilizadas
- **HTML5**: Estrutura semântica para melhor acessibilidade e SEO.
- **CSS3**: Estilização da página, animações e design responsivo.
- **JavaScript**: Para manipulação de eventos, como a exibição do pôster e a ativação de animações no logo.

## Animações Utilizadas
### Explicação de Keyframes
- **`@keyframes posterFadeIn`**: Animação para exibir o pôster de entrada com um efeito de fade-in, tornando a entrada inicial da página mais envolvente ao aparecer de forma gradual.
- **`@keyframes posterFadeOut`**: Utilizada para ocultar o pôster de entrada com um efeito de fade-out suave, garantindo uma transição fluida quando o usuário fecha o pôster.
- **`@keyframes fadeInMoveDown`**: Animação aplicada ao logo da Prime Video para que ele apareça suavemente na página com um leve movimento descendente, criando uma transição visual atraente.
- **`@keyframes titleZoom`**: Uma animação de zoom aplicada ao título principal da página, gerando um efeito pulsante que chama a atenção do usuário de forma sutil.
- **`@keyframes scalePulse`**: Animação aplicada aos elementos de vídeo, criando um efeito de pulsação que enfatiza a importância do conteúdo visual.
- **`@keyframes pulseGlow`**: Adiciona um brilho pulsante em torno das bordas de elementos como o vídeo, atraindo a atenção de forma suave.
- **`@keyframes characterHighlight`**: Animação que faz com que as imagens dos personagens aumentem de escala e recebam uma sombra luminosa ao serem destacadas, criando um efeito de realce.
- **`@keyframes glow`**: Efeito de brilho intermitente aplicado aos links do rodapé para incentivar a interação.
- **`@keyframes characterFloat`**: Animação que faz a imagem de um personagem flutuar suavemente de um lado para o outro, adicionando dinamismo à página.

## JavaScript Utilizado
O JavaScript foi utilizado para manipular a exibição do pôster de entrada e ativar a animação do logo da Prime Video após o fechamento do pôster.

### Explicação do Código
```javascript
function closePoster() {
    const poster = document.getElementById('poster');
    const logo = document.querySelector('.header__logo');

    // Adiciona a animação de fade-out ao pôster
    poster.style.animation = 'posterFadeOut 1s ease';
    setTimeout(() => {
        // Oculta o pôster após a animação
        poster.style.display = 'none';
        // Adiciona a classe para iniciar a animação do logo
        logo.classList.add('logo-visible');
    }, 1000); // Tempo da duração da animação
}
