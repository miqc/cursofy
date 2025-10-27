# Como Executar o Projeto Cursofy

Este guia fornece instruções detalhadas para configurar e executar o projeto Cursofy localmente.

---

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter instalado:

### Requisitos Obrigatórios
- **Node.js** 18.x ou superior
- **Python** 3.11 ou superior
- **PostgreSQL** 14.x ou superior
- **Redis** 6.x ou superior
- **Git**

### Ferramentas Recomendadas
- **Docker** e **Docker Compose** (opcional, mas recomendado)
- **VS Code** com extensões Python e TypeScript
- **Postman** ou **Insomnia** para testes de API

---

## 🐳 Opção 1: Executar com Docker (Recomendado)

### 1. Clone o Repositório
```bash
git clone https://github.com/seu-usuario/cursofy.git
cd cursofy
```

### 2. Configure as Variáveis de Ambiente
```bash
# Copie os arquivos de exemplo
cp frontend/.env.example frontend/.env.local
cp backend/.env.example backend/.env
```

### 3. Inicie os Containers
```bash
docker-compose up -d
```

### 4. Execute as Migrações
```bash
docker-compose exec backend python manage.py migrate
```

### 5. Crie um Superusuário
```bash
docker-compose exec backend python manage.py createsuperuser
```

### 6. Acesse a Aplicação
- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:8000
- **Admin Django**: http://localhost:8000/admin

### Comandos Úteis Docker
```bash
# Ver logs
docker-compose logs -f

# Parar containers
docker-compose down

# Rebuild containers
docker-compose up --build

# Executar testes
docker-compose exec backend pytest
docker-compose exec frontend npm test
```

---

## 💻 Opção 2: Executar Localmente (Sem Docker)

### Backend (Django)

#### 1. Navegue até a pasta do backend
```bash
cd backend
```

#### 2. Crie um ambiente virtual
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/Mac
python3 -m venv venv
source venv/bin/activate
```

#### 3. Instale as dependências
```bash
pip install -r requirements.txt
```

#### 4. Configure o PostgreSQL
```bash
# Crie o banco de dados
createdb cursofy

# Ou via psql
psql -U postgres
CREATE DATABASE cursofy;
\q
```

#### 5. Configure as variáveis de ambiente
```bash
# Crie o arquivo .env
cp .env.example .env

# Edite o .env com suas configurações
DATABASE_URL=postgresql://postgres:senha@localhost:5432/cursofy
SECRET_KEY=sua-chave-secreta-aqui
DEBUG=True
```

#### 6. Execute as migrações
```bash
python manage.py migrate
```

#### 7. Crie um superusuário
```bash
python manage.py createsuperuser
```

#### 8. Execute o servidor
```bash
python manage.py runserver
```

O backend estará disponível em: http://localhost:8000

---

### Frontend (Next.js)

#### 1. Abra um novo terminal e navegue até a pasta frontend
```bash
cd frontend
```

#### 2. Instale as dependências
```bash
npm install
# ou
pnpm install
# ou
yarn install
```

#### 3. Configure as variáveis de ambiente
```bash
# Crie o arquivo .env.local
cp .env.example .env.local

# Edite o .env.local
NEXT_PUBLIC_API_URL=http://localhost:8000/api
NEXT_PUBLIC_STRIPE_PUBLIC_KEY=pk_test_...
```

#### 4. Execute o servidor de desenvolvimento
```bash
npm run dev
# ou
pnpm dev
# ou
yarn dev
```

O frontend estará disponível em: http://localhost:3000

---

### Redis (Para tarefas assíncronas)

#### Windows
```bash
# Instale via Chocolatey
choco install redis-64

# Inicie o serviço
redis-server
```

#### Linux/Mac
```bash
# Ubuntu/Debian
sudo apt-get install redis-server
sudo systemctl start redis

# Mac
brew install redis
brew services start redis
```

#### Verifique se está funcionando
```bash
redis-cli ping
# Deve retornar: PONG
```

---

### Celery (Worker de tarefas)

Em um novo terminal, ative o ambiente virtual do backend e execute:

```bash
cd backend
celery -A config worker --loglevel=info
```

Para tarefas periódicas (Celery Beat):
```bash
celery -A config beat --loglevel=info
```

---

## 🧪 Executar Testes

### Backend
```bash
cd backend

