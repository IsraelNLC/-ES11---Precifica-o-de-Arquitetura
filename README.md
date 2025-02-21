# Ponderada da Semana 3: Precificação de Arquitetura

## Racional dos Custos dos Serviços AWS

Conforme a arquitetura do projetos, escolhemos os serviços Amazon EC2 e Amazon S3 para garantir a eficiência e escalabilidade do processamento e armazenamento de dados. Abaixo está o racional por trás dos custos associados a cada serviço utilizado:

### 1. Amazon EC2
O Amazon EC2 é utilizado para fornecer capacidade computacional escalável na nuvem. No contexto deste projeto, as instâncias EC2 são configuradas para processar grandes volumes de dados, conforme descrito no escopo do projeto no documento TAPI.pdf. Os custos do EC2 são baseados no tipo de instância utilizada, no tempo de execução e na capacidade de armazenamento temporário necessário para o processamento dos dados.

- **Tipo de Instância**: Foi escolhida a instância `t4g.nano`, que é econômica e eficiente para cargas de trabalho consistentes, como servidores de cliquehouse, rabbitmq, streamlit e fastapi.

- **Localização**: As instâncias estão localizadas na região US East (N. Virginia), aproveitando o menor custo em hospedar nessa localização.

- **Configuração**: Utiliza instâncias compartilhadas com sistema operacional Linux, otimizando custos e mantendo a flexibilidade necessária para o projeto.

### 2. Amazon S3
O Amazon S3 é utilizado para armazenamento de dados brutos e processados. Ele oferece uma solução escalável e econômica para armazenar grandes volumes de dados, com alta durabilidade e disponibilidade. Os custos são baseados no volume de dados armazenados e nas operações realizadas (como upload e download de dados).

- **Armazenamento**: Utilizamos o S3 Standard para armazenar dados de forma confiável e acessível. O armazenamento de 1 GB por mês é suficiente para os dados brutos e processados do projeto.
- **Operações**: As operações PUT, COPY, POST, LIST e GET são configuradas para atender às necessidades do projeto, com um limite de 256.000 solicitações.
- **Segurança e Compliance**: Implementamos políticas de segurança para garantir que os dados armazenados no S3 estejam protegidos e em conformidade com as regulamentações aplicáveis.