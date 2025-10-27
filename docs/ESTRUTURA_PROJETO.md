# Estrutura do Projeto Cursofy

Este documento descreve a estrutura de pastas e arquivos do projeto Cursofy, facilitando a navegação e compreensão da organização do código.

---

## 📁 Estrutura de Diretórios

```
cursofy/
├── frontend/                    # Aplicação Next.js (Frontend)
│   ├── src/
│   │   ├── app/                # App Router do Next.js 14
│   │   │   ├── (auth)/        # Grupo de rotas de autenticação
│   │   │   │   ├── login/
│   │   │   │   └── register/
│   │   │   ├── (dashboard)/   # Grupo de rotas do dashboard
│   │   │   │   ├── courses/
│   │   │   │   ├── profile/
│   │   │   │   └── settings/
│   │   │   ├── (instructor)/  # Área do instrutor
│   │   │   │   ├── dashboard/
│   │   │   │   ├── courses/
│   │   │   │   └── analytics/
│   │   │   ├── api/           # API Routes
│   │   │   ├── layout.tsx
│   │   │   └── page.tsx
│   │   ├── components/        # Componentes React
│   │   │   ├── ui/           # Componentes de UI (shadcn/ui)
│   │   │   ├── course/       # Componentes de curso
│   │   │   ├── layout/       # Layout components
│   │   │   └── shared/       # Componentes compartilhados
│   │   ├── lib/              # Utilitários e helpers
│   │   │   ├── api.ts        # Cliente API
│   │   │   ├── utils.ts      # Funções utilitárias
│   │   │   └── validations.ts # Schemas Zod
│   │   ├── hooks/            # Custom React Hooks
│   │   ├── stores/           # Zustand stores
│   │   ├── types/            # TypeScript types
│   │   └── styles/           # Estilos globais
│   ├── public/               # Arquivos estáticos
│   │   ├── images/
│   │   ├── icons/
│   │   └── fonts/
│   ├── tests/                # Testes
│   │   ├── unit/
│   │   ├── integration/
│   │   └── e2e/
│   ├── .env.local            # Variáveis de ambiente
│   ├── next.config.js        # Configuração Next.js
│   ├── tailwind.config.ts    # Configuração Tailwind
│   ├── tsconfig.json         # Configuração TypeScript
│   └── package.json
│
├── backend/                     # Aplicação Django (Backend)
│   ├── apps/                   # Apps Django
│   │   ├── users/             # App de usuários
│   │   │   ├── migrations/
│   │   │   ├── models.py
│   │   │   ├── serializers.py
│   │   │   ├── views.py
│   │   │   ├── urls.py
│   │   │   └── tests.py
│   │   ├── courses/           # App de cursos
│   │   │   ├── migrations/
│   │   │   ├── models.py
│   │   │   ├── serializers.py
│   │   │   ├── views.py
│   │   │   ├── urls.py
│   │   │   └── tests.py
│   │   ├── payments/          # App de pagamentos
│   │   └── notifications/     # App de notificações
│   ├── config/                # Configurações Django
│   │   ├── settings/
│   │   │   ├── base.py
│   │   │   ├── development.py
│   │   │   ├── production.py
│   │   │   └── test.py
│   │   ├── urls.py
│   │   ├── wsgi.py
│   │   └── asgi.py
│   ├── core/                  # Funcionalidades core
│   │   ├── middleware/
│   │   ├── utils/
│   │   └── exceptions/
│   ├── tests/                 # Testes
│   │   ├── unit/
│   │   ├── integration/
│   │   └── fixtures/
│   ├── static/                # Arquivos estáticos
│   ├── media/                 # Upload de arquivos
│   ├── .env                   # Variáveis de ambiente
│   ├── manage.py
│   ├── requirements.txt       # Dependências Python
│   └── pytest.ini
│
├── docs/                       # Documentação
│   ├── sprints/               # Documentação das sprints
│   │   ├── SPRINT_1.md
│   │   ├── SPRINT_2.md
│   │   ├── SPRINT_3.md
│   │   ├── SPRINT_4.md
│   │   ├── SPRINT_5.md
│   │   ├── SPRINT_6.md
│   │   └── SPRINTS.md
│   ├── diagrams/              # Diagramas UML
│   │   ├── casos-de-uso/
│   │   ├── atividades/
│   │   └── classe/
│   ├── BACKLOG.md
│   ├── CRONOGRAMA.md
│   ├── TECNOLOGIAS.md
│   ├── EQUIPE.md
│   ├── CHECKLIST_DOR_DOD.md
│   ├── MANUAL_USUARIO.md
│   ├── ESTRUTURA_PROJETO.md
│   └── COMO_EXECUTAR.md
│
├── .github/                    # GitHub Actions
│   └── workflows/
│       ├── frontend-ci.yml
│       └── backend-ci.yml
│
├── docker/                     # Docker configs
│   ├── frontend/
│   │   └── Dockerfile
│   └── backend/
│       └── Dockerfile
│
├── docker-compose.yml          # Docker Compose
├── .gitignore
└── README.md
```

