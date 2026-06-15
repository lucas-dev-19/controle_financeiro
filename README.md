# 💰 Controle Financeiro Pessoal

> Aplicacao web completa para gestao financeira pessoal, construida com Python e Streamlit.

![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python)
![Streamlit](https://img.shields.io/badge/Streamlit-1.35+-red?logo=streamlit)
![SQLite](https://img.shields.io/badge/SQLite-3-green?logo=sqlite)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## Funcionalidades

### Nivel 1 — Essencial
- Cadastro de receitas e despesas
- Edicao e exclusao de lancamentos
- 11 categorias padrao (Alimentacao, Transporte, Moradia, Lazer, Educacao, Saude e mais)
- Dashboard com saldo atual, receitas, despesas e economia do mes
- Historico com filtros por periodo, categoria e conta
- Persistencia com SQLite (sem JSON em producao)

### Nivel 2 — Diferencial
- Graficos interativos: pizza por categoria, barras receitas vs despesas, area de evolucao
- Metas financeiras com barra de progresso e depositos
- Multiplas contas (Carteira, Conta Corrente, Poupanca, Investimento)
- Transferencia entre contas com controle de saldo

### Nivel 3 — Portfolio Forte
- Login com cadastro, autenticacao e logout
- Senhas protegidas com hash bcrypt
- Relatorios em PDF formatados com ReportLab
- Exportacao CSV e Excel
- Multi-usuario com dados isolados por conta

### Nivel 4 — Diferencial de Destaque
- **IA Financeira (FinBot)**: faca perguntas em linguagem natural e receba analises personalizadas
- **Insights automaticos**: o sistema analisa seus dados e gera recomendacoes
- Exemplos de perguntas:
  - "Gastei muito esse mes?"
  - "Em qual categoria estou gastando mais?"
  - "Como esta minha economia comparada ao mes passado?"

---

## Tecnologias

| Tecnologia   | Uso                                      |
|--------------|------------------------------------------|
| Python 3.11+ | Linguagem principal                      |
| Streamlit    | Interface web                            |
| SQLite       | Banco de dados local                     |
| Pandas       | Manipulacao de dados e exportacao        |
| Plotly       | Graficos interativos                     |
| Matplotlib   | Graficos estaticos                       |
| ReportLab    | Geracao de PDF                           |
| bcrypt       | Hash seguro de senhas                    |
| openpyxl     | Exportacao para Excel                    |

---

## Estrutura do Projeto

```
controle_financeiro/
|-- app.py                  # Ponto de entrada
|-- database.py             # Conexao e criacao do banco
|-- models.py               # Dataclasses e constantes
|-- services/
|   |-- auth.py             # Autenticacao e usuarios
|   |-- transacoes.py       # CRUD de transacoes e contas
|   |-- metas.py            # Metas financeiras
|   |-- relatorios.py       # PDF, CSV e Excel
|-- pages/
|   |-- dashboard.py        # Visao geral e graficos
|   |-- transacoes.py       # Lancamentos e historico
|   |-- metas.py            # Gestao de metas
|   |-- relatorios.py       # Exportacao e IA financeira
|-- database/
|   |-- financeiro.db       # Banco SQLite (gerado automaticamente)
|-- assets/
|-- requirements.txt
|-- README.md
|-- .gitignore
```

---

## Como Executar

### Pre-requisitos
- Python 3.11 ou superior
- pip

### Instalacao

```bash
# 1. Clone o repositorio
git clone https://github.com/seu-usuario/controle-financeiro.git
cd controle-financeiro

# 2. Crie e ative o ambiente virtual
python -m venv venv

# Windows
venv\Scripts\activate

# Linux/Mac
source venv/bin/activate

# 3. Instale as dependencias
pip install -r requirements.txt

# 4. Execute a aplicacao
streamlit run app.py
```

A aplicacao abrira automaticamente em `http://localhost:8501`

### Primeiro Acesso
1. Clique em **Criar Conta**
2. Preencha nome, e-mail e senha
3. Faca login
4. Comece a registrar suas transacoes!

---

## Screenshots

> Dashboard com metricas, graficos de pizza e evolucao de saldo  
> Pagina de transacoes com historico filtrado e indicadores visuais  
> Metas financeiras com barra de progresso  
> IA Financeira com analise personalizada em tempo real

---

## Contribuindo

Pull requests sao bem-vindos. Para mudancas grandes, abra uma issue primeiro.

---

## Licenca

[MIT](LICENSE)

---

Desenvolvido com Python e Streamlit
