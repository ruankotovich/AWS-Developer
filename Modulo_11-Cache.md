# Módulo 11

## Caching

- Melhorar a velocidade da aplicação
- Reduz a latência das respostas
- Aliviar a carga de queries demoradas
- Provê um enorme ganho de performance

### Quando utilizar
-  Data requer uma operação lenta ao ser adquiridos (SAP :P)
-  Dados relativamente estáticos e frequentemente acessados (perfil de rede social)
-  Informações que podem ficar antigas por algum tempo (previsão climática)

## Amazon ElastiCache

![picture 7](images/10376e0724c64a7b8fd5f9b51596b7640220448b060890a1cd2fb620ec91a4e6.png)  

### Memcached vs Redis

![picture 8](images/2104c93bdc840c09b93d0c55b9c7fb245520ccc91cb6a6b39b5afad1c24281c3.png)  


- Cache miss
  - Tentou encontrar no cache e não encontrou, busca no banco
- Cache hit
  - Encontrou no cache

### Caching strategies

#### Lazy Load
- Trabalha em cima do cache miss
- Lê da aplicação, entrega para o usuário, e escreve no cache
- Pode trazer dados antigos

#### Write Through
- Escreve no banco, escreve na cache
- Penalidade na escrita