---

## 🎯 Convenções de Código

### Frontend (TypeScript/React)

**Nomenclatura de Arquivos:**
- Componentes: `PascalCase.tsx` (ex: `CourseCard.tsx`)
- Hooks: `camelCase.ts` com prefixo `use` (ex: `useCourses.ts`)
- Utilitários: `camelCase.ts` (ex: `formatDate.ts`)
- Tipos: `PascalCase.ts` (ex: `Course.ts`)

**Estrutura de Componentes:**
```typescript
// CourseCard.tsx
import { FC } from 'react'

interface CourseCardProps {
  title: string
  description: string
}

export const CourseCard: FC<CourseCardProps> = ({ title, description }) => {
  return (
    <div>
      <h3>{title}</h3>
      <p>{description}</p>
    </div>
  )
}
```

### Backend (Python/Django)

**Nomenclatura:**
- Modelos: `PascalCase` (ex: `Course`, `UserProfile`)
- Views: `snake_case` (ex: `course_list`, `user_detail`)
- Arquivos: `snake_case.py` (ex: `models.py`, `serializers.py`)

**Estrutura de App:**
```python
# courses/models.py
from django.db import models

class Course(models.Model):
    title = models.CharField(max_length=200)
    description = models.TextField()
    created_at = models.DateTimeField(auto_now_add=True)
    
    class Meta:
        ordering = ['-created_at']
```

---

## 📦 Principais Dependências

### Frontend
- **next**: ^14.0.0
- **react**: ^18.2.0
- **typescript**: ^5.2.0
- **tailwindcss**: ^3.3.0
- **zustand**: ^4.4.0
- **@tanstack/react-query**: ^5.0.0

### Backend
- **Django**: ^5.0
- **djangorestframework**: ^3.14
- **psycopg2**: ^2.9
- **celery**: ^5.3
- **redis**: ^5.0

---

## 🔐 Variáveis de Ambiente

### Frontend (.env.local)
```bash
NEXT_PUBLIC_API_URL=http://localhost:8000/api
NEXT_PUBLIC_STRIPE_PUBLIC_KEY=pk_test_...
```

### Backend (.env)
```bash
SECRET_KEY=your-secret-key
DEBUG=True
DATABASE_URL=postgresql://user:pass@localhost:5432/cursofy
REDIS_URL=redis://localhost:6379
STRIPE_SECRET_KEY=sk_test_...
AWS_ACCESS_KEY_ID=your-key
AWS_SECRET_ACCESS_KEY=your-secret
```

---

## 🧪 Estrutura de Testes

### Frontend
```
tests/
├── unit/              # Testes de componentes isolados
├── integration/       # Testes de fluxos
└── e2e/              # Testes Cypress end-to-end
```

### Backend
```
tests/
├── unit/              # Testes unitários
├── integration/       # Testes de integração
└── fixtures/          # Dados de teste
```

---

## 📝 Padrões de Commit

Seguimos o padrão **Conventional Commits**:

```
feat: adiciona nova funcionalidade
fix: corrige bug
docs: atualiza documentação
style: formatação de código
refactor: refatoração de código
test: adiciona ou atualiza testes
chore: tarefas de manutenção
```

**Exemplos:**
```
feat(courses): adiciona filtro por categoria
fix(auth): corrige erro no login com Google
docs(readme): atualiza instruções de instalação
```

---

## 🔄 Fluxo de Trabalho Git

1. Criar branch a partir de `develop`: `git checkout -b feature/nome-da-feature`
2. Fazer commits seguindo conventional commits
3. Abrir Pull Request para `develop`
4. Code review obrigatório
5. Merge após aprovação

**Branches principais:**
- `main`: código em produção
- `develop`: desenvolvimento ativo
- `feature/*`: novas funcionalidades
- `fix/*`: correções de bugs
- `hotfix/*`: correções urgentes em produção

---

## 📊 Arquitetura

### Frontend
- **Padrão**: JAMstack com SSR/SSG
- **State Management**: Zustand para estado global
- **API Client**: Axios com React Query para cache

### Backend
- **Padrão**: REST API
- **Arquitetura**: Monolítica modular
- **Cache**: Redis para sessões e cache
- **Queue**: Celery para tarefas assíncronas

---

## 🚀 Deploy

### Frontend
- **Plataforma**: Vercel
- **Build**: Automático via Git push
- **CDN**: Global Edge Network

### Backend
- **Plataforma**: Railway
- **Database**: AWS RDS PostgreSQL
- **Storage**: AWS S3 + CloudFront

---

Última atualização: **27/10/2025**
