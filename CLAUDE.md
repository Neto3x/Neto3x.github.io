Por padrão, crie todas as páginas web e Landing Pages incorporando uma Seção Hero Interativa com animação baseada em Scroll (Scroll-Driven Storytelling). 

Siga estritamente estas diretrizes de desenvolvimento:

1. Bibliotecas e Dependências:
   - Inclua os scripts da CDN do GSAP (GreenSock) e do plugin ScrollTrigger em todas as páginas.
   - Use CSS moderno / Tailwind CSS para estilização fluida e responsiva.

2. Estrutura da Seção Hero (Hero Pinning):
   - A introdução do site deve ocupar a primeira seção (`min-h-screen` / `100vh`).
   - Trave a seção na tela usando `pin: true` no ScrollTrigger para que o usuário permaneça na seção enquanto rola a página.
   - A animação das camadas visuais do produto/elemento principal deve ser sincronizada com o progresso do scroll (`scrub: true` ou `scrub: 1` para inércia suave).

3. Compatibilidade Mobile & Touch:
   - Garanta compatibilidade total com dispositivos móveis (iOS e Android), assegurando que o gesto de rolagem com o polegar sincronize suavemente a animação sem sobressaltos (*jank*).
   - Otimize o desempenho usando `will-change: transform` e aceleração via GPU (`transform: translate3d`) em elementos animados.

4. Transição Fluida para o Resto do Site:
   - Após a conclusão da animação de introdução (ex: quando as camadas se juntam ou se desfazem), o pin do ScrollTrigger deve ser liberado, permitindo que a rolagem flua normalmente para as seções de conteúdo do site.

Entregue sempre o código HTML/JS/CSS completo, funcional e com comentários claros indicando como substituir os assets (imagens e textos) para o elemento principal da animação.
