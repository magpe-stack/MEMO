# MEMO v7 — Sinfonia da Memória

PWA mobile-first, Chrome-first, offline-first, sem bibliotecas externas.

## Como publicar

Envie todos os arquivos desta pasta para a raiz de um repositório GitHub e habilite **Settings → Pages → Deploy from a branch → main / (root)**. Abra a URL do GitHub Pages em HTTPS. O service worker mantém os recursos estáticos em cache após o primeiro carregamento.

## Jogabilidade

Dez fases sequenciais com emojis diferentes, pontuação por pares e combos, dicas, cronômetro, recordes e dez chefões. Cada vitória libera uma relíquia e uma medalha de bronze, prata, ouro ou diamante. As fases vencidas podem ser rejogadas pelo Hall da Memória; fases ainda não vencidas não podem ser escolhidas.

## Novidades v7

- Mascote expressivo 🧠, que reage aos acertos e erros.
- Cofre com dez relíquias; Hall com chefões, medalhas e opção de rejogar fases já vencidas.
- Laboratório com estatísticas do jogo e recordes; não é avaliação clínica.
- Modos Relâmpago (90 segundos) e Zen (sem cronômetro visível), desbloqueados após vencer a campanha.
- Na fase musical, acertos acrescentam pequenas notas originais.
- Cerimônia de chefão com relíquia, medalha, frase e efeitos sonoros.
- Exportação e restauração de backup JSON no menu. **Restaurar substitui o progresso atual.**

## Som e vibração

A música e os efeitos são gerados pela Web Audio API; a vibração usa `navigator.vibrate` onde houver suporte. O navegador precisa de um gesto do usuário para liberar áudio. Use os controles no cabeçalho e no menu.

## Armazenamento

O progresso fica no localStorage do navegador. Faça backups regulares; limpar os dados do site pode apagar as conquistas.

## Testes recomendados

Verificar Chrome Android: áudio após toque, vibração quando suportada, atualização offline, backup/restauração, cerimônias, desbloqueio sequencial, responsividade sem rolagem na tela principal e uso dos modos especiais.

## MEMO v8 — Vinheta e cartas especiais
- No splash de três segundos, toque em **♫ Ativar vinheta sonora** para ouvir a abertura. O Chrome exige uma interação do usuário antes de permitir áudio; a vinheta não pode ser garantida automaticamente.
- A partir da fase 7, alguns pares recebem uma marca dourada e bônus especiais: Espelho (+75), Gelo (+50) e Mistério (+100). Os pares continuam obedecendo às regras clássicas, sem alterar o número de cartas.
- Os dez chefões agora têm animações de derrota visualmente distintas.
- O cache offline foi atualizado para v8, preservando as chaves de progresso da v7.
