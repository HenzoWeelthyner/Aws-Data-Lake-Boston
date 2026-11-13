# AWS Data Lake — Boston

## Sobre o projeto

Este projeto tem como objetivo desenvolver uma etapa de ingestão de dados para um Data Lake na AWS, utilizando Python, Pandas, Boto3 e Amazon S3.

O projeto utiliza dados abertos da cidade de Boston, abrangendo os anos de 2015 a 2020.

## Tecnologias utilizadas

- Python
- Google Colab
- Pandas
- Boto3
- Amazon S3
- Apache Parquet

## Etapas implementadas

1. Extração de arquivos CSV do portal de dados abertos de Boston.
2. Leitura e organização dos dados utilizando Pandas.
3. Configuração da conexão com a AWS por meio do Boto3.
4. Conversão dos arquivos CSV para o formato Parquet.
5. Envio dos arquivos para a camada Bronze no Amazon S3.
6. Verificação dos objetos armazenados no bucket.

## Arquitetura do projeto

O fluxo de ingestão de dados implementado segue esta sequência:

**Portal de dados abertos de Boston → Python/Pandas → Conversão para Parquet → Boto3 → Amazon S3 (Bronze).**

## Organização do repositório

```text
aws-data-lake-boston/
│
├── notebooks/
│   └── Pipeline_AWS.ipynb
│
├── imagens/
│   ├── CloudWatch.png
│   ├── S3_Bucket.png
│   ├── S3_Dados.png
│   └── S3_Objetos.png
│
├── README.md
└── requirements.txt
```

## Como executar o projeto

1. Acesse o notebook localizado em `notebooks/Pipeline_AWS.ipynb`.
2. Abra o arquivo no Google Colab.
3. Instale as dependências necessárias:

```bash
pip install -r requirements.txt
```

4. Configure suas credenciais AWS utilizando os Secrets do Google Colab.
5. Execute as células do notebook para realizar a ingestão e o armazenamento dos dados no Amazon S3.

**Importante:** é necessário possuir uma conta AWS com as permissões adequadas para acessar o Amazon S3.

## Segurança

As credenciais de acesso à AWS são armazenadas nos Secrets do Google Colab e não devem ser compartilhadas ou publicadas no repositório.

Nunca publique Access Keys, Secret Keys, tokens ou outras informações confidenciais.

## Status do projeto

A etapa de ingestão e armazenamento dos dados na camada Bronze está implementada.

O projeto poderá receber novas etapas de processamento e transformação de dados conforme sua evolução.