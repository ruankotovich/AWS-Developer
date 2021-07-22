# Módulo 4

## Overview das opções de Armazenamento

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


**OBS**: é possível rodar SQL no S3 (?????)

## Componentes do S3
- Escopo regional
  - `https://<bucket_name>.s3.<region_endpoint>.amazonaws.com`
  - Não existem 2 buckets no mundo todo da AWS com o mesmo nome
- Criptografia embutida de dados
- Object lock - WORK (previne que objetos sejam sobreescritos ou deletados por tempo determinado ou para sempre)

### Casos de uso
- Armazenamento de mídia
- Host de site estático
- Recuperação de sinistros
- Análise de big data
- Backup e arquivamento (nosso caso)

### Operações
  - PUT
    - Upload de objetos
    - Copia do objeto
      - Cria uma cópia
      - Renomeia o objeto criando uma cópia e deletando o original
      - Move objetos entre as locations do S3
    - No máximo 5GB em um upload simples
    - No máximo 5TB em um upload multipart (piecewise)
    - Mantém o estado do upload
      - Quando o upload é interrompido, os metadados dizem de onde continuar
  - GET
    - Completo
    - Piecewise (range of bytes)