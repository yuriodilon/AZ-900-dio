# ☁️ Módulo 2: Computação e Rede no Azure

## 💻 Serviços de Computação
* **Máquinas Virtuais (VMs):** Oferta de IaaS (Infraestrutura como Serviço) que emula computadores físicos com controle total do Sistema Operacional. Ideal para migrações *lift-and-shift* (mover para a nuvem sem alterar a arquitetura).
* **Conjunto de Dimensionamento de VM (Scale Sets):** Balanceamento de carga com escalabilidade automática de máquinas virtuais.
* **Conjuntos de Disponibilidade:** Estratégia de redundância que divide as VMs em **Domínios de Falha** (racks físicos diferentes para evitar quedas de energia/rede) e **Domínios de Atualização** (evita que todas as máquinas reiniciem juntas em atualizações do Azure).
* **Azure Virtual Desktop (AVD):** Serviço de virtualização de aplicativos e áreas de trabalho do Windows. Suporta múltiplas sessões (vários usuários no mesmo S.O.) e acesso seguro.

## 📦 Contêineres e Aplicações Web (Serverless)
* **Contêineres do Azure:** Ambientes leves e isolados que não exigem gerenciamento do S.O.
  * **Azure Container Instances (ACI):** PaaS rápido para executar um contêiner isolado.
  * **Azure Container Apps (ACA):** PaaS para contêineres com suporte a balanceamento de carga e escala.
  * **Azure Kubernetes Service (AKS):** Orquestrador para grandes volumes de contêineres e arquiteturas distribuídas (microsserviços).
* **Azure App Service:** Plataforma gerenciada (PaaS) para hospedar aplicativos web e APIs (suporta .NET, Node.js, Java, Python, PHP).
* **Azure Functions:** Oferta *Serverless* (sem servidor). O código é baseado em eventos e executado sob demanda, eliminando a necessidade de infraestrutura inativa.

## 🌐 Serviços de Rede
* **Azure Virtual Network (VNet):** Permite a comunicação segura entre recursos do Azure, internet e redes locais. 
  * Pode ser dividida em **sub-redes** para segmentação.
  * Pode ser interligada a outras VNets via **Emparelhamento (Peering)**.
* **Pontos de Extremidade (Endpoints):** Podem ser **públicos** (abertos para a internet) ou **privados** (restritos à sua rede interna).
* **VPN Gateway:** Roteia tráfego criptografado pela internet entre a rede virtual do Azure e redes locais.
* **Azure ExpressRoute:** Conexão privada e dedicada (não passa pela internet) fornecida por um provedor parceiro.
* **Azure DNS:** Serviço de resolução de nomes altamente confiável (rede Anycast), integrado nativamente ao gerenciamento de acessos (RBAC) do Azure e com suporte a domínios privados.

## 🚀 Laboratório Prático
* Criação e configuração de Máquinas Virtuais (VMs).
* Configuração de Conjuntos de Dimensionamento de VMs.
* Visualização e conceitos práticos do Azure Virtual Desktop.
* Criação básica de um Aplicativo de Funções (Azure Functions).