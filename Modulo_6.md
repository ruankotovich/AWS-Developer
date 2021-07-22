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