# Definition of Ready (DoR) e Definition of Done (DoD) por Sprint

Este documento detalha os critérios de DoR e DoD específicos aplicados em cada sprint do projeto Cursofy.

---

## 📋 Sprint 1 - Autenticação e Catálogo

**Período:** 13/10/2025 a 27/10/2025

### Definition of Ready (DoR)

- [x] História de usuário escrita com formato: "Como [papel], eu quero [ação] para [benefício]"
- [x] Critérios de aceitação definidos e validados com o PO
- [x] Dependências técnicas identificadas (APIs, bibliotecas)
- [x] Estimativa de esforço realizada pela equipe
- [x] Mockups/wireframes aprovados para interfaces
- [x] Endpoints de API documentados
- [x] Modelo de dados definido

### Definition of Done (DoD)

**História CUR-01 (Cadastro de usuários):**
- [x] Formulário de cadastro implementado no frontend
- [x] Validações client-side funcionando
- [x] API de registro criada e testada
- [x] Criptografia de senha implementada (bcrypt)
- [x] Email de confirmação enviado
- [x] Testes unitários escritos (cobertura > 80%)
- [x] Testes de integração passando
- [x] Code review aprovado
- [x] Documentação da API atualizada
- [x] Deploy em ambiente de staging realizado

**História CUR-02 (Login):**
- [x] Interface de login responsiva criada
- [x] Autenticação JWT implementada
- [x] Refresh token configurado
- [x] Recuperação de senha funcional
- [x] Login com Google implementado
- [x] Testes E2E do fluxo completo
- [x] Tratamento de erros implementado
- [x] Mensagens de erro amigáveis
- [x] Performance validada (< 2s)

**História CUR-04 (Catálogo):**
- [x] Grid de cursos responsivo
- [x] Filtros por categoria funcionando
- [x] Busca por texto implementada
- [x] Paginação configurada
- [x] Loading states implementados
- [x] Cache de dados configurado
- [x] SEO otimizado
- [x] Lighthouse score > 85

---

## 📋 Sprint 2 - Gestão de Cursos

**Período:** 28/10/2025 a 10/11/2025

### Definition of Ready (DoR)

- [x] Histórias priorizadas no backlog
- [x] Ambiente de desenvolvimento configurado
- [x] Banco de dados com schema atualizado
- [x] APIs da Sprint 1 em produção
- [x] Design system componentizado
- [x] Permissões de usuário definidas
- [x] Testes da sprint anterior passando

### Definition of Done (DoD)

**História CUR-05 (Detalhes do curso):**
- [x] Página de detalhes completa
- [x] Preview de vídeo funcionando
- [x] Informações do instrutor exibidas
- [x] Lista de módulos e aulas
- [x] Avaliações carregadas
- [x] Botão de inscrição funcional
- [x] Breadcrumbs implementados
- [x] Schema.org markup para SEO
- [x] Testes de acessibilidade (WCAG AA)
- [x] Performance < 1.5s

**História CUR-06 (Progresso do aluno):**
- [x] Dashboard de progresso criado
- [x] Barra de progresso por curso
- [x] Marcação de aulas concluídas
- [x] Persistência em tempo real
- [x] Sincronização multi-dispositivo
- [x] Histórico de atividades
- [x] Certificado gerado automaticamente (100%)
- [x] Notificação de conquistas
- [x] Analytics implementado
- [x] Testes de concorrência

**História CUR-07 (Gestão de módulos):**
- [x] CRUD completo de módulos
- [x] CRUD completo de aulas
- [x] Drag-and-drop para reordenar
- [x] Upload de vídeos com progresso
- [x] Validação de formatos
- [x] Preview antes de publicar
- [x] Versionamento de conteúdo
- [x] Permissões por instrutor
- [x] Testes de upload grandes (>1GB)

---

## 📋 Sprint 3 - Área do Instrutor

**Período:** 11/11/2025 a 24/11/2025

### Definition of Ready (DoR)

- [x] Métricas de analytics definidas
- [x] Integração S3 documentada
- [x] Template de certificados aprovado
- [x] Fluxo de avaliações validado
- [x] Permissões de instrutor implementadas
- [x] Storage configurado
- [x] CDN configurada

