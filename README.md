# Guia de Estudos

---

### 1. **Spring Boot com Banco de Dados**

   - **Desafio 1**: Crie uma API REST básica para cadastro de usuários (CRUD) com banco de dados relacional.
     - **Fácil**: Crie, leia, atualize e delete usuários usando MySQL ou PostgreSQL.
     - **Intermediário**: Adicione autenticação básica e controle de acesso com roles e JWT.

   - **Estudo**:
     - Conceitos de **Spring Boot** para API REST, JPA e Hibernate para mapeamento de dados.
     - **Spring Security** para autenticação e controle de acesso com JWT.

   - **Materiais**:
     - Documentação do [Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/html/).
---

### 2. **JUnit**

   - **Desafio 2**: Desenvolva uma suíte de testes para o CRUD da API.
     - **Fácil**: Teste cada endpoint da API garantindo funcionamento básico.
     - **Intermediário**: Implemente testes de integração para garantir o funcionamento do sistema completo.

   - **Estudo**:
     - Conceitos de **JUnit 5**: asserções, testes de unidade e de integração com Spring Boot.

   - **Materiais**:
     - Documentação do [JUnit 5](https://junit.org/junit5/docs/current/user-guide/).

---

### 3. **Mockito**

   - **Desafio 3**: Escreva testes de unidade usando Mockito na API de usuários.
     - **Fácil**: Use mocks para simular interações com o banco de dados.
     - **Intermediário**: Teste interações mais complexas, como chamadas entre serviços, com mocks para integração futura com RabbitMQ.

   - **Estudo**:
     - Conceitos de **Mockito** e configuração de testes de unidade e integração no Spring Boot.

   - **Materiais**:
     - Documentação do [Mockito](https://site.mockito.org/).

---

### 4. **RabbitMQ**

   - **Desafio 4**: Desenvolva uma fila de mensagens para notificações de cadastro.
     - **Fácil**: Configure o RabbitMQ com Spring Boot para enviar e receber mensagens simples.
     - **Intermediário**: Integre com serviços externos (email ou SMS) e crie um mecanismo de reenvio de mensagens.

   - **Estudo**:
     - Conceitos de **RabbitMQ** e integração com **Spring AMQP**.
     - Configuração de tentativas de reenvio em caso de falha de entrega.

   - **Materiais**:
     - Documentação do [RabbitMQ](https://www.rabbitmq.com/documentation.html).

---

### 5. **Microsserviços**

   - **Desafio 5**: Crie uma arquitetura de microsserviços para serviços de usuários e pedidos.
     - **Fácil**: Desenvolva dois serviços separados que se comuniquem usando REST ou RabbitMQ.
     - **Intermediário**: Implemente um gateway para comunicação centralizada e segurança com autenticação JWT.

   - **Estudo**:
     - **Spring Cloud** para configuração de microsserviços, API Gateway e segurança JWT para autenticação centralizada.
     - Comunicação via REST ou mensageria com RabbitMQ.

   - **Materiais**:
     - Documentação do [Spring Cloud](https://spring.io/projects/spring-cloud).

---

### 6. **Angular**

   - **Desafio 6**: Crie um frontend básico para consumir a API de usuários.
     - **Fácil**: Interface para cadastro e listagem de usuários.
     - **Intermediário**: Adicione autenticação com controle de sessão e feedback para erros de cadastro.

   - **Estudo**:
     - Conceitos básicos de **Angular**: componentes, módulos e rotas.
     - **HTTP Client** para comunicação com APIs REST e uso de JWT.

   - **Materiais**:
     - Documentação do [Angular](https://angular.io/docs).

---

### 7. **Aplicação Full Stack com Angular + Spring Boot**

   - **Desafio 7**: Desenvolva uma aplicação completa com Angular e Spring Boot.
     - **Fácil**: Crie uma interface de listagem e criação de tarefas, com persistência em banco de dados.
     - **Intermediário**: Adicione filtros, pesquisa e notificações em tempo real com RabbitMQ.

   - **Estudo**:
     - **Integração Angular e Spring Boot** para frontend e backend.
     - Configuração de CORS, notificações em tempo real com **RabbitMQ** ou **WebSocket**.
     - Autenticação JWT para segurança.

   - **Materiais**:
     - Guia [Angular + Spring Boot](https://www.baeldung.com/spring-boot-angular-web) da Baeldung.
