# Páginas e horários

Ler relógio real e converter para o fuso configurado, preferencialmente America/Sao_Paulo quando aprovado. Não deduzir o horário local pelo UTC do disparo.

## Política proposta

| Slot estável | Horário nominal | Destinos |
|---|---|---|
| 1 | 02h | Somente páginas com terceira postagem explicitamente aprovada |
| 2 | 10h | Todas as páginas prontas autorizadas |
| 3 | 18h | Todas as páginas prontas autorizadas |

Variar os minutos dentro da faixa aprovada, por exemplo de 06 a 40 minutos depois do horário nominal. Persistir o horário sorteado uma vez no plano e reutilizá-lo na retomada. Essa faixa é uma proposta, não um valor obrigatório para todo operador.

Duas postagens/dia não significa slots1/2: o padrão acima usa slots2/3. Manter IDs estáveis no banco. Exceções são uma lista explícita de páginas; não mudar as líderes automaticamente após nova coleta.

## Selecionar destinos

Consultar cadastro atual: entra apenas page_ready=true, sem pausa/arquivo/impedimento, e com slot já autorizado pela data de entrada. Página pronta que só começa às10h não entra retroativamente às02h. Não ativar candidatas para preencher quota.

Antes de novos arquivos, consultar intents, aceites, receipts, reprogramações e horários nativos existentes. Um slot com efeito incerto continua ocupado. Reprogramações usam o dia/slot efetivos e preservam os originais no histórico.

## Montar lote

1. Definir páginas, quantidade, dias, slots e tratamento de sobras conforme pedido.
2. Encontrar os próximos horários futuros livres por página, respeitando a frequência e o tempo mínimo exigido pela interface nativa.
3. Garantir estoque suficiente e áudios distintos por página/dia.
4. Congelar plano com índice, página, dia/slot, scheduled_at com fuso, SHA, origem, áudio, tipo, caminho e legenda aprovada.
5. Reservar exclusivamente e registrar a autorização do grupo exato antes do envio.

Não preencher buracos do passado ou aumentar frequência sem ordem específica. Se houver sobras e nenhuma regra aprovada para elas, apresentar a proposta ou perguntar enquanto prepara a parte independente. Lote parcial precisa ser identificado, nunca apresentado como cobertura completa.

Uma estimativa de N dias completos é limitada pela demanda diária e pelas restrições de áudio, prontidão e agenda, não só pela divisão de arquivos. Com P páginas e L delas com terceira postagem, demanda diária = 2P + L.

## Rotina do agente e agenda nativa

O agendador do Codex desperta o agente. O botão Programar da Meta cria um compromisso nativo. Não são a mesma agenda. Quando já existe intent/agendamento para o slot, a rotina apenas reconcilia; não envia outro Reel.

Criar/alterar automação somente pelo recurso oficial disponível e por pedido humano. Preservar estado pausado. Validar fuso, próximo disparo e primeiro disparo real. Computador indisponível ou heartbeat atrasado não autoriza compensar horário perdido. Notificar falha acionável; ficar em silêncio quando nada mudou.
