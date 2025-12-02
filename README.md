# Gerência-de-Requisitos---Engenharia-de-Requisitos

# Sistema de Gestão de Academia - Especificação de Requisitos

## Descrição Geral do Sistema
O sistema tem como objetivo gerenciar todas as operações de uma academia, incluindo:
- Cadastro e controle de alunos
- Gestão de planos e pagamentos
- Agendamento de aulas e horários
- Controle de equipamentos
- Relatórios de frequência e desempenho

**Usuários:** Administradores, Professores, Alunos, Recepcionistas

**Plataforma:** Web e Mobile

---

## Requisitos Gerais

### Requisitos Funcionais (RF)
| ID | Descrição | Prioridade |
|----|------------|-----------|
| RF01 | O sistema deve permitir cadastro de alunos com dados pessoais | Essencial |
| RF02 | O aluno deve poder visualizar seu plano atual | Essencial |
| RF03 | O sistema deve gerar mensalidades automaticamente | Essencial |
| RF04 | O professor deve poder registrar presença em aulas | Importante |
| RF05 | O administrador deve gerar relatórios financeiros | Importante |
| RF06 | O aluno deve poder agendar horário para uso de equipamentos | Desejável |

### Requisitos Não Funcionais (RNF)
| ID | Descrição | Prioridade |
|----|------------|-----------|
| RNF01 | O sistema deve responder em até 2 segundos | Essencial |
| RNF02 | Deve suportar 500 usuários simultâneos | Essencial | 
| RNF03 | Interface responsiva para mobile | Essencial |
| RNF04 | Backup automático diário dos dados | Importante |
| RNF05 | Conformidade com LGPD | Essencial |

### Regras de Negócio (RN)
| ID | Descrição | Prioridade |
|----|------------| -----------|
| RN01 | Aluno com mensalidade atrasada não pode agendar aulas | Essencial |
| RN02 | Cada aluno pode ter apenas um plano ativo por vez | Essencial |
| RN03 | Cancelamento de plano requer aviso prévio de 30 dias | Essencial |
| RN04 | Aulas em grupo limitadas a 20 alunos | Importante |

---

## Diagramas UML

### Diagrama de Casos de Uso
*(Adicione a imagem aqui depois)*
![Diagrama de Casos de Uso](docs/use-case-diagram.png)

**Principais atores:** Aluno, Professor, Administrador

### Diagrama de Sequência - Agendamento de Aula
*(Adicione a imagem aqui depois)*
![Diagrama de Sequência](docs/sequence-diagram.png)

### Diagrama de Atividades - Processo de Check-in
*(Adicione a imagem aqui depois)*
![Diagrama de Atividades](docs/activity-diagram.png)

---

## Arquitetura do Sistema

### Padrão MVC (Model-View-Controller)

**Model (Modelo):**
- Entidades: Aluno, Plano, Aula, Pagamento
- Lógica de negócio e acesso ao banco de dados

**View (Visão):**
- Interface web (React.js/Angular)
- App mobile (React Native)
- Dashboards administrativos

**Controller (Controlador):**
- Rotas e endpoints da API
- Validação de dados
- Comunicação entre Model e View

**Tecnologias sugeridas:**
- Backend: Node.js ou Spring Boot
- Banco de Dados: PostgreSQL
- Frontend: React.js
- Mobile: React Native
