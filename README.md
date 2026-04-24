# 🍽️ Menu API - Restaurante

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

## 🧱 Estrutura do projeto

```
src/main/java/com/example/menu
├── controller
├── model
├── repository
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

Exemplo de body:

```json
{
  "nome": "Hambúrguer",
  "preco": 25.0
}
```

---

## 🧪 Testes

Você pode testar a API usando:

* Postman
* Insomnia

---

## 💡 Melhorias futuras

* Implementar update e delete (CRUD completo)
* Validação de dados
* Tratamento de exceções
* Camada de Service
* Autenticação e autorização

---

## 👨‍💻 Autor

Vítor 🚀
