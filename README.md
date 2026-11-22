# MEMO — Jogo de Memória PWA (v3)

Jogo mobile-first, offline-first, feito com HTML, CSS e JavaScript nativo.

## Como jogar

Toque em duas cartas para descobrir pares. O primeiro toque inicia o cronômetro. Cada par rende 100 pontos, com bônus de 25 pontos por acertos consecutivos (até +125). Ao concluir a fase, você recebe bônus por tempo e precisão. A pontuação da partida aparece no painel em tempo real; o total acumulado fica em **Minhas conquistas**.

Dez fases sequenciais: só a próxima fase é liberada após vencer o chefão da fase atual. Não existe seletor de fases. Ao final de cada fase há uma cerimônia animada, uma mensagem motivacional e um botão para continuar. Na décima fase, há o troféu de Mestre da Memória.

## Áudio

Efeitos gerados localmente com Web Audio API, sem downloads de MP3 ou serviços externos. O botão 🔊 liga/desliga os sons. O navegador libera áudio após interação do usuário.

## Publicação

Envie os arquivos da raiz deste ZIP (incluindo `assets/`) para a raiz do repositório e ative **Settings → Pages → Deploy from a branch → main / (root)**. Acesse via HTTPS. Atualize a página após publicar para obter a versão nova do service worker.

## Armazenamento e offline

O jogo guarda progresso e recordes em localStorage. O service worker mantém arquivos essenciais em cache após o primeiro acesso online. Limpar dados do site pode apagar o progresso.

## Layout

A interface usa a altura visível (`100dvh`), painel compacto, tabuleiro de quatro colunas e barra inferior fixa na composição, sem rolagem da tela principal. Em telas muito pequenas, a altura das cartas é reduzida automaticamente. Janelas de informações podem rolar internamente.
