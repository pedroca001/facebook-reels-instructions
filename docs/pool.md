# Pool de vídeos

## Inventário confiável

Usar apenas finais editados e aprovados. Sincronizar a pasta pelo inventariador da instalação antes de selecionar. Conferir disco conectado, erros e arquivos pendentes. Quantidade física de MP4 não é estoque livre.

Cada vídeo precisa de SHA256 do arquivo, origem identificada, grupo de áudio real, tipo (como receita ou avatar), caminho atual e estado. Recalcular SHA antes de transmitir. Não deduzir áudio pelo nome quando o nome não o identifica. Não criar origem fictícia para liberar exclusividade.

Excluir de novos envios os arquivos ou origens publicados, agendados, aceitos, reservados, em ação incerta, retirados para terceiros, usados em propostas vinculantes ou ainda em revisão. Cópia devolvida ao pool não desfaz vínculo anterior. Não mudar hash, nome ou origem para permitir repostagem.

## Pastas sugeridas

```text
pool/
  01_disponiveis/
  02_enviados/
    agendados/
    publicacao_a_confirmar/
  03_postados/
  04_a_conferir/
  05_fontes_preservadas/
```

Dentro de cada área, separar por tipo e depois por áudio, por exemplo receita/audio_01. Catálogo CSV e guia humano devem mostrar estado, página, horário, áudio, tipo, nome, SHA e caminho atual. Fontes e cópias preservadas não contam como novos finais.

Caminho pode mudar; SHA e vínculo original permanecem. Resolver o caminho pelo catálogo atual, não pelo caminho antigo congelado no plano. Movimentação rastreada exige preflight, prevenção de colisão, hash após transferência e registro persistido; não organizar em massa durante uploads ou gravações incertas.

## Distribuição dos áudios

Listar todos os grupos com finais elegíveis depois do sync. Cobrir os grupos antes de repetir quando houver páginas e estoque suficientes. Distribuir o restante uniformemente e desempatar pelo menor uso recente. Se houver mais grupos que páginas, priorizar os ainda não cobertos. Registrar limitações de estoque e a distribuição real.

Cada página usa áudios diferentes nos posts do mesmo dia. Não restringir a rodada a um subconjunto fixo quando grupos novos aprovados estiverem disponíveis. Prioridade de um lote específico só muda a seleção dos novos slots, nunca os arquivos já agendados.

## Saldo

Informar separadamente livres, reservados, agendados futuros, envios a confirmar, publicados e retirados. Horário vencido não transforma automaticamente agendamento em publicação nem libera a mídia para reenvio. Corrigir movimento pendente sem publicar outra vez.
