# 🛡️ Governança e Conformidade no Azure

Resumo sobre as ferramentas e serviços do Azure focados em padronização, conformidade regulatória e proteção de recursos e dados.

---

## 1. Azure Blueprints

* Permite definir e criar ambientes padronizados, de forma rápida e repetível.
* Usado para garantir que novas assinaturas ou ambientes de projeto sejam implantados de acordo com os padrões, requisitos e governança da organização desde o primeiro dia.

---

## 2. Azure Policy

Serviço que ajuda a impor padrões organizacionais e avaliar a conformidade em escala.
* **Governança:** Fornece consistência de recursos com foco em conformidade regulatória, segurança, custo e gerenciamento.
* **Auditoria:** Avalia e identifica continuamente os recursos do Azure que não atendem às políticas estabelecidas.
* **Iniciativas:** Fornece definições de políticas e iniciativas integradas divididas em categorias (armazenamento, rede, computação, central de segurança e monitoramento).
* **Efeito de Modificação (Modify Effect):** Pode atuar na remediação de recursos não conformes (Non-compliant -> Recomandation -> Compliant), corrigindo-os automaticamente durante a criação ou atualização.

---

## 3. Bloqueios de Recurso (Resource Locks)

Evitam a exclusão ou modificação acidental de recursos essenciais do Azure. Podem ser aplicados em diferentes níveis hierárquicos: Assinatura, Grupo de Recursos ou diretamente em Recursos Individuais.

| Tipo de Bloqueio | Permite Ler? | Permite Atualizar? | Permite Excluir? |
| :--- | :--- | :--- | :--- |
| **Excluir (CanNotDelete)** | SIM | SIM | NÃO |
| **Somente Leitura (ReadOnly)** | SIM | NÃO | NÃO |

---

## 4. Microsoft Purview

Família de soluções voltada para governança, risco e conformidade de dados, fornecendo uma visão unificada sobre os ativos de informação da organização (locais, multinuvem e SaaS).
* **Descoberta automatizada:** Mapeamento automático de dados espalhados pela infraestrutura.
* **Classificação de dados:** Identificação e rotulagem de dados confidenciais (ex: números de cartão de crédito, documentos de identidade).
* **Linhagem de dados:** Rastreamento de ponta a ponta, mostrando a origem dos dados e como eles se movem pela organização.