# SynHand

![SynHand Logo](<img width="1280" height="320" alt="Prioritize your health" src="https://github.com/user-attachments/assets/733ab809-9083-4169-ac02-69b8d1a332ed" />
)

**SynHand** é um MVP de backend para reconhecimento de sinais de Libras
a partir de vídeos ou keypoints extraídos com MediaPipe. O objetivo é
traduzir gestos em texto, criando uma solução de acessibilidade com
inteligência artificial.

------------------------------------------------------------------------

## 🌟 Funcionalidades do MVP

-   Extração de keypoints de mãos usando **MediaPipe**\
-   Normalização dos dados para treinamento\
-   Treinamento de modelo simples (**RandomForest**) para classificação
    de sinais\
-   API em **FastAPI** para predição em tempo real

------------------------------------------------------------------------

## 📁 Estrutura do Projeto

    libras-ai/
    │
    ├── src/
    │   ├── data/               # Datasets (raw, processed, samples)
    │   ├── models/             # Modelos treinados e scripts de treino
    │   ├── preprocessing/      # Scripts de extração e normalização de keypoints
    │   ├── inference/          # Scripts de predição
    │   ├── api/                # FastAPI endpoints
    │   └── utils/              # Funções auxiliares e configuração
    │
    ├── notebooks/              # Protótipos e testes
    ├── requirements.txt        # Dependências do projeto
    ├── README.md
    └── .gitignore

------------------------------------------------------------------------

## 🚀 Como rodar o projeto

### 1. Criar ambiente virtual

``` bash
python -m venv venv
source venv/bin/activate  # Linux / Mac
venv\Scriptsctivate     # Windows
```

### 2. Instalar dependências

``` bash
pip install -r requirements.txt
```

### 3. Treinar modelo

``` bash
python src/models/training/train_model.py
```

### 4. Rodar API FastAPI

``` bash
uvicorn src.api.main:app --reload
```

Agora a API estará disponível em `http://127.0.0.1:8000/predict`.

------------------------------------------------------------------------

## 🛠 Tecnologias Utilizadas

-   Python 3.10+\
-   MediaPipe (extração de keypoints)\
-   OpenCV (processamento de vídeo)\
-   scikit-learn (modelo RandomForest)\
-   FastAPI (API backend)\
-   NumPy (manipulação de dados)

------------------------------------------------------------------------

## 🎯 Próximos Passos

-   Treinar modelos mais avançados (LSTM / Transformer)\
-   Implementar módulo de voz → Libras\
-   Criar interface web / mobile\
-   Implementar pipeline em tempo real com webcam

------------------------------------------------------------------------

## 📄 Licença

Este projeto está sob a licença **MIT**.
