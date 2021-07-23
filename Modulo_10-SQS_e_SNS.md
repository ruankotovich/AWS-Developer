# Módulo 10


## SQS
- Consumidor não pode processar todas as requisições de uma vez
- Gargalo
- Desacoplamento do consumidor e produtor

### Ciclo de Vida
- Insertion
  - Wait Time (ttl)
  - Número de mensagens recebidas
- Deletion
  - Deleção chamada pelo consumidor

### Operações
- Criar Fila
- Estipular atributos da fila
- Recuperar atributos da fila
- Recuperar URI da fila
- Listar filas
- deletar fila

### Dead Letter Queue
- Fila de mensagens que não consegui processar

### Casos de Uso

![picture 9](images/da0d0bb54ea446070d2aa7ca3f0f790835485e80171c33a8fb7397a2aacf382e.png)  


## SNS
- Tópicos
  - AWS Lambda
  - SQS
  - HTTP
  - Email
  - SMS
  - Mobile (Push Notifications)
- Subject pode ser usado para filtros
- Os tópicos precisam ser criados antes da utilização  
  - Diferente do kafka, que os tópicos podem ser criados on-the-fly

### Operações
 - CreateTopic
 - Subscribe
 - DeleteTopic
 - Publish

### Caso de Uso

![picture 11](images/b2b152c45eddd75dcab863ef6b2e34b5c44195c18a4ca84abc6a0ee935fd49fe.png)  


![picture 10](images/d5863cac111f837668fe9a40601310df4ef73d1fc3c33e3f116e701ac4991a3c.png)  


### Comparativo entre SQS e SNS

![picture 12](images/5067011db29be9fb29b025f8d0e78795bff321e402d382c68d0c6e0988cf074a.png)  

