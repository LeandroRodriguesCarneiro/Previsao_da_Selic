# Previsao_da_Selic
Plataforma end-to-end de Engenharia de Dados e Machine Learning para ingestão, processamento, análise e previsão de indicadores macroeconômicos brasileiros como SELIC, IPCA, IGPM e Dólar (USD/BRL).

O projeto implementa uma arquitetura moderna baseada em Data Lakehouse + MLOps, transformando dados econômicos brutos em previsões automatizadas e visualizações analíticas.

## 🚀 Visão Geral do Projeto

A Previsao_da_Selic realiza automaticamente:

- Coleta de dados econômicos via API do Banco Central
- Processamento em múltiplas camadas (Bronze, Silver e Gold)
- Validação de qualidade dos dados
- Engenharia de atributos
- Treinamento e versionamento de modelos preditivos
- Disponibilização de previsões via API
- Visualização em dashboard interativo

O objetivo é simular uma plataforma real de dados utilizada em instituições financeiras.

## 🏗️ Arquitetura da Solução

![Texto alternativo](pictures/Arquitetura.drawio.png)

## 🧱 Arquitetura de Dados
A arquetura de dados do projeto utiliza Arquitetura de Medalhão

### 🥉 Camada Bronze

Armazena os dados brutos extraídos da API do Banco Central.
Indicadores coletados:
- Taxa SELIC
- IPCA
- IGPM
- Cotação do Dólar

Formato de armazenamento:
- Arquivos Parquet
- Dados históricos completos
- Sem transformações

### 🥈 Camada Silver

Dados tratados e padronizados.
Transformações realizadas:
- Normalização temporal
- Tratamento de valores ausentes
- Padronização de frequências
- Correção de tipos de dados

### 🥇 Camada Gold

Dados prontos para consumo analítico e Machine Learning.
Inclui:

- Junção dos indicadores econômicos
- Features temporais
- Variáveis defasadas (lags)
- Médias móveis

Dataset final para treinamento

