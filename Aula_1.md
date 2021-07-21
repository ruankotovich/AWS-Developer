# Aula 1

## Pausas
- Intervalo 9h30 ~ 9h45 (UTC)
- Intervalo 15h30 ~ 15h45 (UTC)
- Almoço 12h ~ 13h20 (UTC)
  
## Material

## Introdução ao AWS

- Introdução ao cloud
- Cenários de cloud
- Overview da infraestrutura
- Introdução ao AWS Foundation Services
- Wrap-Up


### Cloud Computing
- IaaS - Infraestructure as a service - rodar a infraestrutura sem gerenciá-la (EC2, por exemplo)
- PaaS - Platform as a service - rodar aplicações sem gerenciar a infraestrutura (RDS, por exemplo)
- SaaS - software as service (Lamnda, por exemplo)
- Parar de pensar a infraestrutura como hardware, e sim pensar nela como um software (seviço). 



#### Benefícios

![picture 1](images/9168a8a79e63918ccacfcd1a0cf53241ea73d96287b2d3934bd628d98f534883.png)  

- Não é necessário administrar um datacenter
- Pensar na aplicação, e só
- "o servidor não tá dimensionado direitinho...", rapidamente modificável
- Despezas variáveis
- On demand
- Maior utilizações, Menor preço (massive economies of scale)
- Elasticidade
- Agilidade de recursos
- Ubiquidade

### Service Stack
![picture 2](images/b19483851c3a7dd4185a51b774080e6710ac290f2abb5ea4105eca06f0d59547.png)

![picture 3](images/a0a808d79a26cf1da9a6109bbb0e0e38fce133789932dea4f295d3dcfa2d695a.png)  


- Serviços de Computação
  - EC2
- Serviços de Networking
  - VPC
  - Route 53
- Serviços de Armazenamento
  - S3 - armazenamento de objetos.
  - S3 Glacier - o mesmo que o S3, só que baseado em long-term-storage.
  - EBS - dimensionamento de disco, escolhendo com throughput otimizado, etc.
  - EFS - totalmente gerenciado para compartilhamento de arquivos, não é necessário dimensionar, ele é autoescalável, escolher zona de disponibilidade, várias instâncias concorrentes. (petabytes)
- Serviços de Gerenciamento
  - CloudWatch - monitoramento e observação criado para engenheiros de DevOps
  - CloudTrail - "Dedo duro", registra todas as chamadas de API dentro da conta
  - CloudFormation - IaC

#### Serviços gerenciados vs Não Gerenciados

##### Não Gerenciados
- Você gerencia somente a escala, a tolerância a falha e a disponibilidade, mas não o hardware.
  - EC2

##### Gerenciados
- Não é gerenciada a escala, tolerância, nem disponibilidade, são geralmente construidos em um serviço
  - DB

![picture 4](images/764dbd250d0871158df94b5c1e5877055c1b3756a26feb99b031995d817cd4fb.png)


#### Cenários de Núvem

- All-In cloud
- Hybrid

#### Microsserviços

![picture 5](images/57bbf895a13f5d4b5978b48058bafa0de0767de73d757e51a899e334c833afe2.png)  

- Agilidade - Features específicas por ms (arquitetura mais rápida em ms específico)
- Escalabilidade flexível - não é necessário pensar em escalar monolito, somente o MS (lei de ahmdal)
- Liberdade Tecnológica - Não é necessário que outro ms conheça outro, somente a interface de comunicação entre eles
- Código reutilizável
- Resiliência (isolation)
- Deploy fácil

##### Melhores práticas
- Trocar os componentes sem quebrá-los
  - A interface de comunicação é um contrato (tipo o gRPC ou Ethereum)
  - Cada um dos microsserviços é dono de seu processo

- Usar uma API simples
  - Diminui o custo de usar o serviço
  - É possível esconder os detalhes

- Tratar como stateless (não armazenar informações nem dados de sessão)

##### Desacoplamento
- Orientado a eventos
  - AWS Lambda - Responde a eventos da infraestrutura AWS (event driven, reactive)

- Orientado a serviços
  - gRPC
  - HTTP
  - Kafka
  - SQS
  - RabbitMQ

 ![picture 7](images/0f6f121009d50895cad49980c14085a7dd779036a10d53c5a4828bb1c15727f7.png)  

### Arquitetura AWS

![picture 8](images/893745b2c78e3cfe579b135d0ddd096b753435aec19484bfc663ea5f4bde52da.png)  


[AWS GCI](https://apps.kaonadn.net/5181491956940800/index.html)

  - AZ (Availability Zone)
    - Um ou mais datacenters
    - Arquiteturado para existir isolamento de falha (falha uma AZ, as outras não são afetadas)
    - Interconectadas com outras AZs usando links de altíssima velocidade
  - Regions
    - Localizações geográficas
    - Duas ou mais AZs
