# Check de Estúdio

Ferramenta web para professores que gravam aula em casa. Abre a câmera e o microfone do aparelho e sugere ajustes de:

- **Enquadramento:** espaço acima da cabeça, distância da câmera, centralização e câmera torta.
- **Iluminação:** cena escura ou clara demais, contraluz, luz estourando e luz forte de um lado só.
- **Fundo:** poluição visual e objetos logo atrás da cabeça.
- **Microfone:** teste guiado de cerca de 25 segundos (ruído, nível da voz, distorção, zumbido, eco e agudos).

A imagem e o áudio não saem do aparelho. A análise acontece no navegador.

## Como usar

Abra o endereço da página no Chrome, Edge ou Safari e permita câmera e microfone. A câmera só é liberada em páginas HTTPS (como o GitHub Pages) ou abertas direto no computador. Não funciona dentro de iframes nem de navegadores embutidos (WhatsApp, Instagram).

## Ajustes

É um único arquivo, `index.html`, sem dependências para instalar. Os limites usados para avaliar câmera e microfone estão nos objetos `CAM` e `MIC`, no início do script. São valores heurísticos, vale calibrar com gravações reais.

O detector de rosto (MediaPipe) é baixado de uma CDN na hora. Sem internet, a análise de luz, fundo e alinhamento continua, mas as dicas de posição do rosto ficam desligadas.
