# Publicar e agendar pela UI

## Preparação por página

Conferir ambiente, disco, plano, ledger e cadastro. Acesso/ADM já confirmado no autoconfig não é relido a cada postagem. Ao entrar na página, observar recomendações e renovar prova de identidade ativa por ID. Não confiar apenas no nome ou asset_id.

Usar janela dedicada e as APIs CUA documentadas na sessão. Ler UI atual após ações e avançar pela prontidão observada. Labels neste guia são referências históricas e precisam corresponder aos controles atuais. Não usar estado oculto, rede privada ou um controlador alternativo como contorno.

## Um vídeo ou grupo paralelo

O caso simples usa um compositor. Quando o usuário autorizar e o executor suportar, usar de dois a seis compositores independentes da MESMA página. Congelar o grupo exato de SHA/slots e persistir autorização de upload e de commits paralelos.

Páginas diferentes e trocas de identidade são sequenciais. Não trocar perfil enquanto houver upload/commit em andamento. Aguardar todas as tarefas do grupo, inclusive em falha, sem promises ou executor UI em background. Falha exige inspecionar cada compositor; não executar o grupo inteiro novamente.

## Upload e preenchimento

1. Conferir ID ativo recente e destino Postar em. Recalcular hash e resolver caminho atual.
2. Persistir reserva/intenção de envio com página, slot, SHA, origem, horário e prova de identidade.
3. Criar reel e abrir o seletor documentado: registrar a espera do filechooser antes do clique em Adicionar vídeo; setFiles recebe o caminho absoluto autorizado.
4. Aguardar conclusão do upload e preencher a legenda literal e todas as hashtags. Não acrescentar música, story, grupo ou edição de mídia implicitamente.
5. Avançar pelos controles reais, conferir vídeo, autor e público. Usar texto/controle acessível observado; não confundir Turbinar com abrir detalhe.

Métricas não são coletadas nesta fase por padrão. Se uma instalação aprovar coleta simultânea, ela deve terminar e ser persistida antes do clique final, em aba da mesma página. O fluxo básico mantém a coleta separada.

## Agendamento nativo

Escolher Programar, selecionar data e conferir America/Sao_Paulo ou o fuso aprovado. Navegar no calendário pelos meses/anos reais, incluindo virada de ano; não codificar um mês fixo.

Campos de hora podem ser recriados a cada dígito. Selecionar o valor, enviar dígitos por press vinculado ao campo atual, End antes dos seguintes, Tab e validar aria-valuenow, data e fuso. Não depender de digitação sequencial quando ela perde foco. Corrigir campo no compositor existente sem reenviar arquivo.

Renovar ID ativo antes do clique final. Persistir intenção de commit e estado anterior. Clicar Programar uma única vez por item. Capturar aceite explícito Reel programado e encerrar o modal observado. Aceite é pending até a conferência da fila/detalhe.

Abrir a fila nativa da página correta. Localizar pela data/hora, autor, legenda e tipo; conferir público. Abrir detalhe e obter ID nativo e URL realmente oferecida. Fechar e aguardar o painel anterior desaparecer antes de outro item, evitando associar o CID anterior à linha seguinte. Detalhes são lidos serialmente mesmo após commits paralelos.

Se a UI ainda disser Processando, aguardar e voltar por leitura. Não repetir upload/Programar. Prévia indisponível explícita pode ser registrada como tal, desde que página, ID, horário, fuso, legenda e público tenham provas suficientes. Não inventar permalink a partir de um número interno.

## Publicação imediata

Só quando autorizada para aquele slot/destino. Público e legenda conferidos, intenção persistida e um único Compartilhar. Aceite Reel em processamento é intermediário e não soma publicado. Reconciliar conteúdo/insights/permalink externo. Nunca reenviar para acelerar processamento.

## Fechamento

Aplicar os critérios de docs/tracking.md. Somar separadamente enviados, aceitos, agendados confirmados, publicados e pendentes. Atualizar app, relatório e lista de horários com fuso. Guardar screenshot verificável do resultado. Encerrar worker local quando não for mais necessário, preservar aba produtiva e fechar somente auxiliares próprios desnecessários.
