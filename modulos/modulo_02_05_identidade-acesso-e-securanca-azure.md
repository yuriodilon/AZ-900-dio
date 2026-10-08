# ☁️ Módulo: Identidade, Acesso e Segurança no Azure

## 🔐 Microsoft Entra ID e Domain Services
* **Microsoft Entra ID (antigo Azure AD):** Serviço de gerenciamento de identidades e acesso baseado em nuvem.
  * **Principais recursos:** Autenticação, Logon Único (SSO), gerenciamento de aplicativos e dispositivos, e colaboração B2B.
* **Domain Services:** Fornece serviços de domínio na nuvem (como ingresso no domínio e políticas de grupo) sem a necessidade de gerenciar controladores de domínio (DCs) físicos. Ideal para executar aplicativos herdados que não suportam protocolos modernos.

## 🛡️ Autenticação vs. Autorização
* **Autenticação (AuthN):** Identifica *quem* está acessando (solicita credenciais válidas).
* **Autorização (AuthZ):** Determina *o que* a identidade autenticada pode fazer (nível de acesso e permissões).
* **MFA (Autenticação Multifator):** Exige dois ou mais elementos: algo que você sabe (senha), algo que possui (token/celular) e algo que você é (biometria).
* **Entra External ID (B2B):** Permite convidar pessoas externas (parceiros/clientes) para acessar o seu ambiente de forma segura.

## 🚦 Controle de Acesso e Confiança Zero (Zero Trust)
* **Acesso Condicional:** Avalia sinais (usuário, IP, dispositivo, risco) antes de conceder o acesso.
* **RBAC (Controle de Acesso Baseado em Função):** Gerenciamento granular que garante acesso de privilégio mínimo (apenas o necessário para o trabalho).
* **Confiança Zero (Zero Trust):** Modelo de segurança baseado em não confiar em ninguém por padrão. Princípios: verificar explicitamente, privilégio mínimo e assumir a violação (proteção em camadas).

## 🛡️ Microsoft Defender for Cloud
* Serviço de monitoramento e proteção contra ameaças para datacenters do Azure e locais.
* Fornece recomendações (Secure Score/Termômetro de segurança), detecta malwares, bloqueia ataques potenciais e oferece acesso Just-in-Time (JIT) para portas de gerenciamento.

## 🚀 Laboratório Prático
* **Entra ID:** Criação e gerenciamento de usuários (internos e externos), atribuição de regras (Roles), configuração de domínios personalizados e visualização do SLA (Health Preview). Observação: contas excluídas podem ser restauradas em até 30 dias.
* **Defender for Cloud:** Análise da postura de segurança, DevOps Security, criação de alertas e visão geral para equipes de SOC.