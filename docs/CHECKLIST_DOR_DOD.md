# Checklist de Definições (DoR & DoD)

Este documento estabelece os critérios de qualidade e os processos que governam o ciclo de vida de uma tarefa no projeto Cursofy.

---

## Definition of Ready (DoR)
*Uma tarefa deve atender a todos os critérios abaixo para ser movida para a coluna "Em Andamento".*

- [ ] **História Clara:** A história de usuário está bem escrita, com um objetivo claro.
- [ ] **Critérios de Aceite Definidos:** Os requisitos para considerar a funcionalidade completa estão listados e são compreensíveis.
- [ ] **ID da Tarefa Criado:** A tarefa possui um identificador único no Backlog (ex: `CUR-07`).
- [ ] **Estimativa Realizada:** A equipe discutiu e estimou o esforço necessário para a tarefa.

---

## Definition of Done (DoD)
*Uma tarefa deve atender a todos os critérios abaixo para ser considerada "Concluída".*

- [ ] **Código Entregue:** O código foi comitado e enviado (`push`) para sua respectiva branch no repositório.
- [ ] [cite_start]**Padrão de Commit:** A mensagem do commit segue o padrão `tipo(ID): descrição`. [cite: 34]
- [ ] [cite_start]**Pull Request Aberto:** Um Pull Request (PR) foi criado para mesclar a branch de trabalho na branch `main`. [cite: 81]
- [ ] [cite_start]**Revisão de Código (Code Review):** Pelo menos um outro membro da equipe revisou e aprovou o PR. [cite: 83]
- [ ] **Merge Realizado:** O Pull Request foi aprovado e o código foi integrado (`merged`) à branch `main`.