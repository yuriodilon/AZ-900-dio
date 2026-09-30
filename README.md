# ☁️ Microsoft Azure Essentials | DIO.me

![Microsoft Azure](https://img.shields.io/badge/Microsoft_Azure-0089D6?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![DIO.me](https://img.shields.io/badge/DIO.me-Desafio_de_Projeto-E94D5F?style=for-the-badge)

**Módulo:** Conceitos Iniciais de Cloud com Azure  
**Descrição:** Repositório com o resumo dos principais conceitos aprendidos sobre infraestrutura em nuvem no Azure, abordando Máquinas Virtuais (VMs), estratégias de Alta Disponibilidade e Acordos de Nível de Serviço (SLA).

---


## Microsoft Azure Essentials

O **Microsoft Azure** é a plataforma de computação em nuvem da Microsoft que oferece serviços nos modelos **IaaS** (Infraestrutura), **PaaS** (Plataforma) e **SaaS** (Software), permitindo criar, implantar e gerenciar aplicações através de uma rede global de datacenters divididos em **Regiões** e **Geografias**.

---

## Máquinas Virtuais (Azure VMs)

Recurso de **IaaS** que fornece computação sob demanda e escalável (Windows ou Linux) sem a necessidade de adquirir hardware físico.

* **Controle Total:** Acesso ao sistema operacional, configurações de rede e instalação de softwares personalizados.
* **Famílias de VMs:** Dimensionadas conforme a carga de trabalho — Uso Geral (Série B, D), Otimizadas para Computação (Série F), Memória (Série E) ou Armazenamento (Série L).
* **VM Scale Sets (VMSS):** Permite criar e gerenciar um grupo de VMs idênticas com balanceamento de carga e escalonamento automático (*autoscaling*).

---

## Alta Disponibilidade (High Availability)

Estratégias do Azure para garantir que aplicações e VMs continuem operando mesmo diante de falhas de hardware, manutenção ou quedas de datacenters:

* **Conjuntos de Disponibilidade (Availability Sets):** Agrupam VMs dentro de um **mesmo datacenter**, distribuindo-as em:
* **Domínios de Falha (Fault Domains):** Racks físicos separados (proteção contra falha de energia ou switch de rede).
* **Domínios de Atualização (Update Domains):** Grupos lógicos reiniciados separadamente durante manutenções planejadas.


* **Zonas de Disponibilidade (Availability Zones):** Datacenters fisicamente separados dentro de uma **mesma região do Azure**, cada um com energia, refrigeração e rede independentes.
* **Recuperação de Desastres (Regiões Pareadas):** Replicação entre regiões geograficamente distantes (ex: Azure Site Recovery) para proteção contra desastres em larga escala.

---

## SLA (Service Level Agreement)

O **Acordo de Nível de Serviço** define o compromisso formal da Microsoft quanto ao tempo de atividade (*uptime*) e conectividade. O SLA de máquinas virtuais varia conforme a arquitetura de redundância adotada:

| Configuração da Arquitetura | SLA Garantido | Tempo Máximo de Inatividade (Mensal) |
| --- | --- | --- |
| **VM Única** (com SSD Standard) | **99,5%** | ~3,6 horas |
| **VM Única** (com SSD Premium ou Ultra Disk) | **99,9%** | ~43,2 minutos |
| **2+ VMs em Conjunto de Disponibilidade** (Availability Set) | **99,95%** | ~21,6 minutos |
| **2+ VMs em Zonas de Disponibilidade** (Availability Zones) | **99,99%** | ~4,32 minutos |
