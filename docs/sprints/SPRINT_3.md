# Documentação - Sprint 3

**Período:** 11/11/2025 a 24/11/2025
**Meta da Sprint:** Implementar área do instrutor e sistema de avaliações.

---

## Histórias de Usuário e Tarefas Planejadas

| ID | Descrição da Tarefa | Status |
| :--- | :--- | :---: |
| **CUR-08** | Como um instrutor, eu quero ter um dashboard para visualizar estatísticas dos meus cursos... | Concluída |
| **CUR-09** | Como um instrutor, eu quero fazer upload de vídeos e materiais complementares... | Concluída |
| **CUR-10** | Como um aluno, eu quero avaliar cursos e receber certificados ao concluir... | Concluída |
| **(DOC-03)** | Criar documentação de API e guias para desenvolvedores. | Concluída |

---

## Detalhamento das Histórias

### CUR-08: Dashboard do Instrutor
**Descrição:** Painel administrativo para instrutores acompanharem métricas e performance de seus cursos.

**Critérios de Aceitação:**
- Visualizar total de alunos inscritos
- Gráficos de engajamento e conclusão
- Receita gerada por curso
- Avaliações recebidas
- Alertas e notificações importantes

### CUR-09: Sistema de Upload de Conteúdo
**Descrição:** Funcionalidade para upload de vídeos, PDFs, arquivos e outros materiais de apoio aos cursos.

**Critérios de Aceitação:**
- Upload de vídeos com progress bar
- Processamento e encoding automático
- Upload de PDFs e documentos
- Organização por aula/módulo
- Limite de tamanho e validação de formatos

### CUR-10: Sistema de Avaliações e Certificados
**Descrição:** Sistema completo de avaliação de cursos pelos alunos e emissão automática de certificados de conclusão.

**Critérios de Aceitação:**
- Avaliação por estrelas (1-5)
- Comentários escritos opcionais
- Geração automática de certificados PDF
- Certificado com QR Code de validação
- Galeria de certificados no perfil do aluno

---

## Resultado da Sprint

A meta da sprint foi atingida com sucesso. A plataforma agora possui funcionalidades completas tanto para alunos quanto para instrutores.

**Destaques:**
- Dashboard do instrutor com visualizações em tempo real
- Integração com AWS S3 para armazenamento de vídeos
- Sistema de certificados com validação única
- Performance otimizada no upload de arquivos grandes

**Métricas:**
- 4 histórias de usuário completadas
- 12 endpoints de API criados
- 91% de cobertura de testes
- Tempo médio de upload reduzido em 40%

---

## Retrospectiva

**O que funcionou bem:**
- Integração com serviços cloud bem-sucedida
- Testes E2E implementados com sucesso
- Deploy contínuo funcionando perfeitamente

**O que pode melhorar:**
- Documentação de API mais detalhada
- Performance em uploads simultâneos

**Ações para próxima sprint:**
- Implementar upload paralelo
- Expandir documentação com exemplos práticos
