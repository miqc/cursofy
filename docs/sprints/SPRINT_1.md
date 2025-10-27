# Documentação - Sprint 1

**Período:** 13/10/2025 a 27/10/2025
**Meta da Sprint:** Estabelecer o sistema de autenticação e a estrutura inicial para a exibição de cursos.

---

## Histórias de Usuário e Tarefas Planejadas

| ID | Descrição da Tarefa | Status |
| :--- | :--- | :---: |
| **CUR-01** | Como um novo usuário, eu quero me cadastrar na plataforma... | Concluída |
| **CUR-02** | Como um usuário cadastrado, eu quero fazer login com meu e-mail e senha... | Concluída |
| **CUR-04** | Como visitante, eu quero ver uma página com o catálogo de todos os cursos... | Concluída |
| **(DOC-01)** | Criar a modelagem UML inicial (Casos de Uso, Atividade, Classe). | Concluída |

---

## Detalhamento das Histórias

### CUR-01: Cadastro de Novos Usuários
**Descrição:** Permitir que novos usuários se cadastrem na plataforma fornecendo informações básicas como nome, email e senha.

**Critérios de Aceitação:**
- Formulário de cadastro responsivo
- Validação de email único
- Senha com requisitos mínimos de segurança
- Confirmação de email enviada
- Mensagens de erro claras e amigáveis

### CUR-02: Login de Usuários
**Descrição:** Sistema de autenticação seguro para usuários já cadastrados acessarem a plataforma.

**Critérios de Aceitação:**
- Autenticação com email e senha
- Geração de token JWT
- Refresh token implementado
- Opção "Lembrar-me"
- Recuperação de senha funcional
- Login com Google OAuth

### CUR-04: Catálogo de Cursos
**Descrição:** Página inicial exibindo todos os cursos disponíveis na plataforma com informações básicas.

**Critérios de Aceitação:**
- Grid responsivo de cursos
- Imagem, título e descrição curta
- Filtros por categoria
- Busca por texto
- Ordenação (mais recentes, populares)
- Paginação implementada

---

## Resultado da Sprint

A meta da sprint foi atingida com sucesso. O trabalho foi dividido em duas frentes principais:

- **Desenvolvimento:** Foram criadas as estruturas de backend (API de autenticação) e frontend (UI do catálogo), com os respectivos Pull Requests (#1 e #2) abertos para revisão.
- **Arquitetura e Documentação:** Paralelamente, foi realizada a modelagem inicial do sistema para guiar o desenvolvimento futuro. Foram criados os **Diagramas de Casos de Uso, de Atividade (Login) e de Classe**, estabelecendo a base para a arquitetura do software.

A sprint estabeleceu uma base sólida tanto em código quanto em documentação para as próximas fases do projeto.

**Destaques:**
- Sistema de autenticação JWT seguro implementado
- Integração com OAuth do Google funcionando
- Catálogo de cursos com performance otimizada
- Diagramas UML completos e validados

**Métricas:**
- 4 histórias de usuário completadas
- 10 endpoints de API criados
- 85% de cobertura de testes
- 0 bugs críticos em produção

---

## Retrospectiva

**O que funcionou bem:**
- Planejamento inicial bem estruturado
- Divisão clara de responsabilidades
- Documentação desde o início

**O que pode melhorar:**
- Estimativas de tempo para tarefas novas
- Mais pair programming
- Testes automatizados desde o início

**Ações para próxima sprint:**
- Reservar tempo para pair programming
- Implementar TDD (Test-Driven Development)
- Melhorar processo de code review
