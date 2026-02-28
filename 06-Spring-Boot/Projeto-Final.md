# Projeto Final — API REST Profissional com Spring Boot

> Fase 6 — Projeto Final 
> Este projeto representa **o ponto de chegada do plano de estudos**. 
> Se você concluir isso sozinho, você está **pronto para o mercado Java**.

---
## 🎯 Objetivo do Projeto

Desenvolver uma **API REST completa**, aplicando:

- ✅ Java moderno
- ✅ Spring Boot
- ✅ API REST
- ✅ JPA / Hibernate
- ✅ Banco de dados
- ✅ DTOs
- ✅ Boas práticas
- ✅ Organização em camadas

📌 Este projeto pode (e deve) ir para o **GitHub**.

---

## 🧠 Contexto do Sistema


Você irá criar um **Sistema de Gerenciamento de Tarefas** (To-Do API).

O sistema deve permitir:
- Criar tarefas
- Listar tarefas
- Atualizar tarefas
- Remover tarefas
- Marcar tarefas como concluídas

---

## 🧱 Regras Gerais do Projeto

✅ API REST 
✅ JSON como formato 
✅ Arquitetura em camadas 
✅ Controller sem regra de negócio 
✅ Service com regras 
✅ Repository para persistência 
✅ Uso de DTO 
✅ Tratamento de erros 

---

## 🧩 Arquitetura do Projeto

```text
controller → service → repository → banco
```

Pacotes sugeridos:
```Plain Text
com.exemplo.tarefas
├── controller
├── service
├── repository
├── domain
├── dto
└── exception
```

---

## 🧱 Entidade — Tarefa

```Java
@Entity
@Table(name = "tarefas")
public class Tarefa {
	
	@Id
	@GeneratedValue(strategy = GenerationType.IDENTITY)
	private Long id;
	
	private String titulo;
	private String descricao;
	private boolean concluida;  
	
	protected Tarefa() {
	}
	
	public Tarefa(String titulo, String descricao) {
		this.titulo = titulo;
		this.descricao = descricao;
		this.concluida = false;
	}
	
	public Long getId() {
		return id;
	}
	
	public String getTitulo() {
		return titulo;
	}
	
	public String getDescricao() {
		return descricao;
	}
	
	public boolean isConcluida() {
		return concluida;
	}
	
	public void concluir() {
		this.concluida = true;
	}
}
```

---

## 🧩 DTOs

### DTO de Entrada

```Java
public record TarefaRequest(String titulo, String descricao) {
}
```

### DTO de Saída

```Java
public record TarefaResponse(
	Long id,
	String titulo,
	String descricao,
	boolean concluida
) {
}
```

---

## 🧩 Repository

```Java
public interface TarefaRepository
		extends JpaRepository<Tarefa, Long> {
}
```

---

## 🧱 Service

```Java
@Service
public class TarefaService {  
	
	private final TarefaRepository repository;  
	
	public TarefaService(TarefaRepository repository) {  
		this.repository = repository;
	}
	
	public List<Tarefa> listar() {  
		return repository.findAll();  
	}  
	
	public Tarefa criar(TarefaRequest request) {  
		Tarefa tarefa = new Tarefa(
			request.titulo(),
			request.descricao()  
		);  
		return repository.save(tarefa);  
	}  
	
	public Tarefa concluir(Long id) {  
		Tarefa tarefa = repository.findById(id)  
			.orElseThrow(() -> new RuntimeException("Tarefa não encontrada"));  
		
		tarefa.concluir();
		return repository.save(tarefa);  
	}
	
	public void remover(Long id) {
		repository.deleteById(id);
	}
}
```

---

## 🌐 Controller

```Java
@RestController
@RequestMapping("/tarefas")
public class TarefaController {
	
	private final TarefaService service;  
	
	public TarefaController(TarefaService service) {
		this.service = service;
	}
	
	@GetMapping
	public List<TarefaResponse> listar() {
		return service.listar()
			.stream()
			.map(t -> new TarefaResponse(
					t.getId(),
					t.getTitulo(),
					t.getDescricao(),
					t.isConcluida()
			))
			.toList();
	}
	
	@PostMapping  
	public TarefaResponse criar(@RequestBody TarefaRequest request) {
		Tarefa tarefa = service.criar(request);
		return new TarefaResponse(
			tarefa.getId(),
			tarefa.getTitulo(),
			tarefa.getDescricao(),
			tarefa.isConcluida()
		);
	}
	
	@PutMapping("/{id}/concluir")
	public TarefaResponse concluir(@PathVariable Long id) {
		Tarefa tarefa = service.concluir(id);
		return new TarefaResponse(
			tarefa.getId(),
			tarefa.getTitulo(),
			tarefa.getDescricao(),
			tarefa.isConcluida()
		);
	}
	
	@DeleteMapping("/{id}")
	public void remover(@PathVariable Long id) {
		service.remover(id);
	}
}
```

---

## ⚠️ Tratamento de Erros (Opcional, mas Recomendado)

```Java
@RestControllerAdvice
public class GlobalExceptionHandler {  

	@ExceptionHandler(RuntimeException.class)
	public ResponseEntity<String> handle(RuntimeException ex) {
		return ResponseEntity.badRequest().body(ex.getMessage());
	}
}
```

---

## 🧪 Testes (Opcional, Diferencial)

- Testes unitários no Service
- Testes de Controller com MockMvc

✅ Não obrigatório  
✅ Muito valorizado

---

## 🧠 O que este projeto demonstra?

✅ Organização em camadas  
✅ Uso correto de Spring Boot  
✅ API REST limpa  
✅ JPA integrado  
✅ DTOs  
✅ Código profissional

---

## 🚀 Desafios Extras (Portfólio Forte)

### 🔹 Desafio 1

Adicionar:
- Data de criação
- Data de conclusão

---

### 🔹 Desafio 2

Adicionar:
- Paginação no endpoint de listagem

---

### 🔹 Desafio 3

Adicionar:
- Filtro de tarefas concluídas

---

### 🔹 Desafio 4

Adicionar:
- Testes unitários

---

## 🧭 Checklist Final do Curso

```Markdown
- [ ] Concluí todas as fases
- [ ] Entendo Java moderno
- [ ] Entendo POO
- [ ] Sei criar API REST
- [ ] Sei usar JPA
- [ ] Tenho um projeto no GitHub
```

---

## 🎓 Conclusão Final

🎉 **Parabéns!**  
Você percorreu **todo o caminho do Java moderno até uma API profissional**.

Se você:
- Consegue explicar esse projeto
- Consegue modificar sem medo
- Consegue criar outro parecido do zero

👉 Então você **ESTÁ PRONTO PARA O MERCADO**.

---

## 📝 Anotações Finais

Registre aqui:
- O que aprendeu
- Pontos fortes
- Próximos passos

```Markdown

```
