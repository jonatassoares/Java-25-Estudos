# JPA e Banco de Dados

> Fase 6 — Java Profissional 
> Aqui você aprende a **persistir dados em banco** usando Spring Boot + JPA. 
> Sem banco de dados, não existe aplicação real.

---
## 🎯 Objetivo deste arquivo

Ao finalizar este material, você deve ser capaz de:
- Entender o que é JPA
- Mapear classes para tabelas
- Usar Spring Data JPA
- Criar CRUD com banco de dados
- Integrar API REST com persistência

✅ **Seus dados agora sobrevivem ao desligar da aplicação.**

---
## 🧠 O que é JPA?

JPA (Java Persistence API) é:
> Uma **especificação** para mapeamento objeto–relacional (ORM).

Ela permite:
- Converter classes Java ↔ tabelas do banco
- Evitar SQL manual na maioria dos casos
- Trabalhar com objetos em vez de registros

📌 Implementação mais usada: **Hibernate**

---
## 🗄️ O que é ORM?

ORM significa:

> Object-Relational Mapping

| Java     | Banco  |
| -------- | ------ |
| Classe   | Tabela |
| Objeto   | Linha  |
| Atributo | Coluna |

---
## 🧱 Dependências Necessárias

No `start.spring.io`, adicione:
- **Spring Data JPA**
- **H2** (para testes) ou **PostgreSQL/MySQL**

---
## 🧩 Configuração Básica (`application.yml`)

Exemplo com H2:

```yml
spring:
  datasource:
    url: jdbc:h2:mem:testdb
    driver-class-name: org.h2.Driver
    username: sa
    password:

  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true

  h2:
    console:
      enabled: true
```
      
      Acesse:
```Plain Text
http://localhost:8080/h2-console
```

---
## 🧱 Criando uma Entidade

```Java
@Entity
@Table(name = "clientes")
public class Cliente {
	
	@Id
	@GeneratedValue(strategy = GenerationType.IDENTITY)
	private Long id;
	private String nome;
	
	protected Cliente() {
	}
	
	public Cliente(String nome) {
		this.nome = nome;
	}
	
	public Long getId() {
		return id;
	}
	
	public String getNome() {
		return nome;
	}
}
```
✅ `@Entity` → classe persistente  
✅ `@Id` → chave primária  
✅ Construtor vazio obrigatório

---
## 🧠 Entity ≠ DTO

- **Entity** → modelo do banco
- **DTO** → modelo da API

✅ Nunca exponha Entity diretamente.

---

## 🧩 Criando um Repository

```Java
public interface ClienteRepository
		extends JpaRepository<Cliente, Long> {
}
```
✅ CRUD automático  
✅ Sem SQL  
✅ Interface simples

---
## 🧱 Usando Repository no Service

```Java
@Service  
public class ClienteService {

	private final ClienteRepository repository;  
	
	public ClienteService(ClienteRepository repository) {
		this.repository = repository;
	}
	
	public List<Cliente> listar() {
		return repository.findAll();
	}
	
	public Cliente salvar(String nome) {
		return repository.save(new Cliente(nome));
	}
}
```

---
## 🌐 Controller com Banco

```Java
@RestController
@RequestMapping("/clientes")
public class ClienteController {
	
	private final ClienteService service;
	
	public ClienteController(ClienteService service) {
		this.service = service;
	}
	
	@GetMapping
	public List<ClienteDTO> listar() {
		return service.listar()
					.stream()
					.map(c -> new ClienteDTO(c.getId(), c.getNome()))
					.toList();
	}
	
	@PostMapping
	public ClienteDTO criar(@RequestBody ClienteDTO dto) {
		Cliente cliente = service.salvar(dto.nome());
		return new ClienteDTO(cliente.getId(), cliente.getNome());
	}
}
```

---
## 🧩 DTO Usado

```Java
public record ClienteDTO(Long id, String nome) {
}
```
✅ API desacoplada  
✅ Segurança  
✅ Clareza

---
## ⚠️ Erros Comuns de Iniciantes

❌ Retornar Entity direto  
❌ Colocar lógica no controller  
❌ Ignorar DTO  
❌ Não entender `ddl-auto`

✅ JPA exige **disciplina de arquitetura**.

---
## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:
1️⃣ Crie entidade `Produto`  
2️⃣ Crie `ProdutoRepository`  
3️⃣ Crie `ProdutoService`  
4️⃣ Crie endpoints CRUD  
5️⃣ Teste no Postman ou navegador

Anote abaixo:
```Markdown
## ⚠️ Erros que aconteceram
- 
- 

## ✅ O que aprendi com esses erros
- 
```

---
## 🧠 Insight Importante

> JPA transforma banco de dados  
> em **parte natural do código Java**.

---
## 🧪 Mini Desafio

Crie uma API de pedidos:
- Pedido
- ItemPedido
- Relacionamento simples
- CRUD completo

✅ Use JPA  
✅ Use DTO  
✅ Use Service

---

## 🧭 Checklist de Conclusão

Antes de avançar:
```Markdown
- [ ] Sei o que é JPA
- [ ] Sei criar entidades
- [ ] Sei usar Repository
- [ ] Sei integrar banco à API
- [ ] Resolvi o mini desafio
```

---
## ✅ Conclusão

🎉 Parabéns!  
Agora sua API é **persistente e profissional**.

➡️ Próximo arquivo: [[Projeto-Final]]

---
## 📝 Anotações Pessoais

Use este espaço para registrar dificuldades e aprendizados:
```Markdown

```