# Todos os testes
pytest

# Com cobertura
pytest --cov=apps

# Testes específicos
pytest apps/users/tests.py

# Testes rápidos (sem slow)
pytest -m "not slow"
```

### Frontend
```bash
cd frontend

# Testes unitários
npm test

# Testes com cobertura
npm run test:coverage

# Testes E2E (Cypress)
npm run test:e2e
```

---

## 📊 Popular Banco de Dados com Dados de Teste

### Usando fixtures Django
```bash
cd backend

# Carregar dados de exemplo
python manage.py loaddata fixtures/initial_data.json

# Ou criar seus próprios dados
python manage.py shell
>>> from apps.courses.models import Course
>>> Course.objects.create(title="Python Básico", description="...")
```

### Usando script personalizado
```bash
python manage.py populate_db
```

---

## 🔧 Troubleshooting

### Erro: "Port 3000 is already in use"
```bash
# Windows
netstat -ano | findstr :3000
taskkill /PID <PID> /F

# Linux/Mac
lsof -ti:3000 | xargs kill -9
```

### Erro: "connection to server at localhost refused"
```bash
# Verifique se o PostgreSQL está rodando
# Windows
services.msc  # Procure por PostgreSQL

# Linux
sudo systemctl status postgresql

# Mac
brew services list
```

### Erro de migração Django
```bash
# Reset do banco (CUIDADO: apaga todos os dados)
python manage.py flush
python manage.py migrate

# Ou recriar migrações
find . -path "*/migrations/*.py" -not -name "__init__.py" -delete
find . -path "*/migrations/*.pyc" -delete
python manage.py makemigrations
python manage.py migrate
```

### Erro de dependências Node
```bash
# Limpe o cache e reinstale
rm -rf node_modules package-lock.json
npm cache clean --force
npm install
```

---

## 🌐 Acessar Serviços

| Serviço | URL | Credenciais |
| --- | --- | --- |
| Frontend | http://localhost:3000 | - |
| Backend API | http://localhost:8000/api | - |
| Admin Django | http://localhost:8000/admin | superuser criado |
| API Docs (Swagger) | http://localhost:8000/api/docs | - |
| Mailhog (emails dev) | http://localhost:8025 | - |

---

## 📱 Configuração de Desenvolvimento Mobile

### Acessar do celular na mesma rede

1. Descubra seu IP local:
```bash
# Windows
ipconfig

# Linux/Mac
ifconfig
```

2. Configure o frontend para aceitar conexões externas:
```bash
# frontend/next.config.js
module.exports = {
  async rewrites() {
    return [
      {
        source: '/api/:path*',
        destination: 'http://SEU_IP_LOCAL:8000/api/:path*'
      }
    ]
  }
}
```

3. Acesse via: `http://SEU_IP_LOCAL:3000`

---

## 🚀 Build de Produção

### Frontend
```bash
cd frontend
npm run build
npm start
```

### Backend
```bash
cd backend

# Coletar arquivos estáticos
python manage.py collectstatic --noinput

# Usar gunicorn
gunicorn config.wsgi:application --bind 0.0.0.0:8000
```

---

## 📚 Próximos Passos

Após configurar o ambiente:

1. ✅ Leia a [Documentação Completa](./MANUAL_USUARIO.md)
2. ✅ Veja a [Estrutura do Projeto](./ESTRUTURA_PROJETO.md)
3. ✅ Confira as [Tecnologias Utilizadas](./TECNOLOGIAS.md)
4. ✅ Explore o [Backlog do Produto](./BACKLOG.md)

---

## 💬 Precisa de Ajuda?

- Consulte a [documentação da equipe](./EQUIPE.md)
- Abra uma [issue no GitHub](https://github.com/seu-usuario/cursofy/issues)
- Entre em contato com a equipe

---

Última atualização: **27/10/2025**
