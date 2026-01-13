# Cash Card Service API

Uma API RESTful segura e robusta desenvolvida para o gerenciamento de cartões de débito digitais e controle de mesadas familiares.

Este projeto foi desenvolvido como parte do meu portfólio de especialização em **Spring Boot**, focando em boas práticas de design de API, segurança e testes automatizados.

## Tecnologias Utilizadas

* **Java 21** (Linguagem base)
* **Spring Boot 3.5** (Framework principal)
* **Spring Data JDBC/JPA** (Persistência de dados)
* **Spring Security** (Autenticação e Autorização)
* **H2 Database** (Banco de dados em memória para dev)
* **JUnit 5** (Testes Unitários e de Integração)
* **Gradle (Groovy)** (Gerenciamento de dependências)
* **Docker** (Containerização)

## Principais Funcionalidades

* **CRUD Completo:** Criação, leitura, atualização e exclusão de cartões (Cash Cards).
* **Segurança (AuthN/AuthZ):**
    * Autenticação via Basic Auth.
    * Autorização baseada em "Ownership" (Usuários só veem/editam seus próprios cartões).
    * Proteção de rotas sensíveis.
* **Paginação e Ordenação:** Endpoints otimizados para listar grandes volumes de dados.
* **Tratamento de Erros:** Respostas HTTP adequadas e amigáveis (404, 403, 401).

## Metodologia: TDD (Test-Driven Development)

Este projeto foi construído seguindo rigorosamente o ciclo **Red-Green-Refactor**.
* **Testes Primeiro:** Cada funcionalidade começou com um teste de falha (Red).
* **Implementação:** O código foi escrito para passar no teste (Green).
* **Refatoração:** O código foi limpo e otimizado mantendo os testes passando (Refactor).
* **Cobertura:** Testes abrangentes para Controllers (Integração) e Camada de Domínio (Unitários).

## Como rodar o projeto

```markdown
1. Clone o repositório:

bash git clone https://github.com/cgmarquess/cash-card-service.git

2. Entre na pasta

bash cd cash-card-service

3. Execute com Gradle

-Para rodar os testes (TDD):
bash ./gradlew test

-Para subir a aplicação (API):
bash ./gradlew bootRun
```

## Como rodar com Docker

```markdown
1. Gere a imagem Docker:

bash docker build -t cash-card-api . 

2. Execute o container:

bash docker run -p 8080:8080 cash-card-api
```
Desenvolvido por [Gabriel Marques] - [[LinkedIn](https://www.linkedin.com/in/cgmarquess/)]
