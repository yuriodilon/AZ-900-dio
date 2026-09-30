# ☁️ Tipos de Serviço e Modelos de Nuvem no Azure

Resumo sobre os modelos de implantação de nuvem, modelos de serviço, o Modelo de Responsabilidade Compartilhada e a criação de banco de dados gerenciado no portal.

---

## 1. Modelos de Implantação de Nuvem

* **Nuvem Pública:** A infraestrutura pertence e é operada por um provedor terceirizado (Microsoft). Recursos distribuídos pela internet, alta escalabilidade e cobrança por consumo.
* **Nuvem Privada:** Infraestrutura dedicada exclusivamente a uma única organização, no datacenter local (*on-premises*) ou hospedada por terceiros, garantindo controle total.
* **Nuvem Híbrida:** Combinação entre ambientes públicos e privados/locais, permitindo compartilhar dados e cargas de trabalho conforme a necessidade de flexibilidade ou segurança.

---

## 2. Modelos de Serviço de Nuvem

* **IaaS (Infraestrutura como Serviço):** Servidores virtuais, rede e discos sob demanda. O cliente gerencia SO, middlewares e aplicações (ex: Azure VMs).
* **PaaS (Plataforma como Serviço):** O provedor gerencia hardware, sistema operacional e atualizações. O cliente foca exclusivamente no código e nos dados (ex: Azure App Service, Azure SQL Database).
* **SaaS (Software como Serviço):** Solução completa entregue pela nuvem e consumida diretamente pelo usuário final (ex: Microsoft 365, Teams).

---

## 3. Modelo de Responsabilidade Compartilhada (Shared Responsibility Model)

| Componente | On-Premises (Local) | IaaS | PaaS | SaaS |
| :--- | :--- | :--- | :--- | :--- |
| **Aplicações** | Cliente | Cliente | Cliente | Microsoft |
| **Dados e Acessos** | Cliente | Cliente | Cliente | Cliente |
| **Sistema Operacional** | Cliente | Cliente | Microsoft | Microsoft |
| **Rede Virtual / Middleware** | Cliente | Cliente | Microsoft | Microsoft |
| **Rede Física e Datacenter** | Cliente | Microsoft | Microsoft | Microsoft |

> **Regra fundamental:** Governança de dados, contas de usuários e controle de acessos são sempre de responsabilidade do **cliente**, em qualquer modelo.

---

## 4. Prática: Criação de Banco de Dados no Portal do Azure

Configuração de um serviço de banco de dados relacional gerenciado (PaaS) via portal:

* **Provisionamento:** Criação do recurso selecionando Grupo de Recursos (*Resource Group*), região e servidor lógico.
* **Camada de Computação e Armazenamento:** Ajuste de vCores, memória e tipo de desempenho conforme a carga da aplicação.
* **Segurança e Rede:** Configuração de regras de firewall do servidor, definindo liberação de IPs específicos e habilitando o acesso de outros serviços do Azure ao banco.
* **Vantagens do Modelo Gerenciado:** Backups automatizados, alta disponibilidade nativa e aplicação automática de patches de segurança sem intervenção manual no SO.