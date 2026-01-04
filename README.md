# azure-databricks-lakehouse-cdc
Simula um banco de dados de Clientes que sofre atualizações frequentes (mudança de endereço, telefone, status).

# 🏗️ Azure Databricks Lakehouse: End-to-End CDC Pipeline

![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)
![Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta_Lake-001F3E?style=for-the-badge&logo=delta&logoColor=white)


Este projeto implementa uma arquitetura **Lakehouse moderna** no Azure Databricks, simulando um cenário real de ingestão e processamento de dados de clientes com mudança de histórico (**SCD Type 2**).

![Painel Final de Monitoramento](https://github.com/leoneveslima/azure-databricks-lakehouse-cdc/blob/feat/orchestration-and-structure/img/final_dashboard.jpg?raw=true)
## 🏗️ Arquitetura da Solução

Este pipeline segue a arquitetura **Medallion (Multi-hop)** utilizando
**Databricks Lakehouse** e **Unity Catalog**, garantindo:

- Qualidade de dados
- Rastreabilidade ponta a ponta
- Governança e segurança
- Escalabilidade em streaming

### 🔄 Fluxo de Dados

- **Ingestão**: Dados brutos em JSON ingeridos via **Autoloader**
- **Processamento**: Streaming com **Structured Streaming**
- **Tratamento**:
  - Deduplicação
  - CDC (Change Data Capture)
- **Persistência**:
  - Camada Bronze (dados crus)
  - Camada Silver (SCD Type 2)
  - Camada Gold (dados agregados e analíticos)
- **Governança**: Dados organizados em **Unity Catalog Volumes**
le UC fill:#f9f9f9,stroke:#333,stroke-width:2px
```

