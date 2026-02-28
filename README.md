# ✅ API REST de Gerenciamento de Tarefas — Spring Boot

  
Projeto desenvolvido com **Java moderno e Spring Boot**, aplicando boas práticas de arquitetura, API REST e persistência de dados com JPA/Hibernate.

> 🎯 Objetivo: demonstrar domínio prático de **Java + Spring Boot** em um projeto real, pronto para portfólio profissional.


---

## 🚀 Visão Geral

  
Esta aplicação é uma **API REST para gerenciamento de tarefas (To-Do)**, permitindo:

- Criar tarefas
- Listar tarefas
- Concluir tarefas
- Remover tarefas
- Persistir dados em banco de dados

O projeto segue **arquitetura em camadas**, uso de **DTOs**, **JPA**, **Spring Data** e princípios de **Clean Code**.  

---

## 🧠 Tecnologias Utilizadas

- **Java 21+**
- **Spring Boot**
- **Spring Web**
- **Spring Data JPA**
- **Hibernate**
- **Banco de dados H2** (ambiente de desenvolvimento)
- **Maven**
- **API REST**
- **DTOs (Data Transfer Objects)**

---

## 🏗️ Arquitetura do Projeto

```text
controller → service → repository → banco de dados
```

### Estrutura de Pacotes

```Markdown
com.exemplo.tarefas
├── controller
├── service
├── repository
├── domain
├── dto
└── exception
```

✅ Separação clara de responsabilidades  
✅ Código organizado e escalável

---

## 📦 Modelo de Dados

### Entidade Principal — Tarefa

- `id`
- `titulo`
- `descricao`
- `concluida`

A entidade é mapeada com **JPA** e persistida automaticamente no banco.

---

## 🌐 Endpoints da API

### 🔹 Listar tarefas

```Plain Text
GET /tarefas
```

---

### 🔹 Criar tarefa

```Plain Text
POST /tarefas
```

**Body (JSON):**

```JSON
{
	"titulo": "Estudar Spring Boot",
	"descricao": "Criar API REST com JPA"
}
```

---

### 🔹 Concluir tarefa

```Plain Text
PUT /tarefas/{id}/concluir  
```

---

### 🔹 Remover tarefa

```Plain Text
DELETE /tarefas/{id}  
```

---

## 🧩 Padrões e Boas Práticas Aplicadas

✅ API REST semântica  
✅ Controllers finos  
✅ Services com regra de negócio  
✅ DTOs para entrada e saída  
✅ JPA com Spring Data  
✅ Encapsulamento  
✅ Código limpo e legível

---

## ⚠️ Tratamento de Erros

- Exceções tratadas de forma centralizada
- Mensagens claras para o cliente da API
- Evita falhas inesperadas

---

## 🧪 Testes (Opcional / Expansão)

O projeto está preparado para:
- Testes unitários no Service
- Testes de Controller com MockMvc

> 📌 Testes não são obrigatórios neste estágio, mas são um **diferencial profissional**.

---

## ▶️ Como Executar o Projeto

### Pré-requisitos

- Java 21+
- Maven

### Passos

```Shell
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
mvn spring-boot:run
```

A aplicação estará disponível em:

```Plain Text
http://localhost:8080
```

---

## 🗄️ Console do Banco H2 (Dev)

```Plain Text
http://localhost:8080/h2-console
```

Configuração padrão:

- JDBC URL: `jdbc:h2:mem:testdb`
- User: `sa`
- Password: _(vazio)_

---

## 🎯 Próximas Evoluções (Roadmap)

- ✅ Paginação
- ✅ Filtros por status
- ✅ Datas de criação e conclusão
- ✅ Testes automatizados
- ✅ Autenticação (JWT)
- ✅ Documentação com Swagger

---

## 👨‍💻 Autor

Desenvolvido por **Jônatas Barbosa Soares**  
📌 Projeto criado para **aprendizado avançado e portfólio Java/Spring Boot**

---

## 📄 Licença

Este projeto é livre para fins de estudo e aprendizado.