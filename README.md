# Banco de Dados - Clínica Médica

Este projeto é um banco de dados para gerenciar informações de uma clínica médica. Ele inclui as tabelas de **Pacientes**, **Médicos**, **Consultas** e **Receitas**. O objetivo é fornecer uma estrutura para o armazenamento de dados médicos e permitir consultas sobre pacientes, médicos, consultas realizadas e medicamentos prescritos.

## Estrutura do Banco de Dados

O banco de dados contém as seguintes tabelas:

1. **Paciente**
   - **id_paciente** (INT): Identificador único do paciente (chave primária)
   - **nome** (VARCHAR): Nome do paciente
   - **telefone** (VARCHAR): Telefone de contato do paciente
   - **data_nascimento** (DATE): Data de nascimento do paciente

2. **Medico**
   - **id_medico** (INT): Identificador único do médico (chave primária)
   - **nome** (VARCHAR): Nome do médico
   - **especialidade** (VARCHAR): Especialidade médica

3. **Consulta**
   - **id_consulta** (INT): Identificador único da consulta (chave primária)
   - **id_paciente** (INT): ID do paciente (chave estrangeira referenciando `Paciente`)
   - **id_medico** (INT): ID do médico (chave estrangeira referenciando `Medico`)
   - **data_consulta** (DATETIME): Data e hora da consulta
   - **valor** (DECIMAL): Valor da consulta

4. **Receita**
   - **id_receita** (INT): Identificador único da receita (chave primária)
   - **id_consulta** (INT): ID da consulta (chave estrangeira referenciando `Consulta`)
   - **descricao_medicamentos** (TEXT): Descrição dos medicamentos receitados

## Funcionalidades

### 1. Listar todas as consultas realizadas por um médico específico
Consulta as consultas realizadas por um médico, incluindo informações sobre os pacientes e o valor da consulta.

### 2. Exibir os medicamentos receitados para um paciente
Exibe a lista de medicamentos prescritos para um paciente específico, com base nas consultas realizadas.

### 3. Mostrar o total de consultas e a receita gerada por especialidade médica
Calcula o total de consultas realizadas e a receita gerada por especialidade médica, permitindo uma análise financeira por área.

## Como usar

1. **Clonando o repositório**

   Clone o repositório para o seu ambiente local:
   ```bash
   git clone https://github.com/usuario/repo-clinica-medica.git
   cd repo-clinica-medica
