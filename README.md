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

Primeira versão de modelagem concluída: baseline, regressão logística
e árvore de decisão foram avaliados na validação.

A regressão logística com limiar 0,50 foi escolhida antes da avaliação
final, considerando pesos iguais para os dois tipos de erro.
Essa premissa é didática e não representa custos empresariais validados.

### Resultado no teste

- Acurácia: 80,3%.
- Recall de cancelamento: 55,6%.
- Precisão dos alertas: 65,2%.
- Cancelamentos identificados: 208 de 374.
- Cancelamentos não identificados: 166.
- Alertas incorretos: 111.

O resultado não comprova capacidade de antecipar cancelamentos futuros
nem retorno financeiro de ações de retenção.

### Próximas melhorias

- Organizar o notebook e o código reutilizável.
- Adicionar verificações automatizadas.
- Validar a execução em outros computadores ou sistemas.

## Execução no Windows — PowerShell

Pré-requisitos: Python instalado e acesso à internet.
A ingestão consulta um CSV público hospedado no GitHub.

Com o projeto disponível no computador, abra um terminal na pasta
que contém requirements.txt e execute:

### 1. Criar o ambiente virtual

```powershell
python -m venv .venv
```

### 2. Instalar as dependências

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

### 3. Abrir o JupyterLab

```powershell
.\.venv\Scripts\python.exe -m jupyterlab
```

No navegador, abra 01_exploracao_churn.ipynb e selecione
Run → Run All Cells para executar as células em ordem.

### Validação da execução

As dependências foram reinstaladas a partir de requirements.txt
em um ambiente virtual separado, usando Python 3.13.5 no Windows.

O notebook foi executado integralmente com o kernel desse ambiente,
após reinicialização, sem erros e mantendo as métricas finais reportadas.

Essa verificação foi realizada no mesmo computador do desenvolvimento.
A execução em outros sistemas e versões de Python ainda não foi validada.