### Definition of Done (DoD)

**História CUR-08 (Dashboard instrutor):**
- [x] Métricas em tempo real
- [x] Gráficos interativos (Chart.js)
- [x] Total de alunos por curso
- [x] Taxa de conclusão exibida
- [x] Receita gerada calculada
- [x] Avaliações agregadas
- [x] Exportação de relatórios (CSV/PDF)
- [x] Filtros por período
- [x] Cache de métricas (Redis)
- [x] Testes de performance

**História CUR-09 (Upload de conteúdo):**
- [x] Upload multipart para vídeos
- [x] Progress bar em tempo real
- [x] Encoding automático (AWS MediaConvert)
- [x] Thumbnail gerado automaticamente
- [x] Suporte a PDFs e documentos
- [x] Validação de tamanho (< 5GB)
- [x] Validação de formato
- [x] Retry em caso de falha
- [x] Resumable uploads
- [x] Testes com arquivos grandes

**História CUR-10 (Avaliações e certificados):**
- [x] Sistema de 5 estrelas
- [x] Comentários com moderação
- [x] Geração de PDF de certificado
- [x] QR Code único por certificado
- [x] API de validação de certificados
- [x] Template responsivo
- [x] Envio por email automatizado
- [x] Galeria de certificados
- [x] Compartilhamento social
- [x] Testes de geração em massa

---

## 📋 Sprint 4 - Pagamentos

**Período:** 25/11/2025 a 08/12/2025

### Definition of Ready (DoR)

- [x] Conta Stripe configurada (test mode)
- [x] Fluxos de pagamento mapeados
- [x] Políticas de reembolso definidas
- [x] Compliance PCI validado
- [x] Sistema de NF-e integrado
- [x] Webhooks documentados
- [x] Testes de pagamento planejados

### Definition of Done (DoD)

**História CUR-11 (Gateway de pagamento):**
- [x] Stripe Payment Intent API integrada
- [x] Suporte a cartões crédito/débito
- [x] 3D Secure implementado
- [x] Webhooks de confirmação
- [x] Retry automático de falhas
- [x] Logs de transações
- [x] Reembolsos funcionais
- [x] Testes com cartões de teste
- [x] Compliance PCI DSS Level 1
- [x] Auditoria de segurança

**História CUR-12 (Assinaturas):**
- [x] Plano mensal criado (R$ 49,90)
- [x] Plano anual criado (R$ 499,90)
- [x] Renovação automática
- [x] Cancelamento a qualquer momento
- [x] Prorata em upgrades
- [x] Trial gratuito de 7 dias
- [x] Emails de renovação
- [x] Dunning management
- [x] Testes de ciclo completo
- [x] Analytics de churn

**História CUR-13 (Histórico de transações):**
- [x] Lista completa de transações
- [x] Filtros por data e status
- [x] Download de comprovantes
- [x] Detalhes de cada transação
- [x] Status em tempo real
- [x] Paginação eficiente
- [x] Busca por ID/valor
- [x] Exportação em CSV
- [x] Testes de performance (>10k transações)

**História CUR-14 (Notas fiscais):**
- [x] Emissão automática de NF-e
- [x] Envio por email
- [x] Download de XML e PDF
- [x] Integração contábil
- [x] Armazenamento seguro (S3)
- [x] Numeração sequencial
- [x] Cancelamento de NF
- [x] Compliance fiscal validado
- [x] Testes com SEFAZ homologação

---

## 📋 Sprint 5 - Comunicação

**Período:** 09/12/2025 a 22/12/2025

### Definition of Ready (DoR)

- [x] WebSockets configurados
- [x] SendGrid API configurada
- [x] Firebase FCM configurado
- [x] Templates de email aprovados
- [x] Estrutura de fórum definida
- [x] Moderação planejada
- [x] Notificações priorizadas

### Definition of Done (DoD)

**História CUR-15 (Chat em tempo real):**
- [x] WebSocket server implementado
- [x] Chat UI responsivo
- [x] Histórico de mensagens persistido
- [x] Indicador "digitando..."
- [x] Status online/offline
- [x] Notificação de novas mensagens
- [x] Suporte a emojis
- [x] Timestamp em cada mensagem
- [x] Testes de concorrência (>1000 usuários)
- [x] Fallback para long-polling

