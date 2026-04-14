# 📚 Sistema de Gestão Acadêmica

Este projeto é uma aplicação full stack para gestão acadêmica simples, permitindo o cadastro de alunos, controle de notas, cálculo de médias e análise de frequência.

O sistema foi desenvolvido como parte de um desafio técnico, com foco em **boas práticas**, **organização de código**, **validações** e **experiência do usuário**.

---

## 🧱 Tecnologias Utilizadas

### Backend
- Java 21
- Spring Boot
- Spring Data JPA
- Bean Validation (Jakarta Validation)
- PostgreSQL
- Docker / Docker Compose

### Frontend
- React
- TypeScript
- CSS puro

---

## 🐳 Banco de Dados com Docker

O banco de dados PostgreSQL é executado via **Docker**, eliminando a necessidade de instalação local do PostgreSQL.

Um arquivo `docker-compose.yml` está presente no backend para facilitar a execução do projeto.

---

## ▶️ Como executar o sistema

### Pré-requisitos
- Docker e Docker Compose
- Java 21
- Node.js 18+

---

### 1️⃣ Subir o banco de dados (PostgreSQL)

Na pasta do **backend**, execute:


docker compose up -d

### 2️⃣ Executar o backend

Abra o projeto do backend no IntelliJ (ou IDE de sua preferência) e execute a aplicação Spring Boot:


./mvnw spring-boot:run

---
### 3️⃣ Executar o frontend

Na pasta do frontend, execute:


npm install
npm run dev

O frontend ficará disponível em:
http://localhost:5173


## 🧠 Decisões de Projeto

### 🔹 Uso de Docker para o banco de dados
- Facilita a execução do projeto em qualquer ambiente
- Evita dependência de instalação local do PostgreSQL
- Garante consistência do ambiente de desenvolvimento

### 🔹 Uso de DTOs com validação
- Separação clara entre camada de API e entidade JPA
- Centralização das regras de validação
- Mensagens de erro personalizadas em português

### 🔹 Validação no frontend e backend
- Frontend: melhora a experiência do usuário
- Backend: garante integridade dos dados

### 🔹 Entidade única `Aluno`
- Simplificação do modelo para o escopo do desafio
- Notas armazenadas como `@ElementCollection`
- Estrutura preparada para futura normalização (Disciplina, Nota, etc.)

## 🚀 Possíveis melhorias futuras

- Normalização do modelo (entidades Disciplina e Nota)
- Paginação na listagem de alunos
- Autenticação e autorização
- Testes automatizados
- Estilização com framework (Material UI / Tailwind)

