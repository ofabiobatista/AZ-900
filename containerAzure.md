# 2.2.3 Descrever contêineres do Azure
###### Fonte: https://learn.microsoft.com/pt-br/training/modules/describe-azure-compute-networking-services/5-containers

Embora as máquinas virtuais sejam uma excelente maneira de reduzir os custos em comparação com os investimentos necessários para o hardware físico, elas ainda estão limitadas a um sistema operacional por máquina virtual. Se você quer executar várias instâncias de um aplicativo em um só computador host, os contêineres são uma ótima opção.

# O que são contêineres?

Contêineres são um ambiente de virtualização. Diferentemente das máquinas virtuais, você não gerencia o sistema operacional para um contêiner. Os contêineres são leves e projetados para serem criados, dimensionados e interrompidos dinamicamente. Os contêineres foram projetados para permitir que você responda às alterações sob demanda.

# Instâncias de Contêiner do Azure

As Instâncias de Contêiner do Azure oferecem a maneira mais rápida e simples de executar um contêiner no Azure, sem a necessidade de gerenciar máquinas virtuais nem adotar serviços adicionais. Instâncias de Contêiner do Azure são uma oferta de PaaS (plataforma como serviço).

# Usar contêineres em suas soluções

Contêineres geralmente são usados para criar soluções que utilizam uma arquitetura de microsserviço. Essa arquitetura é onde você divide as soluções em partes menores e independentes. Por exemplo, você pode dividir um site em um contêiner que hospeda o front-end, outro que hospeda o back-end e um terceiro para o armazenamento. Essa divisão permite separar as partes do aplicativo em seções lógicas que podem ser mantidas, dimensionadas ou atualizadas de forma independente.
