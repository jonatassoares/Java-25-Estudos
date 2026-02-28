# Referências Técnicas — Java & Spring Boot

> Este arquivo concentra **fontes oficiais, materiais de alto nível e referências de engenharia**.
> Ele não é para estudo sequencial, mas para **consulta, aprofundamento e evolução contínua**.

📌 **Regra de uso** 

Sempre que aprender algo novo relevante, pergunte:
> “Isso merece entrar nas referências?”

  

---

## ☕ Java — Documentação Oficial

  

### 📘 Java SE

- https://docs.oracle.com/javase/specs/
- https://docs.oracle.com/en/java/javase/

  

Conteúdo:
- Especificação da linguagem
- JVM
- Tipos
- Collections
- Streams
- Records
- Optional
  

📌 **Fonte primária da verdade** sobre Java.

  

---

### 📘 Java Tutorials (Oracle)

- https://docs.oracle.com/javase/tutorial/

  

Excelente para:
- Revisões conceituais
- Exemplos claros
- Confirmação de comportamento esperado

---

## 🧠 Java Moderno (8+)

### 🔹 Streams & Lambdas

- https://docs.oracle.com/javase/8/docs/api/java/util/stream/package-summary.html
- https://docs.oracle.com/javase/tutorial/java/javaOO/lambdaexpressions.html


Use quando:
- Pipeline ficar confuso
- Precisar validar operação intermediária vs terminal

---
### 🔹 Records

- https://docs.oracle.com/en/java/javase/17/language/records.html

  

Importante para:
- DTOs
- Objetos imutáveis
- APIs REST modernas

---

### 🔹 Optional

- https://docs.oracle.com/javase/8/docs/api/java/util/Optional.html

  

📌 Referência essencial para evitar uso incorreto de `Optional`.

  

---

## 🧱 Programação Orientada a Objetos (POO)

  
### 📘 Princípios Fundamentais

- Encapsulamento
- Herança
- Polimorfismo
- Interfaces
- Composição
  

📌 Sempre preferir **composição** a herança quando possível.

  

---


### 📗 SOLID (Referência conceitual)

- https://martinfowler.com/articles/dipInTheWild.html

  

Use como:
- Guia mental
- Critério de decisão
- Referência arquitetural
  

---

## 🌱 Spring Framework


### 📘 Documentação Oficial Spring

- https://docs.spring.io/spring-framework/docs/current/reference/html/

  

Conteúdo:
- IoC
- DI
- Context
- Beans
- Ciclo de vida
  

📌 Base conceitual do Spring Boot.

  

---

## 🚀 Spring Boot


### 📘 Spring Boot Reference

- https://docs.spring.io/spring-boot/docs/current/reference/html/


Leitura obrigatória para:
- Configurações
- Profiles
- Auto-configuration
- Properties
- Actuator
  

---

### 🌐 Spring Web (REST)

- https://docs.spring.io/spring-framework/reference/web/webmvc.html

  

Referência para:
- Controllers
- RequestMapping
- REST APIs
- Serialização JSON
  

---

## 🗄️ Persistência e Banco de Dados

### 📘 Spring Data JPA

- https://docs.spring.io/spring-data/jpa/docs/current/reference/html/

Conteúdo essencial:
- Repositories
- Derived Queries
- Paginação
- Transações

---


### 📘 Hibernate ORM

- https://hibernate.org/orm/documentation/

Use para:
- Entender comportamento do JPA
- Performance
- Cache
- Lazy vs Eager

---  

## 🧪 Testes

### 📘 JUnit 5

- https://docs.junit.org/5.14.3/overview.html


Base para:
- Testes unitários
- Testes de comportamento
- Regressão
  

---

### 📘 Spring Boot Test

- https://docs.spring.io/spring-boot/docs/current/reference/html/features.html#features.testing


Conteúdo:
- @SpringBootTest
- MockMvc
- Testes de Controller
- Testes de integração
  

---

## 🧹 Clean Code & Engenharia de Software

  

### 📗 Clean Code — Robert C. Martin

📌 Livro **obrigatório** para qualquer engenheiro de software.
  

Tópicos:
- Nomes
- Métodos pequenos
- Classes coesas
- Código legível
  

---


### 📗 Refactoring — Martin Fowler

- https://martinfowler.com/refactoring/

Referência para:
- Evoluir código existente
- Refatorar com segurança
- Identificar code smells

---

  
## 🌐 REST & Arquitetura

  

### 📘 REST — Martin Fowler

- https://martinfowler.com/articles/richardsonMaturityModel.html

  

Modelo de maturidade REST:
- Level 0 → Level 3

📌 Excelente para avaliar APIs.

  

---

### 📘 HTTP Status Codes

- https://developer.mozilla.org/en-US/docs/Web/HTTP/Status

  

Use sempre para:
- Escolher status correto
- APIs previsíveis
  

---

  
## 📦 Dev & Ecossistema

  

### 🔹 Maven

- https://maven.apache.org/guides/

  

### 🔹 Git

- https://git-scm.com/doc

  

### 🔹 GitHub

- https://docs.github.com/

  

---

  

## 🧭 Evolução Contínua (Próximos Passos)

  

Tópicos futuros para este Vault:

- ✅ Swagger / OpenAPI
- ✅ Spring Security
- ✅ JWT
- ✅ Docker
- ✅ Testcontainers
- ✅ Observabilidade (logs, métricas)

---

  

## 🧠 Nota Final

> Um engenheiro de software não sabe tudo, 
> mas sabe **onde procurar**, **como validar** 
> e **quando aplicar**.