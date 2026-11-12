# Facebook Reels: instruções para operar com Codex

Guia em português para configurar páginas, organizar vídeos, publicar e agendar Reels e manter o tracking. Reúne o procedimento de operação revisado em 12/11/2026, sem contas, páginas, vídeos ou dados de uma instalação real.

Este repositório contém **instruções e modelos**. O agente usa o controle de navegador disponível no Codex e uma instalação local com ledger persistente. Clonar este guia não instala um publicador independente nem cria uma agenda.

## Como usar

Abra este repositório no Codex e envie:

> Leia AGENTS.md e docs/onboarding.md. Quero configurar minhas páginas e operar meus Reels seguindo este guia. Faça as perguntas necessárias em blocos curtos, descubra as ferramentas disponíveis, prepare minha própria instalação e meu próprio registro e comece por uma página piloto autorizada. Use meus vídeos e os textos que eu aprovar. Depois do piloto, configure a rotina que eu pedir, sem duplicar posts ou agendamentos existentes. Explique qualquer recurso que ainda precise ser implementado no aplicativo escolhido.

O [Reels Codex Bot](https://github.com/pedroca001/reels-codex-bot) é uma implementação pública de referência com onboarding, painel local e SQLite. Sua versão inicial oferece publicação serial; os fluxos avançados deste guia, como agendamento nativo em paralelo, dependem de suporte efetivamente disponível no executor. Confira a documentação e os comandos daquela versão antes de instalar ou migrar.

## Ordem de leitura

1. [Contrato do agente](AGENTS.md).
2. [Instalação e perguntas de configuração](docs/onboarding.md).
3. [Autoconfig completo](docs/autoconfig.md).
4. [Pool e exclusividade dos vídeos](docs/pool.md).
5. [Páginas, horários e planejamento](docs/planejamento.md).
6. [Publicação e agendamento nativo](docs/postagem.md).
7. [Tracking e métricas](docs/tracking.md).
8. [Retomada e problemas conhecidos](docs/recuperacao.md).
9. [Prompt de rotina](templates/rotina.md).

O [modelo de configuração](examples/politica.example.json) contém placeholders. Ele não é uma configuração executável e não autoriza nenhuma página.

## Padrão de operação

- Duas postagens por dia, perto de 10h e 18h, no fuso escolhido. Uma terceira perto de 02h somente em páginas explicitamente aprovadas.
- Minutos variados, horários futuros e slots livres. Agendamentos existentes permanecem ocupados até reconciliação comprovada.
- Apenas páginas prontas e vídeos finais aprovados, com SHA e origem inéditos e áudio diferente por página/dia.
- Um grupo de página por vez. Até seis compositores da mesma página podem trabalhar em paralelo quando autorizados e suportados pelo executor.
- Acesso e administradores conferidos no autoconfig. Na postagem, conferir identidade ativa, prontidão registrada e recomendações.
- Métricas ficam em uma rotina separada sob demanda. Não atrasar postagem com uma coleta que não foi solicitada.
- Aceite, agendamento e publicação são estados diferentes. Conservar provas e histórico; nunca repetir uma ação de resultado incerto.

O operador escolhe e autoriza os valores durante o onboarding. Nenhuma conta, regra de país, legenda ou rotina da pessoa que criou este guia deve ser herdada automaticamente.

## Dados locais

Login permanece no Chrome do operador. Banco, mídia, configurações pessoais, relatórios e comprovantes ficam fora do Git. O dashboard público, quando solicitado, recebe somente a projeção aprovada dos dados.

Licença [MIT](LICENSE).
