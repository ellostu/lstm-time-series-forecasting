# LSTM Forecasting of IoT System Requests

Este projeto implementa um pipeline completo de previsão de séries temporais baseado em LSTM (Long Short-Term Memory) usando dados reais de um sistema IoT monitorado em data centers. Ele foi desenvolvido com o objetivo de consolidar habilidades fundamentais em IA e Cloud aplicadas ao mundo real.

## 💼 Contexto Profissional

Este repositório faz parte do meu portfólio técnico voltado para oportunidades em Data Science, IA e Cloud Computing, com interesse especial em projetos que envolvam escalabilidade, séries temporais e aplicações em engenharia de sistemas.

## 📊 Objetivo

Prever a quantidade de requisições futuras com base no histórico de métricas extraídas de arquivos CSV disponibilizados pelo [SIR Lab - data-release](https://github.com/sir-lab/data-release).

## 🧠 Habilidades Demonstradas

- **Processamento de Dados com Pandas**:
  - Leitura eficiente de múltiplos arquivos
  - Tratamento de NaNs e estruturação de DataFrames
- **Engenharia de Features Temporais**:
  - Construção de índices datetime
  - Criação de sequências (janelas temporais) para treinamento
- **Modelagem com Redes Neurais (Keras + TensorFlow)**:
  - Construção e treino de modelo LSTM com Dropout
  - Definição correta de input shape
  - Avaliação com loss e val_loss
- **Validação Temporal**:
  - Divisão treino/validação/teste cronológica
  - Visualização gráfica das previsões

## 🔧 Como Rodar

Crie um ambiente virtual (opcional, mas recomendado):

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
