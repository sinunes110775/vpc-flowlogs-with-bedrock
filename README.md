# Análise de VPC Flow Logs com Amazon Bedrock usando Linguagem Natural

Este repositório contém os artefatos utilizados no blogpost **“Como analisar VPC Flow Logs com Amazon Bedrock usando consultas em linguagem natural”**, que demonstra como equipes de segurança e infraestrutura podem transformar perguntas em linguagem natural em consultas SQL para analisar logs de rede, sem a necessidade de conhecimento avançado em SQL.

## Visão Geral

A solução combina os seguintes serviços da AWS:

- **Amazon Bedrock + Claude 3 Haiku**: converte perguntas em linguagem natural para SQL
- **Amazon Athena**: executa as consultas sobre os logs
- **AWS Lambda**: processa e retorna os resultados
- **VPC Flow Logs + Amazon S3 + AWS Glue**: fonte e estrutura dos dados
- **Amazon Bedrock Guardrails**: restringe temas não permitidos nas consultas

---

## 📁 Estrutura do Repositório

├── cloudformation/
│ └── bedrock-agent-lambda.yaml # Template para criar a função Lambda e permissões associadas
├── prompts/
│ ├── prompt-template.txt # Exemplo de template de prompt usado pelo agente
│ └── instrucoes-para-agente.txt # Instruções detalhadas para o agente Bedrock
├── schemas/
│ └── inline-OpenAPI-schema.json # Esquema OpenAPI usado para definir o action group do agente
├── images/
│ └── *.png # Capturas de tela usadas no blogpost
└── README.md # Este arquivo
