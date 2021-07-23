# Módulo 7

## Serverless Computing
- Não gerenciar servidor
- Escala com a utilização
- Não pagar por inatividade
- Disponível e tolerante a falhas

![picture 2](images/9ae1b0c8d01d2fe6fa47ce855811263301e216018f5c04a85f56ec17922cd640.png)  

### AWS Serverless Platform

![picture 3](images/11f8f885e06d46f3c739fcc016210aa0a625968e49cba7bdc65d0785c76012ac.png)  


## AWS Lambda
- Serviço de computação serverless sem provisionar um servidor
- "FUNCTION AS A CODE"

![picture 4](images/4cd584414dde40ccc1ed9e14f099934831488e3d5307685ba9ab14996624f365.png)  

- Integra nativamente com outros serviços da AWS
- Runtime [Firecracker](https://firecracker-microvm.github.io/)

![picture 5](images/b41217ddb826c8fb81fe955551d72c32fae54b06a60bb2c9f30fef4baeb99096.png)  

- Variáveis de Ambiente
- Diferentes Runtime
- Ferramentas de monitoramento
- Publicação de Logs pro CloudWatch

### Execution Model
![picture 1](images/d726d976f18ef2bd0bfbf7789116645774f89a7adbb6678f520fca5899481746.png)  


### Política de acesso
1. Role
2. Permissões para assumir a Role
3. Attach da permissão

### Scheduling
-   Fixar uma expressão (minuto, hora)
-   Cronjob (1/2 * * * *), qualquer combinação