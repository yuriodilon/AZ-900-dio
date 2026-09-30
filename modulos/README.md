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

O **Acordo de Nível de Serviço** define o compromisso formal da Microsoft quanto ao tempo de atividade (*uptime*) e conectividade. Abaixo está a relação entre a porcentagem de SLA e o tempo máximo de inatividade tolerado:

| SLA | Tempo de inatividade por semana | Tempo de inatividade por mês | Tempo de inatividade por ano |
| :--- | :--- | :--- | :--- |
| **99%** | 1,68 hora | 7,2 horas | 3,65 dias |
| **99,9%** | 10,1 minutos | 43,2 minutos | 8,76 horas |
| **99,95%** | 5 minutos | 21,6 minutos | 4,38 horas |
| **99,99%** | 1,01 minuto | 4,32 minutos | 52,56 minutos |
| **99,999%** | 6 segundos | 25,9 segundos | 5,26 minutos |
