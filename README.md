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


### Backlog de cada aplicação:

### **Desafio 1: Spring Boot com Banco de Dados (CRUD com Autenticação)**

#### 📌 Descrição
Criação de uma API REST para um sistema de cadastro de usuários, com operações CRUD, autenticação básica e controle de acesso.

#### 📋 Backlog de Funcionalidades

1. **Configuração do Projeto**
   - [ ] Criar um projeto Spring Boot.
   - [ ] Configurar dependências: Spring Web, Spring Data JPA, MySQL/PostgreSQL Driver, Spring Security, JWT.

2. **Modelo e Banco de Dados**
   - [ ] Definir a entidade `User` com os campos: `id`, `username`, `password`, `email`, `role`.
   - [ ] Configurar conexão com o banco de dados (MySQL ou PostgreSQL).
   - [ ] Criar repositório JPA para a entidade `User`.

3. **Endpoints CRUD**
   - [ ] Implementar endpoints para `create`, `read`, `update`, e `delete` usuários.
   - [ ] Adicionar validações nos endpoints.

4. **Autenticação e Controle de Acesso**
   - [ ] Configurar autenticação básica com Spring Security.
   - [ ] Adicionar controle de acesso por roles (`USER`, `ADMIN`).
   - [ ] Implementar JWT para proteger os endpoints.
   - [ ] Testar autenticação e autorização dos endpoints.

---

### **Desafio 2: RabbitMQ - Sistema de Notificações**

#### 📌 Descrição
Desenvolvimento de um sistema de notificações assíncronas utilizando RabbitMQ para enviar mensagens ao realizar o cadastro de um usuário.

#### 📋 Backlog de Funcionalidades

1. **Configuração do RabbitMQ**
   - [ ] Instalar e configurar o RabbitMQ localmente ou via Docker.
   - [ ] Adicionar dependências de Spring AMQP ao projeto.

2. **Produtor de Mensagens**
   - [ ] Criar um serviço de envio de mensagens que envia notificações de cadastro de usuário.
   - [ ] Definir a fila de mensagens para notificações de novos cadastros.

3. **Consumidor de Mensagens**
   - [ ] Criar um consumidor que recebe mensagens da fila e as processa.
   - [ ] Configurar logging para mensagens recebidas.

4. **Integração com Serviço Externo**
   - [ ] Conectar o consumidor a um serviço externo (ex: serviço de email ou SMS).
   - [ ] Implementar reenvio de mensagens em caso de falha.

---

### **Desafio 3: Arquitetura de Microsserviços**

#### 📌 Descrição
Implementação de uma arquitetura de microsserviços com comunicação entre serviços via RabbitMQ e segurança centralizada.

#### 📋 Backlog de Funcionalidades

1. **Estrutura de Microsserviços**
   - [ ] Criar o serviço `User Service` para gerenciar dados dos usuários.
   - [ ] Criar o serviço `Order Service` para gerenciar dados de pedidos.

2. **Comunicação entre Serviços**
   - [ ] Implementar comunicação via RabbitMQ ou REST entre `User Service` e `Order Service`.
   - [ ] Definir contratos de comunicação para garantir consistência.

3. **API Gateway**
   - [ ] Configurar um API Gateway para gerenciar as chamadas de cada serviço.
   - [ ] Adicionar balanceamento de carga e roteamento no Gateway.

4. **Autenticação Centralizada**
   - [ ] Configurar autenticação JWT para todos os serviços.
   - [ ] Implementar autenticação centralizada no API Gateway.

---

### **Desafio 4: Testes de Unidade com Mockito**

#### 📌 Descrição
Desenvolvimento de uma suíte de testes unitários usando Mockito para validar o comportamento dos serviços e interações com o banco de dados.

#### 📋 Backlog de Funcionalidades

1. **Configuração do Mockito**
   - [ ] Configurar dependências do Mockito no projeto.

2. **Testes de Unidade**
   - [ ] Criar mocks para repositórios e serviços de banco de dados.
   - [ ] Testar métodos de serviço para criação, atualização e remoção de usuários.

3. **Testes de Interação**
   - [ ] Simular interações entre o serviço de usuários e outros componentes.
   - [ ] Criar mocks para integração com RabbitMQ e testar envio de mensagens.

---

### **Desafio 5: Suite de Testes com JUnit**

#### 📌 Descrição
Criação de uma suíte de testes com JUnit para verificar o comportamento dos endpoints da API e a integração entre serviços.

#### 📋 Backlog de Funcionalidades

1. **Configuração de JUnit**
   - [ ] Adicionar dependências do JUnit 5.

2. **Testes para Endpoints**
   - [ ] Testar o comportamento dos endpoints CRUD do `User Service`.
   - [ ] Validar respostas HTTP e retornos esperados para cada endpoint.

3. **Testes de Integração**
   - [ ] Implementar testes de integração para garantir que todos os serviços estão funcionando em conjunto.
   - [ ] Simular falhas de comunicação e validar respostas de erro.

---

### **Desafio 6: Frontend com Angular - Consumo da API de Usuários**

#### 📌 Descrição
Criação de uma aplicação frontend em Angular para interagir com a API de usuários.

#### 📋 Backlog de Funcionalidades

1. **Configuração do Projeto Angular**
   - [ ] Criar um projeto Angular com módulos e rotas.
   - [ ] Configurar o HTTP Client para comunicação com a API.

2. **Interfaces de Cadastro e Listagem de Usuários**
   - [ ] Criar formulário para cadastro de usuários.
   - [ ] Implementar listagem de usuários cadastrados.

3. **Autenticação e Controle de Sessão**
   - [ ] Implementar interface de login.
   - [ ] Configurar guarda de rota para controle de acesso e autenticação JWT.

4. **Feedback Visual e Tratamento de Erros**
   - [ ] Exibir mensagens de erro e sucesso para o usuário.
   - [ ] Implementar tratamento de erros no frontend.

---

### **Desafio 7: Aplicação Full Stack com Angular + Spring Boot**

#### 📌 Descrição
Desenvolvimento de uma aplicação completa de gerenciamento de tarefas com Angular no frontend e Spring Boot no backend.

#### 📋 Backlog de Funcionalidades

1. **API de Tarefas com Spring Boot**
   - [ ] Criar entidade `Task` com os campos `id`, `title`, `description`, `status`.
   - [ ] Implementar CRUD para `Task`.

2. **Frontend Angular - Tarefas**
   - [ ] Criar interface para listagem e criação de tarefas.
   - [ ] Exibir detalhes da tarefa e atualizar status.

3. **Filtros e Pesquisa de Tarefas**
   - [ ] Adicionar filtros e pesquisa no frontend.
   - [ ] Implementar paginador para listas extensas de tarefas.

4. **Notificações em Tempo Real**
   - [ ] Configurar RabbitMQ para envio de notificações em tempo real.
   - [ ] Integrar WebSocket no frontend para notificações de tarefas em tempo real.

5. **Autenticação e Controle de Acesso**
   - [ ] Implementar autenticação JWT no backend.
   - [ ] Configurar o frontend para controle de acesso baseado em sessão.

