# Descrever a Infraestrutura como serviço (*Iaas*) 🏛
###### Fonte: https://learn.microsoft.com/pt-br/training/modules/describe-cloud-service-types/2-describe-infrastructure-service

O *IaaS* (infraestrutura como serviço) é a categoria mais flexível de serviços de nuvem, pois oferece o máximo de controle sobre os recursos de nuvem. Em um modelo de IaaS, o provedor de nuvem é responsável por manter o hardware, a conectividade de rede (com a Internet) e a segurança física. Você é responsável por todo o resto: instalação, configuração e manutenção do sistema operacional; configuração de rede; configuração de banco de dados e armazenamento e assim por diante. Com o IaaS, basicamente o hardware é alugado em um datacenter de nuvem, mas cabe a você decidir o que fazer com ele.

# Modelo de responsabilidade compartilhada

No IaaS, a maior parte da responsabilidade fica com você. O provedor de nuvem é responsável por manter a infraestrutura física e o acesso à Internet. Você é responsável por: instalação e configuração, aplicação de patch, atualizações e segurança.

<img src="https://learn.microsoft.com/pt-br/training/wwl-azure/describe-cloud-service-types/media/shared-responsibility-b3829bfe.svg">

# Cenários em que o *IaaS* faz sentido
* Migração lift-and-shift: você conta com recursos de nuvem semelhantes aos do datacenter local e apenas migra os elementos em execução local para execução na infraestrutura IaaS.
* Teste e desenvolvimento: você estabeleceu configurações para ambientes de desenvolvimento e teste que precisa replicar rapidamente. Você pode ativar ou desativar os diferentes ambientes rapidamente com uma estrutura de IaaS, mantendo o controle completo.

### ⏭ <a href="https://github.com/ofabiobatista/AZ-900/blob/main/PaaS.md"> Descrever a Plataforma como serviço 💻 </a>