**História CUR-16 (Notificações email):**
- [x] Template de boas-vindas
- [x] Confirmação de compra
- [x] Novos cursos
- [x] Lembretes de cursos
- [x] Newsletter semanal
- [x] Preferências de email
- [x] Unsubscribe funcionando
- [x] Tracking de abertura
- [x] A/B testing configurado
- [x] Testes de deliverability

**História CUR-17 (Push notifications):**
- [x] Service Worker instalado
- [x] Solicitação de permissão
- [x] Notificações de mensagens
- [x] Alertas de novos conteúdos
- [x] Lembretes de aulas
- [x] Configurações personalizáveis
- [x] Suporte multi-browser
- [x] Fallback gracioso
- [x] Testes em diferentes dispositivos

**História CUR-18 (Fórum de discussão):**
- [x] Criação de tópicos
- [x] Sistema de respostas aninhadas
- [x] Curtidas e reações
- [x] Marcar como solução
- [x] Moderação por instrutores
- [x] Sistema de denúncias
- [x] Busca full-text
- [x] Filtros e ordenação
- [x] Gamificação (pontos)
- [x] Testes de spam prevention

---

## 📋 Sprint 6 - Otimização e Lançamento

**Período:** 06/01/2026 a 19/01/2026

### Definition of Ready (DoR)

- [x] Todas as features anteriores em produção
- [x] Ferramentas de teste configuradas
- [x] Ambiente de staging estável
- [x] Checklist de segurança preparado
- [x] Plano de monitoramento definido
- [x] Documentação pronta
- [x] Runbook de deploy criado

### Definition of Done (DoD)

**História CUR-19 (Performance):**
- [x] Load testing executado (10k usuários)
- [x] Tempo de carregamento < 2s
- [x] Lighthouse score > 90
- [x] Queries otimizadas (< 100ms)
- [x] Cache implementado (Redis)
- [x] CDN configurado
- [x] Lazy loading em imagens
- [x] Code splitting implementado
- [x] Bundle size otimizado (< 500KB)
- [x] Relatório de performance documentado

**História CUR-20 (Segurança):**
- [x] Pentest executado
- [x] OWASP Top 10 verificado
- [x] Vulnerabilidades corrigidas
- [x] Rate limiting implementado
- [x] Headers de segurança configurados
- [x] SSL A+ rating
- [x] Secrets em vault
- [x] Auditoria de dependências
- [x] GDPR compliance
- [x] Relatório de segurança aprovado

**História CUR-21 (Documentação):**
- [x] Manual do usuário completo
- [x] API docs (Swagger)
- [x] Contributing guidelines
- [x] Architecture Decision Records
- [x] README atualizado
- [x] Changelog mantido
- [x] Vídeos tutoriais gravados
- [x] FAQ criado
- [x] Troubleshooting guide
- [x] Review pela equipe

**História CUR-22 (Deploy):**
- [x] Pipeline CI/CD funcional
- [x] Deploy automatizado
- [x] Rollback configurado
- [x] Blue-green deployment
- [x] Health checks implementados
- [x] Monitoramento ativo (New Relic)
- [x] Alertas configurados (Slack)
- [x] Logs centralizados
- [x] Backup automático (diário)
- [x] Disaster recovery testado
- [x] Runbook de produção validado

---

## 📊 Métricas Gerais de Qualidade

### Todos os Sprints

**Código:**
- Cobertura de testes: > 85%
- Complexidade ciclomática: < 10
- Duplicação de código: < 3%
- Dívida técnica: < 5%

**Performance:**
- Tempo de resposta API: < 200ms
- Tempo de carregamento página: < 2s
- First Contentful Paint: < 1.5s
- Time to Interactive: < 3s

**Acessibilidade:**
- WCAG 2.1 Level AA
- Lighthouse Accessibility: > 95
- Keyboard navigation: 100%
- Screen reader compatible

**Segurança:**
- Nenhuma vulnerabilidade crítica
- Máximo 2 vulnerabilidades médias
- Headers de segurança: A+
- Autenticação segura (JWT)

---

Última atualização: **27/10/2025**
