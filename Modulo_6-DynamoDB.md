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

### [Amazon DMS](https://aws.amazon.com/pt/dms/)
- Schema Convertion Tool

### Amazon DynamoDB
- SGBD não relacional
- Alta disponibilidade
- Resposta de operação consistente
- Suporta documentos

#### Tabelas e Partições
- Tabelas
  - Partition Keys (HASH)
  - Sort Keys (RANGE) (opcional)
  - Atributos

![picture 4](images/c243ce2587b1d54ef532e3b3f1018b985363580cb88d42009855b32b9451d6ad.png)  
- Busca por SortKeys de uma PK

![picture 6](images/5d61cea78237c791267333c67d839e33ba3ce4dd2be791116bfb0702f6db7214.png)  


- Não é possível escolher de qual réplica consultar

#### Itens e atributos
- Key value item
- Document item

#### Modelos de consistência
- RCU (Read Capacity Unit)
  - Lê 4KB/s
  - Leitura Eventual (0.5 RCU)
  - Leitura Forte (1 RCU)
- WCU (Write Capacity Unit)

#### Índices secundários
- Habilita queries para atributos não-chave
- Dois tipos
  - GSI (Global Secondary Index)
    ![picture 8](images/07afa8a7ca004093d748f0653b1397e7696b4780c648cdf792625d37d913fc40.png)  
    - Outra partição de dados
    - Projeção dos dados (cópia, nesse caso)
    - Somente consistência eventual (pois é uma duplicação)

  - LSI (Local Secondary Index)
    ![picture 7](images/5e92af3d5f2894aac3600cd7a2f331c77462495b890a1c68218d48ac243e574d.png)  
    - Troca de sort-keys
    - Chave de partição se mantém
    - Duplica a tabela, mas a segunda parte (duplicada) com o sort_key trocado com a nova chave de busca (um attribute)
    - Somente é possível criar o índice no momento de criação da tabela

#### Streams
- Permite criar stream de dados
  ![picture 9](images/0754827899fa2185e245959125d076227799f8c9016b8058657ca4a3a5782794.png)  

  - Eventos de modificação
    - Leitura
    - Escrita
    - Deleção
    - Modificação
  - Tabelas Globais
    - Replicadas em diferentes Regions
  - Backups
  - Operações Secundárias
    - BatchGet
    - BatchWrite

#### Boas Práticas
- Distribuição de Workload entre partições com WCU/RCU ociosas
![picture 1](images/961ef6811075129e74396678e1cb2e6d8e8fa946b43aa422dc3c77a4298d83e5.png)  

- Usar índices esparsos
  - Não criar para atributos que não estão sendo utilizados
- Em índices globais, só levar os atributos importantes