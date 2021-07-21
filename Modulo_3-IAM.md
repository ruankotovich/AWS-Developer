# Módulo 3

## Shared Responsibility model (AWS + Costumer)

![picture 21](images/feb3b1ac4189c45a8c8ed74b0928328e4bcf51dd32b45699027c56b5d1dcb0ac.png)  

- AWS disponibiliza as ferramentas para tornar a aplicação e infraestrutura segura
- O cliente utiliza os serviços e ferramentas para tornar a aplicação e infraestrutura segura

## IAM (Identity and Access Manager)

Políticas geram permissões para usuários em grupos com determinados papeis

![picture 22](images/f013c0ab04511af06b997691ffc44de7e4ad7e99a0383a9fb3c43d868697c8f2.png)  

- Usuários podem assumir roles (algum papel que desempenhe uma ação em recursos)

![picture 23](images/3fb7256335e035a0032c71a7bf1a24948f12ffaecda3176ef10efdb94e2c20b8.png)  

- Instâncias podem assumir roles para utilizar recursos

### Tipos de Permissão
- Baseados em identidade
  - Não precisa do ARN do usuário
  - Bind serviços para o usuário

- Baseados em recursos
  - Atrelada a um recurso
    - Bucket do S3
    - Instância EC2
  - Bind usuários para o serviço

![picture 24](images/41c89ae3c1d8fb9b2e50a6cf6939968a8e62b5d35a6432ed20911b98609a6637.png)  


(O NÃO você sempre tem, você busca o SIM)

## ARN (Amazon Resource Names)

- Utilizado pra identificar um recurso de maneira única na aws
  
  `arn:aws:<service>:<region>:<account>:<resource_id>`


## Autenticação

- AWS Authentication
- Resource authentication
- App authentication
- DB authentication

## Credentials
- `.aws/credentials` - arquivo de chave
- É preferível usar as ROLES
- 
![picture 25](images/bc57b35d5a0f2f0cee731c64ca9933595545fe423c31f81b01583b99c3f195d9.png)  

### Algoritmo
- 1. Procura no código
- 2. Procura nas variáveis de ambiente
- 3. Procura nos arquivos de credencial
- 4. Procura nas roles da instância