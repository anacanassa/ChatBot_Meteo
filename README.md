# Projeto: Chatbot Meteorológico com Gemini + Open-Meteo

Este projeto implementa um **chatbot inteligente de clima**, utilizando:

- **Gemini API** para interpretar perguntas em linguagem natural  
- **Open-Meteo API** para buscar previsões do tempo  
- Suporte a datas relativas ("hoje", "amanhã", "ontem", "atual")  
- Consulta automática das coordenadas da cidade via **Geocoding API**

O repositório contém dois arquivos principais:

- `chatbot.py` → versão executável em Python puro  
- `chatbot.ipynb` → versão interativa no Google Colab / Jupyter Notebook  

---

## Funcionalidades

- Interpretação de perguntas como:
  - “Vai chover amanhã?”
  - “Temperatura atual no Rio de Janeiro”
  - “Clima em Curitiba na próxima segunda-feira?”
- Extração automática de:
  - Cidade  
  - Data (absoluta ou relativa)  
  - Tipo de dado climático  
- Correção automática de datas relativas  
- Consulta das coordenadas da cidade via Geocoding  
- Consulta da previsão real via Open-Meteo  

---

## Instalação

### Pré-requisitos
- Python **3.10+**
- Pip atualizado
- Uma **API Key do Google Gemini**: https://aistudio.google.com

---

### Clonar o repositório

```bash
git clone https://github.com/SEU_USUARIO/SEU_REPO.git
cd SEU_REPO
```

### Instalar dependências

```bash
pip install google-genai requests
```

## Execução

```bash
python chatbot.py
```

## Rodando o Notebook chatbot.ipynb

Abra localmente no Jupyter

Ou envie para o Google Colab: https://colab.research.google.com

O notebook já inclui:

- Instalação das libs

- Configuração da API Key

- Execução interativa do chatbot
