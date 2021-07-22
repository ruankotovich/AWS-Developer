# Módulo 6


## NoSQL
![picture 2](images/8a4e0cc98cfef8d2a302ae97b41ac13d36b1a0472676639b0850fb6b73f26acb.png)  

### [OLAP vs OLTP](https://www.stitchdata.com/resources/oltp-vs-olap/)
- Bancos relacionais são melhores para operações OLAP
- Bancos não relacionais são melhores para operações VOLATILES ou TRANSITORY (OLTP)



## AWS Database Options
![picture 3](images/5058e477c275e500f156879ca7d1bf796890d99c734c009142501e33391878d4.png)  

### Amazon RDS
 - Suporta diversos bancos de dados
   - SQL Server
   - MariaDB
   - Oracle
   - PostgreSLQ
   - MySQL
 - Autoscalável
 - Replicação
   - Read Replica (Worker)
   - Secondary Replica (Slave)
 - Backups por até 35 dias (mesmo deletando a instância principal)

### Amazon Aurora (Engine da AWS desenhada pra núvem)
- Postgres -> 5x mais rápido que o RDS
- MySQL -> 3x mais rápido que o RDS
- Alta disponibilidade
- Alta performance
- Alta escalabilidade
- Multiregiões

### Amazon Redshift
- Data Warehouse
- SQL Query em dados não estruturados no S3
- Suporta vários formatos
- Suporta vários BIs

### Amazon ElastiCache
- In memory data storage
- Fully managed

### Amazon Neptune
- Banco de dados em grafo
- Alcance e engajamento de perfis em redes sociais

### Amazon DynamoDB
- SGBD não relacional
- Alta disponibilidade
- Resposta de operação consistente
- Suporta documentos

#### Tabelas e Partições
- Tabelas
  - Partition Keys
  - Sort Keys (opcional)
  - Atributos

![picture 4](images/c243ce2587b1d54ef532e3b3f1018b985363580cb88d42009855b32b9451d6ad.png)  
- Busca por SortKeys de uma PK

![picture 5](images/35cd994fabc9938f60b859ce393417e123e03c2351fe1498d572d59217625c16.png)  

- Não é possível escolher de qual réplica consultar

### [Amazon DMS](https://aws.amazon.com/pt/dms/)
- Schema Convertion Tool