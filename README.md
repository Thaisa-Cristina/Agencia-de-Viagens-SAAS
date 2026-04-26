# 🚀 Plataforma SaaS de Gestão de Excursões e Financeiro (EM CONSTRUÇÃO)

Sistema SaaS completo para gestão de **excursões, clientes, financeiro e operações**, desenvolvido com foco em **escalabilidade, automação e controle de negócios**.

A plataforma oferece uma visão centralizada das operações, permitindo o gerenciamento eficiente de viagens, clientes, receitas, despesas e tarefas, além de fornecer **dashboards interativos em tempo real** para tomada de decisão.

<img width="1897" height="865" alt="image" src="https://github.com/user-attachments/assets/3b8788d0-962d-4adb-a694-95169d2ac887" />


---

## 🎯 Objetivo

Desenvolver uma solução robusta para empresas de:

* Turismo e excursões
* Prestação de serviços
* Gestão financeira e operacional

Com foco em:

* 📊 **Controle financeiro**
* ⚙️ **Automação de processos**
* 📈 **Análise de dados**
* 🚀 **Escalabilidade (SaaS)**

---

## 🛠️ Tecnologias Utilizadas

### Backend

* Python
* FastAPI / Django
* SQLAlchemy / ORM
* JWT (autenticação)

### Frontend

* React
* Chart.js
* HTML, CSS, JavaScript

### Banco de Dados

* SQL Server

### Autenticação

* Keycloak
* OpenID Connect (OIDC)
* OAuth2

### Infraestrutura

* Docker
* REST API
* Arquitetura em camadas

---

## 🔐 Autenticação e Segurança

A plataforma utiliza o **Keycloak** como provedor de identidade (IAM), garantindo:

* Autenticação centralizada (SSO)
* Controle de acesso baseado em papéis (RBAC)
* Integração via OpenID Connect (OIDC)
* Tokens JWT para comunicação segura
* Gerenciamento de usuários e sessões

### 🔄 Fluxo de autenticação

1. Usuário realiza login via Keycloak
2. Recebe um token JWT
3. O frontend envia o token para a API
4. O backend valida e autoriza o acesso

---

## 🧠 Arquitetura

A aplicação segue uma arquitetura moderna e escalável:

* **Frontend:** React (SPA)
* **Backend:** API REST (FastAPI ou Django)
* **Autenticação:** Keycloak (OIDC / JWT)
* **Banco de Dados:** SQL Server
* **Infraestrutura:** Docker

### 📦 Estrutura do Projeto

```
app/
 ├── core/        # Configurações e banco
 ├── models/      # Modelos de dados (ORM)
 ├── schemas/     # Validação (Pydantic)
 ├── routes/      # Endpoints da API
 ├── services/    # Regras de negócio
 ├── static/      # Frontend (dashboard)
 └── main.py      # Inicialização da aplicação
```

---

## 🧩 Funcionalidades

### 📊 Dashboard

* Indicadores em tempo real (KPIs)
* Receita vs Despesa
* Status de viagens
* Tarefas pendentes

### 👥 Gestão de Clientes

* Cadastro de clientes
* Histórico de interações
* Contatos

### ✈️ Viagens / Excursões

* Cadastro e controle de viagens
* Status (andamento, finalizada)
* Controle de participantes

### 💰 Financeiro

* Contas a pagar
* Contas a receber
* Fluxo de caixa
* Controle de saldo

### 📄 Orçamentos

* Criação e acompanhamento
* Status (pendente, aprovado, vencido)

### 📅 Tarefas / Agenda

* Gestão de atividades
* Pendências e atrasos

### 🔐 Controle de Acesso

* Usuários
* Perfis
* Permissões

### 📢 Marketing (Futuro)

* Campanhas
* Comunicação com clientes

### 📱 Integração WhatsApp (Futuro)

* Notificações automáticas
* Alertas operacionais

---

## 🏢 Multi-Tenant (Planejado)

A aplicação será evoluída para suportar múltiplos clientes (tenants):

* Isolamento de dados por empresa
* Escalabilidade horizontal
* Personalização por cliente

---

## 🗄️ Modelagem de Dados

### Entidades principais:

* Users
* Clients
* Trips
* Financial Transactions
* Budgets
* Tasks

---

## 🔌 API (Exemplos)

### Autenticação

```
POST /auth/login
POST /auth/register
```

### Clientes

```
GET /clients
POST /clients
```

### Financeiro

```
GET /finance
POST /finance
```

### Viagens

```
GET /trips
POST /trips
```

---

## ⚙️ Como Executar o Projeto

### 🔧 1. Clonar repositório

```
git clone https://github.com/seu-usuario/seu-repo.git
cd seu-repo
```

---

### 🐍 2. Criar ambiente virtual

```
python -m venv venv
venv\Scripts\activate
```

---

### 📦 3. Instalar dependências

```
pip install -r requirements.txt
```

---

### 🐳 4. Subir SQL Server (Docker)

```
docker run --name sqlserver `
-e "ACCEPT_EULA=Y" `
-e "SA_PASSWORD=SuaSenhaForte123" `
-p 1433:1433 `
-d mcr.microsoft.com/mssql/server:2022-latest
```

---

### ▶️ 5. Rodar aplicação

```
uvicorn app.main:app --reload
```

ou (Django):

```
python manage.py runserver
```

---

## 🌐 Acessos

* API: http://127.0.0.1:8000
* Docs: http://127.0.0.1:8000/docs
* Dashboard: http://127.0.0.1:8000/static/index.html

---

## 🧪 Testes

* Testes unitários com Pytest
* Testes de API
* Validação de regras de negócio

---

## 📈 Observabilidade (Futuro)

* Monitoramento com Prometheus
* Dashboards com Grafana
* Logs estruturados
* Alertas automáticos

---

## 🔁 CI/CD (Planejado)

* GitHub Actions
* Build automatizado
* Deploy contínuo
* Containers Docker

---

## 📊 Roadmap

### 🔹 Fase 1

* CRUD completo
* Dashboard
* API REST

### 🔹 Fase 2

* Autenticação com Keycloak
* Multi-tenant

### 🔹 Fase 3

* Integração WhatsApp
* Notificações

### 🔹 Fase 4

* Deploy Cloud (AWS/Azure)
* CI/CD
* Sistema de assinatura SaaS

---

## 💡 Diferenciais

* Arquitetura escalável
* Separação de responsabilidades (Clean Code)
* Simulação de ambiente real (ERP + CRM + Financeiro)
* Segurança com Keycloak (SSO / JWT)
* Pronto para evolução SaaS

---

## 👨‍💻 Autor

**Thaisa Cristina**
Desenvolvedora Full Stack | Backend | Infraestrutura

---

## 📄 Licença

Este projeto está sob a licença MIT.
