# 🚀 FastAPI Investment API

API simples construída com **FastAPI** que permite consultar dados financeiros de ações usando a [Alpha Vantage API](https://www.alphavantage.co/). Este projeto tem fins educacionais e demonstra como integrar FastAPI com uma API externa para obter informações financeiras em tempo real.

---

## 📦 Funcionalidades

- Consulta de ações via ticker (ex: `AAPL`, `GOOGL`, `TSLA`)
- Retorno dos dados formatados em JSON
- Estrutura clara e moderna com **FastAPI**
- Integração com a API da **Alpha Vantage**

---

## 🛠 Tecnologias Utilizadas

- [FastAPI](https://fastapi.tiangolo.com/)
- [Uvicorn](https://www.uvicorn.org/)
- [Requests](https://pypi.org/project/requests/)
- Python 3.9+

---

## ▶️ Como Executar o Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/victorgoveia/fastapi-investment-api.git
cd fastapi-investment-api
```

### 2. Crie um ambiente virtual (opcional, mas recomendado)

```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
```

### 3. Instale as dependências

```bash
pip install -r requirements.txt
```

### 4. Inicie o servidor

```bash
uvicorn main:app --reload
```

A API estará disponível em:  
📍 `http://127.0.0.1:8000`

---

## 🔑 Como Usar a API

### 1. Obtenha uma chave gratuita da Alpha Vantage

- Acesse: [https://www.alphavantage.co/support/#api-key](https://www.alphavantage.co/support/#api-key)
- Clique em **"Get your free API key"**
- Você receberá uma chave por e-mail (algo como `demo123456ABCDEF`)

### 2. Faça uma requisição GET para a API local

#### Exemplo de uso:

```
GET http://127.0.0.1:8000/stock?ticker=AAPL&apikey=demo123456ABCDEF
```

#### Parâmetros:
- `ticker` → símbolo da ação (ex: `AAPL`, `TSLA`)
- `start_date` → data de início (ex: `2025-01-01`)
- `end_date` → data de fim (ex: `2025-04-01`)
- `apikey` → sua chave da Alpha Vantage

---

## 📥 Exemplo de Resposta

```json
{
  "data": "2024-01-01T00:00:00",
  "preco_fechamento": 402.79,
}
```

---