# dio-desafio-gerenciamento-vm-azure.
dio-desafio-gerenciamento-vm-azure.

# Desafio de Projeto: Gerenciando Máquinas Virtuais no Azure

Repositório criado para documentar a execução do Desafio de Projeto da DIO sobre o gerenciamento de Máquinas Virtuais (VMs) na Microsoft Azure.

##Descrição

Este projeto prático aborda a criação e o gerenciamento de uma Máquina Virtual no Azure. O foco principal está nas operações de disco, especificamente na anexação e desanexação de um disco de dados, uma tarefa fundamental na administração de infraestrutura na nuvem.

##Ferramentas Utilizadas
* Microsoft Azure
* Máquinas Virtuais (VMs)
* Discos Gerenciados (Managed Disks)
* GitHub

##⚙️ Etapas do Projeto

### 1. Criação da Máquina Virtual
O primeiro passo foi provisionar uma nova Máquina Virtual (`vm-gerenciada`) dentro de um Grupo de Recursos dedicado.


### 2. Anexação de um Disco de Dados
Para expandir a capacidade de armazenamento, um novo disco de dados (`datadisk-01`) de 4 GiB foi criado e anexado à VM. 


### 3. Desanexação do Disco de Dados
A tarefa de gerenciamento principal foi executada ao desanexar o `datadisk-01` da VM. O disco não é excluído e permanece disponível no grupo de recursos para uso futuro.

![Criação de VM]([VM.jpg](https://github.com/danrod19/dio-desafio-gerenciamento-vm-azure./blob/main/VM.png))

Os SLAs (Acordos de Nível de Serviço) das máquinas virtuais (VMs) do Azure garantem uma porcentagem de tempo de atividade, que se traduz em um tempo máximo de inatividade aceitável semanal, mensal e anual. Quanto maior a porcentagem do SLA, menor é o tempo de inatividade permitido e maior será o custo para o serviço.
SLAs e tempo de inatividade:

99%: até 1,68 hora por semana, 7,2 horas por mês e 3,65 dias por ano.
99,9%: até 10,1 minutos por semana, 43,2 minutos por mês e 8,76 horas por ano.
99,95%: até 5 minutos por semana, 21,6 minutos por mês e 4,38 horas por ano.
99,99%: até 1,01 minuto por semana, 4,32 minutos por mês e 52,56 minutos por ano.
99,999%: até 6 segundos por semana, 25,9 segundos por mês e 5,26 minutos por ano.

Opções de disponibilidade para alta resiliência
Para melhorar a disponibilidade das VMs e garantir um SLA mais alto, você pode usar opções de redundância que determinam como sua VM e seus recursos associados (como discos e IPs públicos) são implantados. As opções incluem:

Conjuntos de disponibilidade: Agrupam duas ou mais VMs para garantir que, durante uma manutenção planejada ou não planejada, pelo menos uma VM esteja disponível.

Conjuntos de dimensionamento de máquinas virtuais: Permitem dimensionar o número de VMs automaticamente e oferecem garantias de alta disponibilidade, distribuindo as VMs entre diferentes domínios de falha.

Zonas de disponibilidade: Separam fisicamente as VMs em diferentes zonas de uma região, cada uma com rede, energia e resfriamento independentes, para proteger contra falhas de data center.

Opções de redundância de armazenamento
Além da redundância da VM, o Azure oferece diferentes níveis de redundância para o armazenamento de dados, que também afetam o SLA:

LRS (Redundância Local): Replica os dados três vezes em um único data center na região primária.

ZRS (Redundância de Zona): Replica os dados de forma síncrona em três zonas de disponibilidade na região primária.

GRS (Redundância Geográfica): Replica os dados em uma região secundária distante.

GZRS (Redundância de Zona Geográfica): Combina ZRS na região primária com replicação para uma região secundária, oferecendo o maior nível de redundância e, consequentemente, o maior custo.

A escolha do SLA, das opções de disponibilidade e do tipo de redundância de armazenamento depende dos seus requisitos de resiliência e orçamento. Um SLA mais elevado garante menos tempo de inatividade, mas custa mais.



