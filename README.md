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
