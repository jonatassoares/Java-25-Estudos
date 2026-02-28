# API REST com Spring Boot


> Fase 6 — Java Profissional
> Aqui você aprende a **construir APIs REST reais**, organizadas e escaláveis.
> Este é o conhecimento mais cobrado no mercado Java.

---  
## 🎯 Objetivo deste arquivo


Ao finalizar este material, você deve ser capaz de:
- Entender o que é uma API REST
- Criar endpoints REST corretamente
- Usar os métodos HTTP (GET, POST, PUT, DELETE)
- Organizar controllers, services e DTOs
- Retornar respostas HTTP adequadas

✅ **API REST é o idioma padrão entre sistemas.**

---

## 🧠 O que é uma API REST?
  

Uma API REST é:
> Uma interface que permite comunicação entre sistemas via HTTP.

Ela trabalha com:
- URLs (endereços)
- Métodos HTTP
- JSON (principal formato)
- Códigos de status HTTP

---

## 🌐 Métodos HTTP (Essenciais)

| Método | Uso |
|------|----|
| GET | Buscar dados |
| POST | Criar dados |
| PUT | Atualizar dados |
| DELETE | Remover dados |
📌 Cada método tem um **significado semântico**.


---

## 🧱 Estrutura Básica de uma API


```text
Controller → Service → (Repository)
```
- **Controller** → recebe requisições
- **Service** → regra de negócio
- **Repository** → acesso a dados (mais tarde)

✅ Separação de responsabilidades.

---
## 🧩 Criando um Controller REST

```Java
@RestController
@RequestMapping("/clientes")
public class ClienteController {
}
```
- `@RestController` → API REST
- `@RequestMapping` → rota base

---
## 🔍 Endpoint GET

```Java
@GetMapping
public List<String> listar() {
	return List.of("Ana", "Carlos");
}
```

Acesso:
```Plain Text
GET /clientes
```
📌 Spring converte automaticamente para JSON.

---
## ➕ Endpoint POST

```Java
@PostMapping
public String criar(@RequestBody String nome) {
	return "Cliente criado: " + nome;
}
```

Acesso:
```Plain Text
POST /clientes
Body: "João"
```

---
## 🔄 Endpoint PUT

```Java
@PutMapping("/{id}")
public String atualizar(@PathVariable int id,
						@RequestBody String nome) {
	return "Cliente " + id + " atualizado para " + nome;
}
```

---
## ❌ Endpoint DELETE

```Java
@DeleteMapping("/{id}")
public String remover(@PathVariable int id) {
	return "Cliente " + id + " removido";
}
```

---
## 🧠 PathVariable x RequestBody

- `@PathVariable` → vem da URL
- `@RequestBody` → vem do corpo da requisição

📌 Não confundir os dois.

---

## 🧱 Criando um Service

```Java
@Service
public class ClienteService {
	
	public List<String> listar() {
		return List.of("Ana", "Carlos");
	}
}
```

Controller usando Service:

```Java
@RestController
@RequestMapping("/clientes")
public class ClienteController {
	
	private final ClienteService service;
	
	public ClienteController(ClienteService service) {
		this.service = service;
	}
	
	@GetMapping
	public List<String> listar() {
		return service.listar();
	}
}
```
✅ Injeção por construtor  
✅ Código desacoplado

---
## 🧠 DTO (Data Transfer Object)

DTO serve para:
> Controlar o que entra e sai da API.

```Java
public record ClienteDTO(String nome) {
}
```

Uso:

```Java
@PostMapping
public String criar(@RequestBody ClienteDTO dto) {
	return "Cliente criado: " + dto.nome();
}
```
✅ API protegida  
✅ Modelo interno isolado

---
## ⚠️ Erros Comuns de Iniciantes

❌ Colocar regra de negócio no controller  
❌ Retornar entidade diretamente  
❌ Ignorar status HTTP  
❌ Misturar responsabilidades

✅ Controller é **fino**, Service é **grosso**.

---
## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:

1️⃣ Crie um controller `ProdutoController`  
2️⃣ Crie endpoints:
- GET `/produtos`
- POST `/produtos`
- DELETE `/produtos/{id}`

3️⃣ Use um service para lógica

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

> Uma boa API REST é **previsível**,  
> não surpreende quem consome.

---
## 🧪 Mini Desafio

Crie uma API de tarefas:
- Endpoint para listar tarefas
- Endpoint para criar tarefa
- Endpoint para remover tarefa

✅ Use DTO  
✅ Use Service  
✅ Sem lógica no controller

---
## 🧭 Checklist de Conclusão

Antes de avançar:
```Markdown
- [ ] Sei o que é API REST
- [ ] Sei criar endpoints GET/POST/PUT/DELETE
- [ ] Sei usar Controller e Service
- [ ] Sei usar DTO
- [ ] Resolvi o mini desafio
```

---

## ✅ Conclusão

🎉 Parabéns!  
Você já consegue criar **APIs REST profissionais com Spring Boot**.

➡️ Próximo arquivo: [[03-JPA-e-Banco]]

---
## 📝 Anotações Pessoais

Use este espaço para registrar dúvidas e aprendizados:
```Markdown

```
