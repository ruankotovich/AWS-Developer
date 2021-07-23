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

