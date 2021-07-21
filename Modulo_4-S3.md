# Módulo 4

## Opções de Armazenamento

- S3
  - "uma biblioteca"
    - Bucket = Prateleira
    - Object = Livro
    - Revisão do livro -> Versão do Objeto
- S3 Glacier
  - Long-term storage
  - Baixo custo para armazenamento de longa data, durabilidade alta
  - Não tem disponibilidade instantânea (demora de 1 minutos até 12 horas pra ficar disponível)
    - Expedited - 1 a 5 minutos ($$$)
    - Standard - 3 a 5 horas ($$)
    - Bulk - até 12 horas ($)
- EFS
  - Multiplos acessos
  - Mount point
- Storage Gateway
  - Armazenamento virtualmente ilimitado
- EBS
  - Montado via network
  - Armazenamento de bloco de longa data
