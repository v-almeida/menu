# 🍔 Restaurant Menu API

API REST desenvolvida com **Spring Boot** para gerenciamento de um menu de restaurante.

---

## 🚀 Tecnologias utilizadas

* Java 17+
* Spring Boot
* Spring Data JPA
* PostgreSQL
* Maven
* Lombok

---

## 📌 Funcionalidades

* Listar itens do menu
* Criar novos produtos
* Persistência de dados em banco relacional

---

## 🏗️ Arquitetura

O projeto segue uma arquitetura em camadas simples:

* **Controller** → recebe e responde requisições HTTP
* **Repository** → acesso ao banco de dados
* **DTOs** → transferência de dados (entrada/saída)
* **Entity** → representação da tabela no banco

---

## 🔄 Fluxo da aplicação

1. Cliente envia requisição HTTP
2. Controller recebe os dados
3. DTO processa entrada/saída
4. Repository persiste no banco
5. Resposta é retornada ao cliente

---

## 🧠 Decisões técnicas

* Uso de **DTOs** para evitar exposição direta da entidade
* Utilização do **PostgreSQL** como banco relacional
* Uso de **JPA/Hibernate** para abstração de persistência
* Uso de **Lombok** para reduzir código boilerplate

---

## 🗄️ Modelo de dados

Tabela: `foods`

| Campo | Tipo    |
| ----- | ------- |
| id    | Long    |
| title | String  |
| image | String  |
| price | Integer |

---

## 🧱 Estrutura do projeto

```
src/main/java/com/example/menu
├── controller
├── food
│   ├── Food.java
│   ├── FoodRepository.java
│   ├── FoodRequestDTO.java
│   ├── FoodResponseDTO.java
```

---

## ⚙️ Configuração do ambiente

### Pré-requisitos

* Java JDK 17+
* Maven
* PostgreSQL

---

### 🔧 Configuração do banco de dados

Crie um banco no PostgreSQL:

```sql
CREATE DATABASE food;
```

Configure o arquivo `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/food
spring.datasource.username=postgres
spring.datasource.password=SUA_SENHA

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

---

## ▶️ Como executar o projeto

```bash
mvn spring-boot:run
```

A aplicação estará disponível em:

```
http://localhost:8080
```

---

## 📡 Endpoints

### 🔍 Listar produtos

```
GET /food
```

### ➕ Criar produto

```
POST /food
```

### 📥 Exemplo de requisição (POST)

```json
{
  "title": "Smash Burger",
  "image": "https://cdn.abrahao.com.br/base/f42/a37/d11/smash-burger.jpg",
  "price": 25
}
```

### 📤 Exemplo de resposta (GET)

```json
[
  {
    "id": 1,
    "title": "Smash Burger",
    "image": "https://cdn.abrahao.com.br/base/f42/a37/d11/smash-burger.jpg",
    "price": 25
  }
]
```

---

## 🌐 CORS

A API está configurada para aceitar requisições externas:

```java
@CrossOrigin(origins = "*", allowedHeaders = "*")
```

---

## 🧪 Testes

Você pode testar a API usando:

* Postman
* Insomnia

---

## 🚧 Melhorias futuras

* Implementar PUT e DELETE (CRUD completo)
* Adicionar camada de Service
* Validação de dados (`@Valid`)
* Tratamento de exceções (`@ControllerAdvice`)
* Autenticação e autorização

---

## 👨‍💻 Autor

Desenvolvido por **Vítor Almeida** 🚀
