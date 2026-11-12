# Tracking, comprovantes e métricas

## Ledger único

O aplicativo, CLI e agente acessam o mesmo ledger configurado. Planos e relatórios têm identidade de rodada e ficam fora do Git público. Antes de migração ou alteração de dados, backup SQLite consistente. Não editar o banco para simular sucesso.

Dados mínimos por item: página/ID, arquivo/SHA, origem, áudio, tipo, dia/slot, scheduled_at ou published_at com fuso, legenda, status, intenção de ação, timestamps reais e provas. Guardar caminho atual separado da proveniência original.

## Estados e critérios

| Estado conceitual | Critério | O que não permite |
|---|---|---|
| Planejado | Arquivo e slot escolhidos sem transmissão | Declarar envio |
| Reservado | Exclusividade persistida | Selecionar a mesma origem em outro item |
| Upload em curso | Intent e transmissão iniciados | Repetir arquivo por timeout |
| Commit iniciado | Intent antes de Programar/Compartilhar | Repetir clique sem reconciliar |
| Aceito, fila pendente | Aceite explícito da Meta salvo | Somar agendamento completo ou publicado |
| Processando | Aceite explícito de publicação, ainda sem receipt | Reenvio ou novo slot na mesma página sem resolução |
| Agendado confirmado | Fila/detalhe nativos com dados do item conferidos | Tratar como publicação pública ou renomear como postado |
| Publicado | Data externa, permalink, autor, público e legenda comprovados | Deduzir apenas porque passou do horário |
| Incerto/bloqueado | Resultado sem confirmação ou impedimento | Liberar mídia/slot para retry |

Os nomes concretos dependem do schema da instalação. O executor precisa ter guardas reais: não acrescentar strings de estado incompatíveis para fazer um relatório parecer concluído. Outras páginas só continuam após aceite e isolamento das pendências quando essa continuação for efetivamente suportada e autorizada.

Receipt de agendamento: ID ativo, SHA, autor, público, legenda, scheduled_at/fuso, horário da observação, ID nativo, URL observada ou indisponibilidade explícita e prova externa. Receipt público: mesmos vínculos, published_at externo e permalink real conferido. ID/URL de prévia podem mudar; confirmar novamente quando publicado.

Novas leituras/correções são append-only. Não sobrescrever prova original ou apagar observações para encobrir falha. Corrigir associação de CID por nova leitura do detalhe, nunca por novo envio. Não renomear/mover como publicado antes de receipt público; se só o movimento falhar, corrigir o catálogo sem repostar.

## Métricas separadas sob demanda

Coletar quando o operador pedir. Para todas as páginas e todos os vídeos, usar manifesto completo do tracking, incluindo arquivadas. Para um escopo menor, registrar o filtro explicitamente.

Exportação nativa do Business Suite pode ser usada quando disponível: Total acumulado, tipo Post, Data de criação e período cobrindo os envios. Conferir os IDs e o número real de páginas selecionadas; interfaces podem limitar o tamanho de cada lote. Guardar CSV bruto, hash, horário do pedido/download e fuso exibido. A tabela/insights pela UI é alternativa para IDs específicos.

Vincular por permalink/ID público ou por combinação única e comprovada de página/data/legenda/duração. Ambiguidade fica pendente. Meta pode omitir conteúdo recente mesmo que ele esteja publicado; ausência no CSV não comprova falha.

Salvar cada leitura com vídeo/página, observed_at ISO com fuso, fonte, evidência e chave de coleta. Preservar leituras anteriores. Visualizações e comentários exatos são o mínimo solicitado normalmente; valor arredondado ou ausente fica indisponível, nunca zero inventado. A leitura reflete o relatório recebido, que pode ter atraso.

## Dashboard e publicação na internet

Atualizar métricas não muda a rotação automaticamente. Ranking deve explicitar critério, amostra e cobertura, por exemplo média de views por Reel e comentários como desempate. Líderes só mudam com regra/autorização do operador.

Dashboard público recebe somente snapshot aprovado. Não publicar SQLite, nomes de administradores, mensagens privadas, caminhos locais, credenciais ou screenshots internos. Publicar por fluxo de deploy configurado e verificar a URL/versão real antes de dizer que está no ar. Uma reconstrução só de agenda preserva a data e as contagens da última coleta.
