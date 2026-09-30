# 🏛️ Arquitetura e Serviços do Azure

Resumo sobre os componentes estruturais da infraestrutura global da Microsoft, estratégias de redundância regional e a hierarquia de governança de recursos.

---

## 1. Infraestrutura Global do Azure

### Regiões (Regions)
* Conjunto de datacenters implantados dentro de um perímetro definido por latência e conectados por uma rede regional dedicada.
* O Azure conta com mais de 60 regiões distribuídas em mais de 140 países.
* **Critérios de escolha:** Proximidade geográfica (menor latência/delay para o usuário final), conformidade legal/regulamentatória e residência de dados (manter dados dentro do país de origem).

### Zonas de Disponibilidade (Availability Zones)
* Datacenters **fisicamente separados** dentro da mesma região geográfica.
* Cada zona possui infraestrutura independente de alimentação elétrica, resfriamento e conectividade de rede.
* Protege aplicações contra falhas em nível de datacenter completo sem sair da região.

### Pares de Região (Region Pairs)
* Cada região do Azure é emparelhada com outra dentro da mesma área geográfica a uma distância mínima de **300 milhas (~480 km)**.
* **Vantagens:** 
  * Replicação assíncrona automática para serviços selecionados.
  * Em caso de indisponibilidade em larga escala, a recuperação é priorizada de forma coordenada (uma região do par por vez).
  * Base fundamental para planos de Recuperação de Desastres (*Disaster Recovery*).

### Regiões Soberanas (Sovereign Regions)
Instâncias isoladas física e logicamente da nuvem pública global para atender a rigorosos requisitos legais e de segurança nacional:
* **Azure Government:** Exclusivo para órgãos governamentais dos EUA (federais, estaduais, locais) e parceiros homologados.
* **Azure China (21Vianet):** Instância independente operada localmente pela 21Vianet para cumprir as regulações chinesas.

---

## 2. Hierarquia de Recursos e Governança

A organização de recursos no Azure segue uma estrutura hierárquica em camadas: