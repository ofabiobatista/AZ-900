# 2.1.2 Infraestrutura física do Azure 🏙
###### Fonte: https://learn.microsoft.com/pt-br/training/modules/describe-core-architectural-components-of-azure/5-describe-azure-physical-infrastructure

Ao longo de seu percurso com o Microsoft Azure, você ouvirá e usará termos como Regiões, Zonas de Disponibilidade, Recursos, Assinaturas etc. Os principais componentes da arquitetura do Azure podem ser divididos em dois agrupamentos principais: a infraestrutura física e a infraestrutura de gerenciamento.

# Infraestrutura física

A infraestrutura física do Azure começa com datacenters. São instalações com recursos organizados em racks com energia, refrigeração e infraestrutura de rede dedicadas. Os datacenters são agrupados em **Regiões do Azure** ou em **Zonas de Disponibilidade do Azure** projetadas para ajudá-lo a obter resiliência e confiabilidade.

# Regiões

Uma região é uma área geográfica do planeta que contém **pelo menos um data center, mas possivelmente vários**, nas proximidades e conectado a uma rede de baixa latência.

> **Observação**
>
>Alguns serviços ou recursos de VM (máquina virtual) estão disponíveis somente em determinadas regiões, como tamanhos específicos de VMs ou tipos de armazenamento. Também há alguns serviços globais do Azure que não exigem que você selecione uma região específica, como o Azure Active Directory, o Gerenciador de Tráfego do Azure e o DNS do Azure.

# Zonas de Disponibilidade

Zonas de disponibilidade são datacenters separados fisicamente dentro de uma região do Azure. Cada zona de disponibilidade é composta de um ou mais datacenters equipados com energia, resfriamento e rede independentes. Uma zona de disponibilidade é configurada para ser um limite de isolamento. Se uma zona ficar inativa, as outras continuarão funcionando. Zonas de disponibilidade são conectadas por meio de redes de fibra óptica privadas de alta velocidade.

![Região do Azure](https://learn.microsoft.com/pt-br/training/wwl-azure/describe-core-architectural-components-of-azure/media/availability-zones-c22f95a3.png)

> **Importante**
> 
> Para garantir a resiliência, **no mínimo três zonas de disponibilidade separadas estão presentes em todas as regiões** habilitadas para zona de disponibilidade. No entanto, nem todas as Regiões do Azure atualmente dão suporte a zonas de disponibilidade.

# Usar zonas de disponibilidade em seus aplicativos

O Azure pode ajudar a tornar seu aplicativo altamente disponível por meio das zonas de disponibilidade. Você pode usar as zonas de disponibilidade para executar aplicativos críticos e incorporar alta disponibilidade à arquitetura do aplicativo, colocalizando seus recursos de computação, armazenamento, rede e dados em uma zona de disponibilidade e replicando em outras zonas de disponibilidade. Tenha em mente que pode haver um custo para duplicar seus serviços e transferir dados entre zonas de disponibilidade. As zonas de disponibilidade são destinadas, principalmente, a VMs, discos gerenciados, balanceadores de carga e bancos de dados SQL. Os serviços do Azure que dão suporte às zonas de disponibilidade enquadram-se em três categorias:

* **Serviços em zonas**: você fixa o recurso a uma zona específica (por exemplo, VMs, discos gerenciados, endereços IP).
* **Serviços com redundância de zona**: a plataforma replica automaticamente entre zonas (por exemplo, armazenamento com redundância de zona, Banco de Dados SQL).
* **Serviços não regionais**: os serviços estão sempre disponíveis em geografias do Azure e são resilientes a interrupções em toda a zona, bem como a interrupções em toda a região.

Mesmo com a resiliência adicional que as zonas de disponibilidade proporcionam, é possível que um evento possa ser tão grande que afete várias zonas de disponibilidade em uma só região.

# Pares de regiões

A maioria das regiões do Azure é emparelhada a outra região na mesma geografia (como EUA, Europa ou Ásia) a pelo menos 300 milhas (cerca de 480 km) de distância. Essa abordagem permite a replicação de recursos em uma geografia, o que ajuda a reduzir a probabilidade de interrupções devido a eventos como desastres naturais, conflitos civis, quedas de energia ou interrupções de rede física afetarem toda uma região.

> **Importante**
> 
> Nem todos os serviços do Azure replicam dados automaticamente ou retornam automaticamente de uma região com falha para replicação cruzada para outra região habilitada. Nesses cenários, a recuperação e a replicação devem ser configuradas pelo cliente.

Como o par de regiões está diretamente conectado e suficientemente afastado para ser isolado contra desastres regionais, você pode usá-lo para fornecer redundância de dados e serviços confiáveis.

![Par de regiões](https://learn.microsoft.com/pt-br/training/wwl-azure/describe-core-architectural-components-of-azure/media/region-pairs-7c495a33.png)

# Vantagens adicionais dos pares de regiões

* Se ocorrer uma interrupção ampla do Azure, uma região de cada par será priorizada para que pelo menos uma seja restaurada o quanto antes para os aplicativos hospedados nesse par de regiões.
* As atualizações planejadas do Azure são distribuídas para regiões emparelhadas uma por vez, de modo a minimizar o tempo de inatividade e o risco de interrupção dos aplicativos.
* Os dados continuam residindo na mesma geografia que seu par (com exceção do Sul do Brasil) para fins de jurisdição do imposto e aplicação da lei.

# Regiões soberanas

Além das regiões normais, o Azure também tem regiões soberanas. Regiões soberanas são instâncias do Azure isoladas da instância principal do Azure. Talvez seja necessário usar uma região soberana para fins legais ou de conformidade.

As regiões soberanas do Azure incluem:

* US DoD Central, US Gov – Virgínia, US Gov Iowa, entre outros: essas regiões são instâncias lógicas e físicas do Azure isoladas da rede, destinadas a parceiros e órgãos do governo dos EUA. Esses datacenters são operados por cidadãos selecionados dos EUA e incluem certificações de conformidade adicionais.
* Leste da China, Norte da China, entre outros: essas regiões estão disponíveis por meio de uma parceria exclusiva entre a Microsoft e a 21Vianet, segundo a qual a Microsoft não mantém diretamente os data centers.

### ⏮ 2.1.1 <a href="https://github.com/ofabiobatista/AZ-900/blob/main/contasAzure.md"> Introdução a contas do Azure 👤💻 </a>
### ⏭ 2.1.3 <a href="https://github.com/ofabiobatista/AZ-900/blob/main/infraestruturaGerenciamentoAzure.md"> Infraestrutura de gerenciamento do Azure 🌐 </a>

