# MEMO — Jogo de Memória PWA

MEMO é um jogo de memória **mobile-first**, **Chrome-first** e **offline-first**, desenvolvido em HTML, CSS e JavaScript puro, sem dependências externas.

## Como jogar

1. Toque em **Start** para começar a fase.
2. Vire duas cartas e encontre os emojis iguais.
3. Ganhe **100 pontos por par**, mais até **125 pontos adicionais** por combos consecutivos.
4. Ao terminar, receba bônus de rapidez e precisão. As dicas revelam um par por instantes, mas custam **50 pontos** cada (duas por fase).
5. Complete as **10 fases**, cada uma com seu próprio conjunto de emojis, e receba o troféu **Mestre da Memória**.

## Controles

- **Start**: começar, pausar, retomar ou preparar uma nova tentativa da fase concluída.
- **Reset**: reiniciar a tentativa atual, com confirmação.
- **Sobre**: regras e informações do jogo.
- **Menu**: jogar, escolher fases liberadas, consultar conquistas e instalar (quando o Chrome disponibilizar a opção).
- **Sol/Lua**: alternar temas claro e escuro.
- **Dica**: revela brevemente duas cartas iguais e desconta 50 pontos.

## Progressão

| Fase | Mundo | Pares |
|---|---|---:|
| 1 | Jardim encantado | 6 |
| 2 | Amigos da floresta | 6 |
| 3 | Doces sonhos | 7 |
| 4 | No fundo do mar | 7 |
| 5 | Céu de estrelas | 8 |
| 6 | Mundo mágico | 8 |
| 7 | Viagem pelo mundo | 9 |
| 8 | Festa da música | 9 |
| 9 | Galáxia neon | 10 |
| 10 | Lendas do MEMO | 10 |

## Publicar no GitHub Pages

1. Extraia o ZIP e envie **o conteúdo da pasta MEMO** para a raiz de um repositório GitHub, mantendo os caminhos e nomes dos arquivos.
2. No GitHub, abra **Settings → Pages**, selecione **Deploy from a branch**, escolha `main` e `/ (root)` e salve.
3. Aguarde a publicação e abra o endereço HTTPS do GitHub Pages.
4. Abra o jogo uma vez conectado à internet. O service worker armazenará os recursos essenciais para futuras visitas offline.

> O PWA requer HTTPS ou `localhost` para instalação e funcionamento do service worker. Abrir `index.html` diretamente como `file://` não habilita os recursos de PWA.

## Dados e privacidade

As fases liberadas, pontuação acumulada, recordes e preferência de tema são guardados localmente em `localStorage`. O aplicativo não possui servidor, contas, rastreadores nem bibliotecas externas. A limpeza dos dados do navegador pode apagar o progresso.

## Estrutura

```text
MEMO/
├── index.html
├── styles.css
├── app.js
├── manifest.webmanifest
├── sw.js
├── README.md
└── assets/
    ├── icon-192.png
    └── icon-512.png
```

## Atualizações

Ao publicar uma nova versão, atualize o identificador `CACHE` em `sw.js` para renovar os arquivos estáticos em dispositivos que já instalaram o aplicativo.


### Correção de interação
As cartas iniciam a partida no primeiro toque. A animação de virada utiliza elemento de bloco para funcionar no Chrome Android.
