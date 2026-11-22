# MEMO v9 — Vinte fases e Desafio do Dia

Jogo de memória PWA, mobile-first, Chrome-first e offline-first, em JavaScript puro. Nenhuma dependência externa.

## Instalação no GitHub Pages

Copie **todos** os arquivos desta pasta, incluindo `assets/`, para a raiz do repositório. Em Settings → Pages, publique a branch `main`, pasta `/ (root)`. Abra em HTTPS. Após a primeira visita online, o service worker permite jogar offline.

## Campanha

São **20 fases sequenciais**, cada uma com tema próprio, pares de emojis, chefão, frase motivacional e relíquia. Não é possível pular fases. As fases 11 a 20 são: Bosque dos Sentidos, Oficina das Ideias, Museu do Tempo, Cozinha Criativa, Cidade Elétrica, Reino dos Enigmas, Safari Fantástico, Circuito Cósmico, Biblioteca Secreta e Trono das Lembranças. Cada fase tem entre 10 e 12 pares nessa segunda metade. O troféu supremo vem após vencer a fase 20.

## Nova inovação: Desafio do Dia

No menu, abra **📅 Desafio do Dia**. O tabuleiro é embaralhado de modo reproduzível a partir da data local do aparelho e usa a fase atualmente desbloqueada. O resultado diário fica registrado no navegador e pode ser melhorado repetindo o desafio. O modo diário **não desbloqueia novas fases nem concede relíquias de campanha**; os pontos obtidos entram no total geral. A data do aparelho determina o desafio; não há relógio de servidor nem ranking online.

## Pontuação e coleções

Ganhe pontos por pares, combos, rapidez e precisão. O total geral aparece no painel. O Hall permite revisitar fases vencidas. O Cofre reúne 20 relíquias e o Laboratório mostra estatísticas de jogo. Medalhas variam de bronze a diamante. Cartas especiais surgem nas fases avançadas.

## Música, vibração e acessibilidade

A trilha e os efeitos são sintetizados pela Web Audio API, sem arquivos externos. No Chrome, a vinheta do splash exige um toque para desbloquear o áudio. Vibrações dependem do suporte do dispositivo (`navigator.vibrate`). O menu permite ajustar volume e ativar/desativar vibração; o cabeçalho contém música, som, tema e tela cheia.

## Dados, atualização e backup

O progresso fica em `localStorage`. O MEMO v9 lê os dados anteriores, expande coleções e recordes para 20 fases e, se a décima fase já foi vencida, libera automaticamente a fase 11. Faça **Exportar conquistas** antes de atualizar e guarde o JSON em local seguro. **Restaurar conquistas** substitui os dados atuais; backups v7/v8 com dez fases continuam aceitos.

## Testes recomendados

No Chrome Android: confirmar o início automático pelo toque na carta, pontuação, áudio após interação, vibração, responsividade sem rolagem na tela de jogo, transição da fase 10 para a 11, conclusão da 20, Desafio do Dia, backup/restauração e funcionamento offline. O suporte a tela cheia e vibração varia conforme o navegador e o dispositivo.
