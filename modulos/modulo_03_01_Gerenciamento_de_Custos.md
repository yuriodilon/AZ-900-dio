# 💰 Gerenciamento de Custos e Governança no Azure

Resumo sobre os fatores que influenciam a precificação, ferramentas de cálculo e estratégias de governança de custos na nuvem.

---

## 1. Fatores que Afetam os Custos

O modelo de nuvem é baseado em despesas operacionais (OpEx), e os custos variam conforme os seguintes fatores:
* **Tipo de recurso:** Cada serviço possui medidores específicos de cobrança (ex: armazenamento vs. processamento).
* **Consumo:** Com o modelo "pago conforme o uso" (*pay-as-you-go*), o volume de uso é o maior gerador de custos.
* **Manutenção:** O monitoramento contínuo permite desligar recursos ociosos (como VMs subutilizadas), reduzindo desperdícios.
* **Área geográfica:** O valor do mesmo recurso pode mudar dependendo da região onde o datacenter está localizado.
* **Tráfego de rede:** A entrada de dados (Ingress) no Azure geralmente é gratuita, mas a saída de dados (Egress) ou o tráfego entre diferentes zonas de disponibilidade é cobrado.
* **Assinatura:** O tipo de assinatura (avaliação gratuita, estudante, corporativa) define os preços e descontos aplicados.

---

## 2. Ferramentas de Estimativa de Custos

* **Calculadora de Preços (Pricing Calculator):**
  * Usada para estimar o custo mensal de **novos recursos** no Azure.
  * Permite configurar variáveis como: Região, Camada (*Tier*), Opções de cobrança, Opções de suporte, Programas de desconto e Preços para Dev/Test.
* **Calculadora TCO (Custo Total de Propriedade):**
  * Usada para estimar a **economia de custos** ao migrar da infraestrutura local (*on-premises*) para o Azure.
  * Gera um relatório comparando os gastos atuais (energia, hardware, TI local) com a projeção na nuvem.

---

## 3. Gerenciamento de Custos do Azure (Azure Cost Management)

Ferramenta nativa para monitorar, alocar e otimizar gastos na nuvem. Suas principais funções incluem:
* **Relatórios:** Visualização de cobranças e faturas.
* **Orçamento (Budgets):** Definição de limites de gastos mensais ou anuais.
* **Alertas:** Notificações automáticas quando o custo atinge ou excede os limites estabelecidos no orçamento.
* **Recomendações:** Sugestões do Azure Advisor para otimizar e reduzir custos.

---

## 4. Marcas (Tags) e Governança

* **O que são:** Metadados (pares de *nome/valor*) anexados aos recursos do Azure.
* **Finalidade:** Organizar recursos de forma lógica e criar taxonomias (ex: `Ambiente: Produção`, `Departamento: RH`).
* **Cobrança:** Extremamente úteis para agrupar e filtrar faturas, permitindo identificar qual setor gerou qual custo.
* **Governança:** É possível usar o *Azure Policy* para exigir a criação obrigatória de marcas ou aplicar herança de tags do Grupo de Recursos para os recursos contidos nele.

---

## 5. Azure Marketplace

Loja virtual da Microsoft que permite aos clientes encontrar, experimentar, comprar e provisionar aplicativos e serviços de **terceiros** (provedores certificados). Inclui imagens de sistemas operacionais, firewalls, plataformas de contêiner e ferramentas de desenvolvedor.

---

## 6. Práticas de Otimização (Simulação de Máquinas Virtuais)

Estratégias práticas para baratear o custo de instâncias de computação:
1. **Instâncias Reservadas:** Comprometer-se com 1 ou 3 anos de uso gera descontos significativos em relação ao "pago conforme o uso".
2. **Azure Hybrid Benefit:** Reutilizar licenças locais do Windows Server ou SQL Server no Azure.
3. **Agendamento de Uso:** Configurar a automação para manter a VM ligada apenas durante o horário comercial (ex: 12 horas por dia), parando a cobrança de computação no restante do tempo.