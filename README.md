# Trabalho-meetologias-ageis
Link: do Trello do projeto
https://trello.com/b/GttNfQIZ/trabalho-metodologias-ageis

# 🚀 Portal de Estágios — Implementação e Gestão Kanban

> **Disciplina:** Gestão / Métodos Ágeis  
> **Trabalho:** B1-T3 — Implementação de Kanban para Time de Desenvolvimento Web  
> **Produto Observado:** Portal de Estágios  

---

## 📌 1. Visão Geral do Produto

O **Portal de Estágios** é uma plataforma web criada para conectar alunos a vagas de estágio em empresas parceiras, além de contar com um módulo administrativo de *Back-office*[cite: 1].

### 👥 Perfis de Usuário
- **Alunos:** Busca e candidatura a vagas[cite: 1].
- **Empresas:** Publicação e gestão de vagas[cite: 1].
- **Back-office (Admin):** Validação de cadastros, empresas e candidaturas[cite: 1].

---

## 📋 2. Tipos de Demandas Tratadas

No fluxo de trabalho, gerenciamos 4 categorias de demandas:
1. **✨ Novas Funcionalidades:** Recursos inéditos para a plataforma (ex.: Notificações por e-mail)[cite: 1].
2. **🐛 Defeitos (Bugs):** Correções operacionais urgentes (ex.: Falha no envio de currículos)[cite: 1].
3. **🔧 Melhorias Técnicas:** Otimização de queries, refatoração de código e padronização[cite: 1].
4. **📅 Demandas com Data Fixa:** Entregas com prazos vinculados ao calendário acadêmico/institucional[cite: 1].

---

## 📐 3. Estrutura do Quadro Kanban e Limites de WIP

O fluxo foi desenhado separando **etapas ativas** (trabalho em andamento) e **etapas de espera** (filas), permitindo identificar gargalos operacionais com precisão[cite: 1].

| Coluna | Tipo | Limite de WIP | Justificativa Técnica |
| :--- | :---: | :---: | :--- |
| **Backlog** | Espera | ∞ | Demandas registradas aguardando priorização[cite: 1]. |
| **Pronto para Desenvolver** | Espera | ∞ | **Ponto de Compromisso.** Requisitos refinados[cite: 1]. |
| **Em Desenvolvimento** | Ativo | **3** | Alinhado ao tamanho do time (3-4 devs) para evitar troca de contexto[cite: 1]. |
| **Aguardando Review** | Espera | - | Fila de espera para revisão de código[cite: 1]. |
| **Em Revisão (Code Review)** | Ativo | **2** | Capacidade limitada de devs sêniores para code review[cite: 1]. |
| **Aguardando Testes** | Espera | - | Fila de espera para validação do QA[cite: 1]. |
| **Em Testes** | Ativo | **2** | Capacidade restrita do time de QA[cite: 1]. |
| **Pronto para Entrega** | Espera | **3** | Agrupamento estratégico para deploy em lote[cite: 1]. |
| **Entregue** | Fim | - | **Ponto de Entrega.** Funcionalidade em produção[cite: 1]. |

---

## 🔒 4. Políticas Explícitas do Fluxo

1. **Critério de Entrada (Compromisso):** Para ir para *Pronto para Desenvolver*, o item precisa de critérios de aceite formalizados e aprovação do PO[cite: 1].
2. **Priorização e Puxada:** Respeita-se a ordem da fila. Demandas com **Data Fixa** possuem prioridade de puxada[cite: 1].
3. **Respeito ao WIP:** Um dev só puxa um novo item se houver saldo no WIP da coluna destino[cite: 1].
4. **Definição de "Pronto" (DoD):** Mudanças de coluna exigem o cumprimento total dos critérios da etapa atual (ex.: testes unitários validados para ir a Code Review)[cite: 1].
5. **Gestão de Bloqueios:** Cartões bloqueados recebem marcação visual evidente e o motivo é pautado na *Daily Meeting*. Não somam na capacidade produtiva ativa do dev[cite: 1].
6. **Critério de Conclusão:** O item só é considerado *Entregue* após deploy e homologação em produção sem falhas críticas[cite: 1].

---

## 🏃 5. Simulação e Diagnóstico do Fluxo

Durante as rodadas de simulação prática do fluxo de trabalho:
- **Identificação de Gargalo:** Ficou evidenciado que a etapa de **Testes (QA)** é o gargalo estrutural do processo, gerando acúmulo de cartões na fila *Aguardando Testes*[cite: 1].
- **Tratamento de Impedimentos:** A demanda `C05` (Erro 500 no envio de currículo) ficou temporariamente bloqueada aguardando definição de regra de negócio do Back-office, sendo desbloqueada após alinhamento[cite: 1].

---

## 🚀 6. Propostas de Melhoria Contínua (Kaizen)

Com base nas métricas observadas na simulação, foram propostas 3 ações de melhoria:
1. **Redimensionamento de QA:** Elevar o WIP de *Em Testes* para 3 ou alocar suporte para automação de testes[cite: 1].
2. **SLA para Bloqueios:** Estabelecer limite de 48 horas para resolução de impedimentos antes do escalonamento[cite: 1].
3. **Sinalização Externa:** Criar indicador visual para dependências de terceiros/APIs externas[cite: 1].

---

## 👥 Integrantes do Projeto e Papéis na Simulação

- **Condutor:** Guia das rodadas de simulação[cite: 1].
- **Movimentador:** Atualização física/virtual das colunas[cite: 1].
- **Registrador:** Anotação de métricas, eventos e filas[cite: 1].
- **Analisadores:** Análise contínua do fluxo e aplicação das regras do WIP[cite: 1].
