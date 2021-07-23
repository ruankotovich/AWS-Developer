# Módulo 13

## DevOps
- Filosofia cultural de compartilhamento de responsabilidade
- Visibilidade e comunicação entre a equipe como um todo
- Microsserviços
- CI/CD

## CI/CD
- Processo de construção de software
![picture 20](images/54017ab580c0a1d3b1a0796410a2f3f49907ab1818bf710d53bc8b2a8e98a0ea.png)  

- IaaC
  - Todos os recursos para rodar a aplicação disponíveis e configuradas
    - Infraestrutura

## AWS Code Services

![picture 21](images/fda6071234f28e7d2b64b901f6a9f3702a7f3fcfd9bed2db7a49cf435e56912a.png)  


- AWS CodeCommit
  - Repositório centralizado
  - Escalável
- AWS CodeBuild
  - Gera um servidor de build (Servless)
  - Build Spec 
    - Parametrizar todo o processo de construção 
    - Instalar dependências
- AWS CodePipeline
  - Criar uma esteira CI/CD de forma interativa, visual e centralizada
  - Controlar as etapas do processo, transição, ações em paralelo entre as etapas
  - Notificação quando é necessário aprovação manual
  - Notificação quando é encontrado um erro
- AWS CodeStar
  - Ferramenta de gerenciamento de projeto
  - Todos os outros centralizados em um dashboard
- AWS CodeDeploy
  - Implementar o artefato no servidor (deploy)
  - Hooks
    - Testar antes de implementar
    - 