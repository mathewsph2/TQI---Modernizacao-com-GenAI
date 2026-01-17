# Desafio de Projeto DRAWIO - Arquitetura AWS

Este projeto foi desenvolvido como parte do desafio proposto pela plataforma DIO, conforme o enunciado:

"Criar o desenho de nossa arquitetura com S3 / EC2 / Lambda Function usando o Drawio e disponibilizar no GitHub."

A arquitetura foi modelada utilizando os principais serviços da AWS, com foco em escalabilidade, modularidade e uso de componentes serverless. Abaixo está a explicação detalhada da estrutura representada no diagrama.

--- 
## Visão Geral da Arquitetura

A arquitetura proposta representa um sistema baseado em nuvem que utiliza os seguintes serviços da AWS:

- Amazon EC2 (Elastic Compute Cloud): instância de servidor que hospeda a aplicação principal ou backend.
- Amazon S3 (Simple Storage Service): serviço de armazenamento de objetos, utilizado para guardar arquivos estáticos ou dados processados.
- AWS Lambda: função serverless que executa tarefas específicas sob demanda, sem necessidade de provisionar servidores.
- Amazon EBS (Elastic Block Store): volume de armazenamento em bloco conectado à instância EC2.
- Client: interface de acesso do usuário, que pode ser um navegador ou aplicação desktop.
- Actor: representação do usuário final que interage com o sistema.

## 🔁 Fluxo de Interação

- Actor → Client: O usuário interage com o sistema por meio de uma interface cliente.
- Client → EC2: A aplicação cliente realiza requisições para o backend hospedado na instância EC2.
- EC2 → EBS: A instância EC2 acessa dados armazenados em volumes EBS para leitura ou escrita.
- EBS → Client: Os dados processados são retornados ao cliente.
- EC2 → Lambda: A instância EC2 pode invocar funções Lambda para tarefas específicas, como processamento assíncrono ou integração com outros serviços.
- EC2 → S3: A aplicação pode armazenar arquivos ou dados no S3, como logs, imagens ou documentos.

## 🎯 Justificativa Técnica

Essa arquitetura foi desenhada para atender aos seguintes requisitos do desafio:

- Uso de S3: armazenamento escalável e seguro para dados estáticos.
- Uso de EC2: controle total sobre o ambiente de execução da aplicação.
- Uso de Lambda Function: execução de tarefas sob demanda, reduzindo custos com infraestrutura.

Além disso, o uso de EBS complementa o armazenamento persistente da instância EC2, e a separação entre Client e Actor reforça a distinção entre interface e usuário.

---
## 🛠️ Ferramenta Utilizada
Drawio (www.drawio.com): ferramenta de diagramas utilizada para modelar visualmente a arquitetura.

## 📌 Conclusão
Este projeto representa uma arquitetura moderna e funcional baseada em serviços da AWS, com foco em modularidade e escalabilidade. O diagrama foi criado no Drawio conforme solicitado como parte do desafio proposto.
