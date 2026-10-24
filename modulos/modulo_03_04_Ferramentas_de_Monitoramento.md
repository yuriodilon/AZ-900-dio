# 📊 Ferramentas de Monitoramento no Azure

Resumo sobre os serviços de análise, alertas de saúde da infraestrutura e monitoramento de desempenho da plataforma Azure.

## 1. Assistente do Azure (Azure Advisor)
* Analisa os recursos implantados e fornece recomendações proativas baseadas nas melhores práticas da Microsoft.
* Centraliza as informações e insights em cinco pilares fundamentais:
  * **Confiabilidade:** Sugestões para garantir a alta disponibilidade de serviços essenciais.
  * **Segurança:** Identificação de vulnerabilidades e riscos de configuração.
  * **Desempenho:** Melhorias na velocidade e responsividade dos recursos e aplicativos.
  * **Custo:** Identificação de recursos subutilizados ou ociosos para redução de gastos.
  * **Excelência Operacional:** Recomendações para aprimorar o gerenciamento de processos e fluxos de trabalho.

## 2. Integridade do Serviço do Azure (Azure Service Health)
Coleção de painéis que mantém o usuário informado sobre o status da infraestrutura e possíveis interrupções. É dividida em três níveis de visibilidade:
* **Status do Azure (Azure Status):** Visão macro e global informando a integridade de todos os serviços do Azure em todas as regiões do mundo.
* **Integridade do Serviço (Service Health):** Visão intermediária e filtrada, focada apenas nos serviços e regiões que você está utilizando. Ignora incidentes em regiões onde sua conta não possui recursos.
* **Integridade de Recursos (Resource Health):** Visão granular e personalizada que detalha o status de saúde de recursos específicos que você provisionou (ex.: informando se uma Máquina Virtual específica sofreu falha de hardware).

## 3. Azure Monitor
* Plataforma central e abrangente que maximiza a disponibilidade e o desempenho de aplicativos.
* Coleta, analisa e permite a tomada de decisões (como acionamento de alertas ou escalonamento automático) com base na telemetria contínua extraída da nuvem e de ambientes locais (*on-premises*).