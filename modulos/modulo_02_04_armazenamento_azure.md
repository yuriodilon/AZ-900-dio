# ☁️ Módulo 2: Armazenamento do Azure

## 💾 Contas de Armazenamento e Redundância
* **Contas de Armazenamento:** Exigem um nome globalmente exclusivo, fornecem acesso via internet e agrupam serviços e opções de redundância.
* **Opções de Redundância:**
  * **LRS (Localmente Redundante):** Datacenter individual na região primária (Durabilidade: 11 noves).
  * **ZRS (Zonas Redundantes):** Três zonas de disponibilidade na região primária (Durabilidade: 12 noves).
  * **GRS (Geograficamente Redundante):** Datacenter único na primária e cópia em região secundária (Durabilidade: 16 noves).
  * **GZRS (Zonas Geograficamente Redundantes):** Três zonas na primária e um datacenter único na secundária (Durabilidade: 16 noves).

## 📦 Serviços e Camadas de Armazenamento
* **Blob:** Otimizado para quantidades massivas de dados não estruturados (textos, binários).
* **Disco:** Fornece armazenamento persistente para VMs e aplicativos.
* **Fila (Queue):** Armazenamento de mensagens para comunicação entre serviços (até 64KB por mensagem).
* **Arquivo (File):** Compartilhamento de arquivos de rede altamente disponível via protocolo SMB.
* **Tabela (Table):** Armazenamento NoSQL de chave/atributo para dados estruturados não relacionais.
* **Camadas de Acesso:** Divididas em Frequente (Hot), Esporádico (Cool), Frio (Cold) e Arquivo Morto (Archive), adequando custo à frequência de uso.
* **Pontos de Extremidade:** Cada serviço gera uma URL específica (ex: `https://<nome>.blob.core.windows.net`).

## 🔄 Migração e Gerenciamento de Dados
* **Migrações do Azure:** Plataforma unificada para avaliação e migração de recursos para a nuvem.
* **Azure Data Box:** Serviço físico (hardware de até 80 TB) enviado pela Microsoft para mover grandes volumes de dados offline.
* **AzCopy:** Utilitário de linha de comando para copiar dados para a conta de armazenamento (sincronização unidirecional).
* **Gerenciador de Armazenamento (Storage Explorer):** Interface gráfica amigável (Win/Mac/Linux) semelhante ao Windows Explorer.
* **Sincronização de Arquivos do Azure (Azure File Sync):** Sincronização bidirecional entre servidores locais e o Azure, liberando espaço local (camada de nuvem) e mantendo arquivos recentes acessíveis.