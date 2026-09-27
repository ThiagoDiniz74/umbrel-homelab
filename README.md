# Homelab com Umbrel

Documentação de um servidor pessoal usado para hospedar serviços em contêineres e praticar Linux, Docker, redes e observabilidade.

## Ambiente observado

- Disco do sistema: aproximadamente 223,6 GiB; nele estão os dados do Docker em `/var/lib/docker`.
- SSD secundário: aproximadamente 111,8 GiB, montado em `/mnt/ssd-secondary`.
- Serviços ativos na captura de 27/09/2026: CS2, Uptime Kuma, MySpeed, Pi-hole, Tor proxy, Beszel e Beszel Agent.
- O contêiner `cs2-server` tem política de reinício `unless-stopped` e montagens para instalação do jogo, Metamod, CounterStrikeSharp, CS2Retake e AstraSkins.

> A localização exata dos volumes persistentes de cada serviço ainda precisa ser conferida. Este repositório não contém dados de aplicativos ou configurações privadas.

## Serviços

| Serviço | Função |
| --- | --- |
| Uptime Kuma | Verificação da disponibilidade dos serviços. |
| Beszel e Beszel Agent | Métricas e acompanhamento do servidor. |
| MySpeed | Medição e histórico de velocidade da conexão. |
| Pi-hole | Filtragem de DNS na rede local. |
| Tor proxy | Serviço auxiliar do ambiente Umbrel. |
| CS2 | Servidor de jogo documentado em projeto separado. |

## O que este projeto demonstra

- Administração de contêineres Docker no Umbrel.
- Separação entre o disco do sistema e o SSD secundário.
- Monitoramento de disponibilidade e métricas.
- Documentação da infraestrutura sem publicar credenciais, endereços externos ou dados persistentes.

## Próximas etapas

- Registrar a arquitetura dos volumes e as políticas de reinício após verificar os metadados dos contêineres.
- Adicionar um diagrama da rede sem endereços reais.
- Documentar backup e restauração após confirmar os procedimentos usados.

## Segurança

Não publique arquivos `.env`, bancos de dados, tokens, webhooks, senhas, chaves privadas, backups nem saídas integrais de `docker inspect`. Consulte `SEGURANCA.md` antes de cada commit.
