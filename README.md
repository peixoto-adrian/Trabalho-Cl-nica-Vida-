# 🏥 Sistema Clínica Vida+ — Projeto Acadêmico Integrador

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![HTML5 / JS](https://img.shields.io/badge/Web-HTML5%20%2F%20JavaScript-orange)](#)
[![Status: Concluído](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen)](#)

Aplicação web completa, moderna e responsiva para gestão da **Clínica Vida+**, integrando os cinco passos da atividade acadêmica: Gestão Ágil de Projetos (Kanban/Sprint), Módulo Interativo de Cadastro e Estatísticas, Lógica Proposicional e Tabelas-Verdade, Algoritmo de Fila FIFO e Diagrama de Casos de Uso UML.

---

## 📑 Sumário

1. [Visão Geral](#-visão-geral)
2. [Apresentação dos 5 Passos](#-apresentação-dos-5-passos)
   - [Passo 1: Quadro Kanban e Gestão Ágil](#passo-1-quadro-kanban-e-gestão-ágil)
   - [Passo 2: Módulo de Cadastro e Estatísticas](#passo-2-módulo-de-cadastro-e-estatísticas)
   - [Passo 3: Lógica Proposicional e Tabelas-Verdade](#passo-3-lógica-proposicional-e-tabelas-verdade)
   - [Passo 4: Fila FIFO (Estrutura de Dados)](#passo-4-fila-fifo-estrutura-de-dados)
   - [Passo 5: Diagrama UML de Casos de Uso](#passo-5-diagrama-uml-de-casos-de-uso)
3. [Como Executar](#-como-executar)
4. [Tecnologias Utilizadas](#-tecnologias-utilizadas)
5. [Licença](#-licença)

---

## 🚀 Visão Geral

O projeto **Clínica Vida+** resolve desafios de gestão em clínicas de saúde através de uma interface unificada contendo ferramentas de planejamento, processamento de dados e validação de regras de negócio.

---

## 📌 Apresentação dos 5 Passos

### Passo 1: Quadro Kanban e Gestão Ágil
- **Quadro Interativo:** Listas *Backlog*, *Sprint Atual*, *Em Progresso* e *Concluído*.
- **Funcionalidades:** Adicionar tarefas, mover entre listas, editar, excluir e acompanhar progresso.
- **Relatório de Sprint:** Resultados, desafios, pontos positivos e ações de melhoria.
- **Integração:** Instruções claras para replicar o quadro no Trello real.

### Passo 2: Módulo de Cadastro e Estatísticas
- **Cadastro Completo:** Nome, Idade e Telefone.
- **Validações:** Tratamento de entradas em branco, idades negativas e buscas não encontradas.
- **Estatísticas Automáticas:** Total de pacientes, idade média, paciente mais novo e paciente mais velho.
- **Busca Interativa:** Localização de pacientes por nome ou parte do nome.

### Passo 3: Lógica Proposicional e Tabelas-Verdade
Definição das variáveis proposicionais:
- **A:** Tem agendamento
- **B:** Documentos válidos
- **C:** Médico disponível
- **D:** Pagamentos em dia

#### Expressões Lógicas e Resultados:
1. **Consulta Normal:** `(A ∧ B ∧ C) ∨ (B ∧ C ∧ D)` — **3 liberações** em 16 combinações.
2. **Emergência:** `C ∧ (B ∨ D)` — **6 liberações** em 16 combinações.

#### Análise do Caso Crítico `(A=F, B=V, C=V, D=F)`:
- **Consulta Normal:** **Negada (F)**. Sem agendamento (`A=F`), exigia-se pagamento em dia (`D=V`).
- **Emergência:** **Liberada (V)**. Não exige agendamento (`A`); tendo médico (`C=V`) e documento (`B=V`), o atendimento é imediato.

### Passo 4: Fila FIFO (Estrutura de Dados)
- **Política:** *First-In, First-Out* (Primeiro a entrar, primeiro a sair).
- **Simulação:** Inserção de 3 pacientes (Nome e CPF) e remoção sequencial do primeiro da fila para atendimento, reorganizando os demais.

### Passo 5: Diagrama UML de Casos de Uso
- **Atores:** Secretária e Médico.
- **Casos de Uso:** Cadastrar Paciente, Agendar Consulta, Confirmar Consulta, Cancelar Consulta, Gerar Receita e Imprimir Receita.
- **Relacionamentos `<<include>>`:**
  - `Agendar Consulta` ➔ `Verificar Cadastro do Paciente`
  - `Confirmar Consulta` ➔ `Verificar Cadastro do Paciente`
  - `Gerar Receita` ➔ `Imprimir Receita`

---

## 💻 Como Executar

Não é necessário instalar nenhum programa ou interpretador adicional.

1. Clone este repositório:
   ```bash
   git clone [https://github.com/seu-usuario/clinica-vida-plus.git](https://github.com/seu-usuario/clinica-vida-plus.git)# Trabalho-Cl-nica-Vida-
