# dio-live-serverless-project
 
# API Serverless com Node.js na AWS

Este projeto demonstra a criação de uma API REST serverless utilizando Node.js, o Serverless Framework e os serviços da AWS. A API é construída com AWS API Gateway, AWS Lambda e DynamoDB, e a infraestrutura é provisionada usando AWS CloudFormation.

## Pré-requisitos

- Conta na AWS
- Node.js instalado
- AWS CLI instalado e configurado

## Primeiros Passos

1. Clone o repositório:

 ```bash
   git clone https://github.com/seu-usuario/dio-live-serverless-project.git


## Instale o Serverless Framework globalmente:

 ```bash
 npm install -g serverless
 ```

## Instale as dependências do projeto:

 ```bash
cd seu-repo
npm install
 ```


## Faça o deploy do projeto:

 ```bash
serverless deploy
 ```



## Estrutura do Projeto

O projeto segue a seguinte estrutura:

 ```bash
├── src
│   ├── hello.js         # Função Lambda para lidar com o endpoint raiz
│   ├── insertItem.js    # Função Lambda para inserir um item
│   ├── fetchItems.js    # Função Lambda para buscar todos os itens
│   ├── fetchItem.js     # Função Lambda para buscar um item específico
│   └── updateItem.js    # Função Lambda para atualizar um item
├── serverless.yml       # Arquivo de configuração do Serverless Framework
└── package.json         # Dependências e scripts do Node.js
 ```

O diretório src contém o código das funções Lambda para os diferentes endpoints.
serverless.yml é o arquivo de configuração do Serverless Framework que define a infraestrutura e as configurações das funções.
package.json lista as dependências do Node.js e os scripts do projeto.

## Utilização

Os endpoints da API são criados e gerenciados automaticamente pelo AWS API Gateway. Após fazer o deploy do projeto, você pode acessar os endpoints utilizando as URLs fornecidas. Os endpoints disponíveis são:

 ```bash
    GET / - Endpoint raiz que aciona a função hello.
    POST /item - Endpoint para inserir um novo item.
    GET /items - Endpoint para buscar todos os itens.
    GET /items/{id} - Endpoint para buscar um item específico.
    PUT /items/{id} - Endpoint para atualizar um item específico.
  ```