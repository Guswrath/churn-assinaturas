# Análise de cancelamento de clientes

Projeto educacional de Data Science com a base pública de exemplo
IBM Telco Customer Churn.

## Objetivo

Investigar características associadas ao cancelamento e, posteriormente,
comparar regressão logística e árvore de decisão.

## Dados

- Fonte: https://github.com/IBM/telco-customer-churn-on-icp4d
- O repositório de origem declara licença Apache 2.0.
- Base com 7.043 registros e 21 colunas.
- Target: Churn, com Yes para cancelamento e No para não cancelamento.

## Etapas concluídas

- Ingestão e diagnóstico inicial de qualidade.
- Separação em treino, validação e teste.
- Verificação de ausência de clientes compartilhados entre os conjuntos.
- Análise exploratória no treino por contrato e tempo de relacionamento.

## Arquivos principais

- 01_exploracao_churn.ipynb: exploração e verificações.
- requirements.txt: pacotes e versões do ambiente.
- .gitignore: regras de exclusão do versionamento.

## Limitações

As análises são exploratórias e não demonstram causalidade.
A base não permite reconstruir um instante de previsão confiável;
o projeto não comprova capacidade de prever cancelamentos futuros.

## Status

Em desenvolvimento. Modelos ainda não treinados.