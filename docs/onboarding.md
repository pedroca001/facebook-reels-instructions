# Instalação e perguntas necessárias

## Descobrir o ambiente

Identificar sistema operacional, pasta de código, aplicativo existente, ferramenta CUA documentada, Chrome e perfil escolhido, diretório de mídia e diretório local dos dados. O usuário entra no Facebook pelo Chrome. Não pedir senha, cookie, token ou exportação de perfil.

Se o pedido for só ler o manual, não instalar nem publicar. Se for instalar, o [pacote de referência](https://github.com/pedroca001/reels-codex-bot) tem seu próprio AGENTS.md e docs/INSTALL_WITH_CODEX.md. Leia ambos antes de executar install.py, setup.py ou bot.py. Use o Python e os comandos da versão instalada. Não copiar runtime de outro computador nem executar setup sobre uma base existente para zerá-la.

## Perguntar em blocos curtos

| Bloco | Dados necessários |
|---|---|
| Destinos | Operador responsável, URLs/IDs das páginas, quais configurar e quais autoriza publicar; política de acesso exclusivo |
| Países e idade | Lista exata, ocultar ou mostrar, substituir lista ou acrescentar; idade mínima |
| Comentários e mensagens | Nome da regra, todas as keywords, tipo de correspondência, textos literais, quebras de linha, URL de destino e canais já disponíveis |
| Posts | Legenda completa, hashtags, público, tipos de vídeo e alterações de mídia permitidas |
| Mídia | Pasta aprovada, grupos de áudio, como identificar origem e quais vídeos têm prioridade |
| Rotação | Fuso, horários, minutos variados, quantidade por página, exceções, início de novas páginas, duração do lote e tratamento de sobras |
| Recuperação | O que fazer com recomendação suspensa, horário perdido, falta de estoque e gravação incerta |
| Tracking | Diretório do ledger e provas, painel, backups, métricas separadas e campos que podem aparecer em dashboard público |
| Execução | Piloto, autorização para upload e agendamento nativo, eventual paralelismo de até seis compositores da mesma página, interesse em rotina recorrente |

Não reapresentar perguntas já respondidas no chat ou na configuração local confiável. Mensagens e URLs comerciais devem ser fornecidas pelo novo operador; o manual não contém uma oferta predefinida.

## Antes da operação

Salvar um resumo local das respostas e vincular a autorização humana. Criar configuração própria com diretório de dados fora do repositório e ledger único. Confirmar que o app, o CLI e o agente apontam ao mesmo banco. Páginas começam pendentes.

Verificar instalação, FFmpeg quando necessário, leitura do disco, gravação do ledger e painel loopback. Nenhum teste local autoriza escrever no Facebook. Fazer o autoconfig de uma página e o piloto autorizado. Só ampliar aos demais destinos depois de conferir o resultado real.

Se o aplicativo escolhido só suporta publicação serial, operar serialmente até implementar e validar as guardas do fluxo avançado. Documentação não acrescenta métodos ao aplicativo. Não inventar comandos ou estados para simular suporte.

Uma rotina recorrente é uma configuração posterior ao piloto, pela ferramenta oficial disponível. A programação nativa da Meta funciona depois que o agendamento foi confirmado; novos uploads e monitoramento pelo agente dependem do computador e da sessão disponíveis.
