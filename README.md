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

## Fluxo de Interação do Chatbot

### Usuário faz uma pergunta
Exemplo:
**Usuário:** "Vai chover amanhã no Rio de Janeiro?"

### Sistema interpreta a pergunta (Gemini)
Retorno:
```json
{
  "city": "Rio de Janeiro",
  "date": "amanha",
  "info": "weathercode"
}
```
## Sistema converte a data relativa

"amanhã" → 2025-12-13

## Sistema busca coordenadas da cidade

Rio de Janeiro → (-22.9068, -43.1729)

## Sistema consulta Open-Meteo

Retorna: weathercode = 0 (céu limpo)

## esposta final exibida ao usuário

Bot: "A condição climática em Rio de Janeiro em 2025-12-13 será: Céu limpo."
