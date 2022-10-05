# 2.2.1 Descrever Máquinas Virtuais do Azure
###### Fonte: https://learn.microsoft.com/pt-br/training/modules/describe-azure-compute-networking-services/2-virtual-machines

As VMs fornecem IaaS (infraestrutura como serviço) na forma de um servidor virtualizado e como em um computador físico, você pode personalizar todos os programas de software em execução. As VMs são uma opção ideal quando você precisa de:

* Controle total sobre o SO (sistema operacional).
* Capacidade para executar um software personalizado.
* Usar configurações personalizadas de hospedagem.

Uma VM do Azure oferece a flexibilidade da virtualização sem a necessidade de comprar e manter o hardware físico que a executa. No entanto, como uma oferta de *IaaS*, você ainda precisa configurar, atualizar e manter o software executado na VM.

# Dimensionar VMs no Azure

Você pode executar VMs únicas para teste, desenvolvimento ou para tarefas secundárias. Ou pode agrupar VMs para fornecer alta disponibilidade, escalabilidade e redundância. O Azure também pode gerenciar o agrupamento de VMs para você com recursos como conjuntos de dimensionamento e conjuntos de disponibilidade.

# Conjuntos de escala de máquina virtual

Os Conjuntos de Dimensionamento de Máquinas Virtuais permitem criar e gerenciar um grupo de VMs idênticas e com balanceamento de carga. Os conjuntos de dimensionamento permitem que você gerencie, configure e atualize centralmente um grande número de VMs em minutos. O número de instâncias de VM pode aumentar ou diminuir automaticamente em resposta à demanda ou você pode defini-lo para uma escala com base em uma agenda definida. Os conjuntos de dimensionamento de máquinas virtuais também implantam automaticamente um balanceador de carga para garantir que seus recursos estejam sendo usados com eficiência. Com conjuntos de dimensionamento de máquinas virtuais, você pode criar serviços em grande escala para áreas como computação, big data e cargas de trabalho de contêiner.

# Conjuntos de disponibilidade da máquina virtual

Os conjuntos de disponibilidade foram projetados para garantir que as VMs escalonem atualizações e tenham conectividade de rede e energia variadas, impedindo que você perca todas as suas VMs com uma só falha de rede ou energia.

Os conjuntos de disponibilidade fazem isso agrupando VMs de duas maneiras: domínio de atualização e domínio de falha.

* **Domínio de atualização:** as VMs de grupos de domínio de atualização que podem ser reinicializadas ao mesmo tempo. Isso permite que você aplique atualizações sabendo que apenas um agrupamento de domínio de atualização estará offline por vez. Todos os computadores em um domínio de atualização serão atualizados. Um grupo de atualizações que passa pelo processo de atualização recebe um tempo de 30 minutos para se recuperar antes que a manutenção no próximo domínio de atualização seja iniciada.
* **Domínio de falha:** o domínio de falha agrupa suas VMs por origem de energia comum e comutador de rede. Por padrão, um conjunto de disponibilidade dividirá suas VMs em até três domínios de falha. Isso ajuda a proteger contra uma falha de energia física ou de rede, tendo VMs em diferentes domínios de falha (portanto, sendo conectadas a diferentes recursos de energia e rede).

Não há nenhum custo adicional para configurar um conjunto de disponibilidade. Você paga apenas pelas instâncias de VM criadas.

# Exemplos de quando usar VMs

Alguns exemplos comuns ou casos de uso para máquinas virtuais incluem:

* **Durante o teste e o desenvolvimento.** As VMs fornecem uma maneira rápida e fácil de criar diferentes configurações de sistema operacional e de aplicativo.

* **Ao executar aplicativos na nuvem.** A capacidade de executar determinados aplicativos na nuvem pública, em vez de criar uma infraestrutura tradicional para executá-los, pode trazer benefícios econômicos substanciais.

* **Ao estender seu datacenter para a nuvem:** uma organização pode estender os recursos de sua própria rede local criando uma rede virtual no Azure e adicionando VMs a ela. Aplicativos como o SharePoint podem, então, ser executados em uma VM do Azure em vez de localmente. 

* **Durante a recuperação de desastre:** Se um datacenter primário falhar, você poderá criar VMs em execução no Azure para executar seus aplicativos críticos e desligá-los quando o datacenter primário ficar operacional novamente.

# Migrar para a nuvem com VMs (lift-and-shift)

Você pode criar uma imagem do servidor físico e hospedá-la em uma VM com poucas ou nenhuma alteração. Assim como um servidor local físico, você deve manter a VM: você é responsável por manter o sistema operacional e o software instalados.

# Recursos da VM

Ao provisionar uma VM, você também terá a oportunidade de escolher os recursos associados a essa VM, incluindo:

* Tamanho (finalidade, número de núcleos de processador e quantidade de RAM)
* Discos de armazenamento (unidades de disco rígido, unidades de estado sólido etc.)
* Rede (rede virtual, endereço IP público e configuração de porta)
