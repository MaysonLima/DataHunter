#  DataHunter

Sistema completo de **data scraping e engenharia de dados**, responsável por coletar, processar, armazenar e disponibilizar dados de múltiplas fontes através de uma API e um dashboard interativo.

---

##  Visão Geral

O **DataHunter** simula um pipeline real de dados utilizado em empresas:

1. Coleta dados de diferentes sites (web scraping)
2. Realiza limpeza e transformação dos dados
3. Armazena em banco de dados
4. Disponibiliza via API REST
5. Exibe visualmente em um dashboard
6. Executa de forma automatizada e monitorada

---

##  Objetivo

Este projeto foi desenvolvido com foco em:

* Demonstrar habilidades práticas em **engenharia de dados**
* Trabalhar com **scraping real de múltiplas fontes**
* Aplicar boas práticas de **arquitetura e organização de código**
* Construir um projeto próximo de um ambiente profissional

---

##  Funcionalidades

- Scraping de múltiplas fontes
- Uso de XPath para extração de dados
- Tratamento e padronização com Pandas
- Armazenamento em banco de dados relacional
- API REST para consumo dos dados
- Dashboard para visualização
- Execução automática (jobs agendados)
- Sistema de logs e monitoramento
- Validação para detectar falhas no scraping

---

##  Stack Tecnológica

### Backend & Data

* Python
* BeautifulSoup 
* Pandas
* PostgreSQL 

### API

* FastAPI

### Frontend

* React 

### Infra & Automação

* Cron Jobs 
* Logging
* Docker 

---

##  Arquitetura

O projeto segue uma arquitetura modular baseada em camadas:

```
Data Sources 
        ↓
Scrapers 
        ↓
Data Processing (Pandas)
        ↓
Database (PostgreSQL)
        ↓
API (FastAPI)
        ↓
Frontend Dashboard
```

### Princípios aplicados:

* Separação de responsabilidades (SRP)
* Código modular e escalável
* Facilidade de manutenção
* Reutilização de componentes

---

##  Estrutura do Projeto 

```
datahunter/
│
├── scrapers/        # Scripts de coleta de dados
├── processors/      # Limpeza e transformação dos dados
├── database/        # Conexão e models do banco
├── api/             # API REST
├── frontend/        # Dashboard
├── jobs/            # Automação / agendamentos
├── logs/            # Logs do sistema
├── tests/           # Testes
└── main.py          # Orquestrador principal
```

---

##  Como Rodar o Projeto

### 1. Clonar o repositório

```bash
git clone https://github.com/seu-usuario/datahunter.git
cd datahunter
```

### 2. Criar ambiente virtual

```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
```

### 3. Instalar dependências

```bash
pip install -r requirements.txt
```

### 4. Configurar variáveis de ambiente

Crie um arquivo `.env`:

```
DATABASE_URL=sqlite:///data.db
```

---

### 5. Rodar o scraping

```bash
python main.py
```

---

### 6. Iniciar API

```bash
uvicorn api.main:app --reload
```

Acesse:

```
http://localhost:8000/docs
```

---

### 7. Rodar o frontend

```bash
cd frontend
npm install
npm start
```

---

##  Exemplos de Uso

### Buscar dados via API

```bash
GET /data
```

### Filtrar dados

```bash
GET /data?source=site1
```

---

##  Exemplos de Dados

```json
{
  "title": "Produto X",
  "price": 199.90,
  "source": "site1",
  "collected_at": "2026-04-04T12:00:00"
}
```

---

##  Automação

O sistema pode ser configurado para rodar automaticamente:

* Via **cron jobs**
* Ou utilizando schedulers em Python

Exemplo:

```bash
0 * * * * python main.py
```

(Roda a cada hora)

---

##  Testes

```bash
pytest
```

##  Autor

Mayson Lima dos Santos - Projeto desenvolvido como projeto de portfólio para engenharia de dados.

---

##  Licença

MIT

