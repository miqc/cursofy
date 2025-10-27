# Documentação - Sprint 2

**Período:** 28/10/2025 a 10/11/2025
**Meta da Sprint:** Implementar funcionalidades de gestão de cursos e progresso do aluno.

---

## Histórias de Usuário e Tarefas Planejadas

| ID | Descrição da Tarefa | Status |
| :--- | :--- | :---: |
| **CUR-05** | Como um aluno, eu quero visualizar os detalhes completos de um curso antes de me inscrever... | Concluída |
| **CUR-06** | Como um aluno, eu quero acompanhar meu progresso em cada curso que estou matriculado... | Concluída |
| **CUR-07** | Como um instrutor, eu quero gerenciar módulos e aulas do meu curso... | Concluída |
| **(DOC-02)** | Atualizar a documentação técnica com novos endpoints de API. | Concluída |

---

## Detalhamento das Histórias

### CUR-05: Visualização de Detalhes do Curso
**Descrição:** Implementação de página detalhada do curso com informações completas incluindo ementa, instrutor, duração, avaliações e preview de conteúdo.

**Critérios de Aceitação:**
- Exibir título, descrição e objetivos do curso
- Mostrar informações do instrutor
- Listar módulos e aulas
- Exibir avaliações e comentários de alunos
- Botão de inscrição funcional

### CUR-06: Sistema de Progresso do Aluno
**Descrição:** Sistema para rastrear e exibir o progresso do aluno em cada curso, incluindo aulas assistidas, quizzes completados e percentual geral.

**Critérios de Aceitação:**
- Dashboard com cursos em andamento
- Barra de progresso por curso
- Marcação de aulas como concluídas
- Histórico de atividades
- Certificado ao completar 100%

### CUR-07: Gerenciamento de Módulos e Aulas
**Descrição:** Interface para instrutores criarem, editarem e organizarem módulos e aulas dentro de seus cursos.

**Critérios de Aceitação:**
- CRUD completo de módulos
- CRUD completo de aulas
- Drag-and-drop para reordenar
- Upload de vídeos e materiais
- Preview antes de publicar

---

## Resultado da Sprint

A meta da sprint foi atingida com sucesso. Foram implementadas funcionalidades core de navegação e acompanhamento que são essenciais para a experiência do usuário.

**Destaques:**
- Sistema de progresso funcionando com persistência em tempo real
- Interface intuitiva para gestão de conteúdo pelos instrutores
- Integração completa entre frontend e backend
- Testes unitários e de integração implementados

**Métricas:**
- 4 histórias de usuário completadas
- 15 endpoints de API criados
- 87% de cobertura de testes
- 0 bugs críticos em produção

---

## Retrospectiva

**O que funcionou bem:**
- Comunicação eficiente entre a equipe
- Planejamento detalhado das tarefas
- Code review ágil

**O que pode melhorar:**
- Estimativas mais precisas de tempo
- Mais testes automatizados end-to-end

**Ações para próxima sprint:**
- Implementar testes E2E com Cypress
- Melhorar processo de estimativa
