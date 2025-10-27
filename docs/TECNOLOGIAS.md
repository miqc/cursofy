# Tecnologias Utilizadas - Cursofy

Este documento detalha todas as tecnologias, frameworks, bibliotecas e ferramentas utilizadas no desenvolvimento da plataforma Cursofy.

---

## 🎨 Frontend

### Framework Principal
- **Next.js 14.0** - Framework React para produção com renderização híbrida (SSR/SSG)
- **React 18.2** - Biblioteca JavaScript para construção de interfaces de usuário
- **TypeScript 5.2** - Superset JavaScript com tipagem estática

### Estilização
- **Tailwind CSS 3.3** - Framework CSS utility-first
- **Shadcn/ui** - Componentes reutilizáveis baseados em Radix UI
- **Framer Motion 10.16** - Biblioteca para animações fluidas

### Gerenciamento de Estado
- **Zustand 4.4** - Gerenciamento de estado leve e escalável
- **React Query (TanStack Query) 5.0** - Gerenciamento de estado assíncrono e cache

### Validação e Formulários
- **React Hook Form 7.48** - Gerenciamento de formulários performático
- **Zod 3.22** - Schema validation TypeScript-first

---

## ⚙️ Backend

### Framework e Linguagem
- **Python 3.11** - Linguagem de programação
- **Django 5.0** - Framework web de alto nível
- **Django REST Framework 3.14** - Toolkit para construção de APIs REST

### Autenticação e Segurança
- **Django Allauth 0.57** - Autenticação e registro de usuários
- **djangorestframework-simplejwt 5.3** - JSON Web Token para autenticação
- **django-cors-headers 4.3** - Gerenciamento de CORS
- **django-environ 0.11** - Gerenciamento de variáveis de ambiente

### APIs e Integrações
- **Celery 5.3** - Task queue para processamento assíncrono
- **Redis 5.0** - Cache e message broker
- **Stripe API** - Gateway de pagamento
- **AWS SDK (Boto3)** - Integração com serviços AWS

---

## 🗄️ Banco de Dados

### Banco Principal
- **PostgreSQL 16.0** - Banco de dados relacional
- **psycopg2 2.9** - Adaptador PostgreSQL para Python

### Ferramentas de Migração
- **Django Migrations** - Sistema de migração do Django
- **django-dbbackup 4.0** - Backup automatizado do banco de dados

---

## 📦 Armazenamento e Mídia

- **AWS S3** - Armazenamento de arquivos estáticos e mídia
- **CloudFront CDN** - Distribuição de conteúdo
- **django-storages 1.14** - Interface para backends de armazenamento

---

## 🧪 Testes

### Frontend
- **Jest 29.7** - Framework de testes JavaScript
- **React Testing Library 14.1** - Testes de componentes React
- **Cypress 13.6** - Testes end-to-end

### Backend
- **pytest 7.4** - Framework de testes Python
- **pytest-django 4.7** - Plugin pytest para Django
- **Factory Boy 3.3** - Criação de fixtures para testes
- **coverage 7.3** - Análise de cobertura de código

---

## 🚀 DevOps e Deploy

### Containerização
- **Docker 24.0** - Containerização de aplicações
- **Docker Compose 2.23** - Orquestração de containers locais

### CI/CD
- **GitHub Actions** - Automação de workflows
- **Pre-commit hooks** - Validação de código antes de commits

### Hospedagem
- **Vercel** - Deploy do frontend Next.js
- **Railway** - Deploy do backend Django
- **AWS RDS** - Banco de dados PostgreSQL gerenciado

### Monitoramento
- **Sentry** - Rastreamento de erros
- **New Relic** - Monitoramento de performance
- **Google Analytics** - Análise de uso

---

## 🛠️ Ferramentas de Desenvolvimento

### Code Quality
- **ESLint 8.54** - Linter JavaScript/TypeScript
- **Prettier 3.1** - Formatador de código
- **Black 23.12** - Formatador de código Python
- **Flake8 6.1** - Linter Python
- **isort 5.13** - Organizador de imports Python

### Documentação
- **Storybook 7.6** - Documentação de componentes UI
- **Swagger/OpenAPI** - Documentação de API
- **MkDocs** - Documentação técnica

---

## 📱 Bibliotecas Adicionais

### Frontend
- **Axios 1.6** - Cliente HTTP
- **Day.js 1.11** - Manipulação de datas
- **React Player 2.13** - Player de vídeo
- **Chart.js 4.4** - Gráficos e visualizações
- **React Icons 4.12** - Biblioteca de ícones

### Backend
- **Pillow 10.1** - Processamento de imagens
- **python-decouple 3.8** - Separação de configurações
- **gunicorn 21.2** - WSGI HTTP Server
- **whitenoise 6.6** - Servir arquivos estáticos

---

## 📊 Análise e Métricas

- **Hotjar** - Análise de comportamento do usuário
- **Mixpanel** - Analytics de produto
- **Prometheus** - Métricas de sistema

---

## 🔐 Segurança

- **OWASP ZAP** - Testes de segurança
- **Let's Encrypt** - Certificados SSL/TLS
- **django-security** - Middlewares de segurança
- **helmet.js** - Segurança de headers HTTP

---

## 📝 Controle de Versão

- **Git** - Sistema de controle de versão
- **GitHub** - Hospedagem de repositório e colaboração
- **Conventional Commits** - Padrão de mensagens de commit

---

## 🌐 APIs e Serviços Externos

- **SendGrid** - Envio de emails transacionais
- **Twilio** - Notificações SMS
- **Firebase Cloud Messaging** - Push notifications
- **Google Cloud Vision API** - Análise de imagens
- **OpenAI API** - Recursos de IA

---

## 📚 Gestão de Dependências

### Frontend
- **npm 10.2** - Gerenciador de pacotes Node.js
- **pnpm 8.10** - Gerenciador de pacotes alternativo (mais rápido)

### Backend
- **pip 23.3** - Gerenciador de pacotes Python
- **Poetry 1.7** - Gerenciamento de dependências Python
- **virtualenv** - Ambientes virtuais Python

---

## 🎯 Resumo da Stack

```
Frontend: Next.js + React + TypeScript + Tailwind CSS
Backend: Django + Django REST Framework + Python
Database: PostgreSQL
Cache: Redis
Storage: AWS S3
Deploy: Vercel (Frontend) + Railway (Backend)
CI/CD: GitHub Actions
Monitoring: Sentry + New Relic
```

---

## 📌 Versões Recomendadas

| Tecnologia | Versão Mínima | Versão Recomendada |
| :--- | :---: | :---: |
| Node.js | 18.0 | 20.x LTS |
| Python | 3.10 | 3.11 |
| PostgreSQL | 14.0 | 16.0 |
| Redis | 6.0 | 7.2 |
| Docker | 23.0 | 24.0 |

---

## 🔄 Atualizações

Este documento é atualizado conforme novas tecnologias são adicionadas ao projeto. Última atualização: **27/10/2025**
