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

## Novidades da versão 4

- Pontuação geral acumulada sempre visível no painel, além dos pontos da fase.
- Botão de tela cheia ao lado do tema (dependente do suporte e permissões do navegador).
- Efeitos sintetizados adicionais para botões, combos, impactos dos chefões, fanfarras e recordes de velocidade.
- Recordes de tempo por fase armazenados localmente.
- Nenhum arquivo de áudio externo é necessário.


## MEMO v5 — Jardim Sonoro

- Trilha musical original generativa, com cinco escalas e motivos que alternam entre fases.
- Botão ♫ no cabeçalho para desligar somente a música; 🔊 controla todos os sons.
- Efeitos para cartas, menus, tema, tela cheia, pausa, retomada, dicas, combos e supercombos.
- Sequências musicais especiais para chefões, impactos, derrota, recordes e troféu final.
- Áudio sintetizado localmente pela Web Audio API, sem arquivos MP3 nem rede.
- O Chrome exige um gesto do usuário antes de tocar áudio: a música começa quando a partida é iniciada.
- A trilha é interrompida ao pausar, abrir diálogos ou colocar a aba em segundo plano.


## MEMO v6 — Áudio e vibração
- Trilha sonora sintetizada audível também na tela inicial após o primeiro toque, com controle independente de música e efeitos.
- Volume ajustável no menu (40% a 250% do nível de referência), salvo no navegador.
- Vibrações distintas para cartas, pares, combos, erros, recordes e vitórias, quando `navigator.vibrate` é suportado.
- No Chrome Android, vibrações dependem de suporte do dispositivo, configurações do sistema e interação do usuário. Navegadores desktop e alguns aparelhos não vibram.
- Áudio exige um toque inicial por política do navegador.
