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


Resultados e Conclusões

O desafio foi concluído com sucesso. As operações de anexar e desanexar discos em uma VM ativa foram realizadas sem dificuldades através do Portal Azure, demonstrando a flexibilidade da plataforma.

**Principais aprendizados:**
* A diferença entre um **Disco de SO** e um **Disco de Dados** e suas finalidades.
* Discos de dados podem ser gerenciados (adicionados ou removidos) sem a necessidade de recriar a máquina virtual.
* Desanexar um disco preserva seus dados, permitindo que ele seja movido entre VMs, o que é essencial para cenários de migração ou recuperação
