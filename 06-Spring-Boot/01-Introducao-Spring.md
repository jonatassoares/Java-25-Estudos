# Introdução ao Spring Boot

> Fase 6 — Java Profissional
> Aqui você entra no **ecossistema mais usado do mercado Java**.
> Spring Boot transforma Java em aplicações reais.

---
## 🎯 Objetivo deste arquivo

Ao finalizar este material, você deve ser capaz de:
- Entender o que é o Spring Boot
- Saber por que ele é tão usado
- Criar um projeto Spring Boot
- Entender o conceito de Inversão de Controle
- Executar uma aplicação web simples

✅ **A partir daqui, Java deixa de ser só linguagem e vira produto.**

---
## 🧠 O que é Spring?

Spring é:
> Um **framework** que ajuda a criar aplicações Java **robustas, escaláveis e organizadas**.
  

Ele resolve problemas como:
- Criação manual de objetos
- Alto acoplamento
- Configuração complexa
- Dificuldade de teste

---
## 🚀 O que é Spring Boot?

Spring Boot é:
> Uma **forma simplificada** de usar o Spring.

Ele oferece:
- Configuração automática
- Servidor embutido (Tomcat)
- Menos XML
- Mais produtividade

📌 Spring Boot ≠ Spring tradicional 
📌 Spring Boot = Spring **rápido e prático**

---
## 🧠 Por que o Mercado Usa Spring Boot?

✅ Padrão em APIs REST 
✅ Grande comunidade 
✅ Integração com bancos 
✅ Escalável 
✅ Ideal para microserviços 

📌 Se você sabe Spring Boot, você é **empregável**.

---
## 🧱 Inversão de Controle (IoC)

IoC significa:
> O Spring **controla a criação dos objetos**, não você.

Antes ❌:
```Java
Servico servico = new Servico();
```

Com Spring ✅:
```Java
@Autowired
Servico servico;

```
📌 Isso reduz acoplamento e melhora testes.

---
## 🧠 Injeção de Dependência

Injeção de dependência é:
> Entregar as dependências prontas para a classe usar.

Tipos comuns:
- Construtor (recomendado)
- Campo
- Setter

---
## 🧱 Criando um Projeto Spring Boot

### Opção recomendada
- https://start.spring.io

Configuração básica:
- Project: Maven
- Language: Java
- Spring Boot: padrão sugerido
- Packaging: Jar
- Java: 21+
- Dependencies:
    - Spring Web

---
## 🧪 Estrutura Básica do Projeto

```Plain Text
src
└── main
	└── java
		└── com.exemplo.demo
			├── DemoApplication.java
			└── controller
```

---
## ▶️ Classe Principal

```Java
@SpringBootApplication
public class DemoApplication {

	public static void main(String[] args) {
		SpringApplication.run(DemoApplication.class, args);
	}
}
```

📌 Essa classe **inicia a aplicação**.

---

## 🌐 Primeiro Endpoint REST

```Java
@RestController
public class HelloController {

	@GetMapping("/hello")
	public String hello() {
		return "Olá, Spring Boot!";
	}
}
```

Acesse:
```Plain Text
http://localhost:8080/hello
```

---
## 🧠 O que está acontecendo aqui?

- `@RestController` → classe web
- `@GetMapping` → endpoint HTTP GET
- Spring cuida de:
    - Instanciação
    - Roteamento
    - Serialização

---
## ⚠️ Erros Comuns de Iniciantes

❌ Criar objetos com `new`  
❌ Ignorar IoC  
❌ Misturar regras no controller  
❌ Não entender anotações

✅ Spring funciona por **anotações e convenções**.

---
## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:
1️⃣ Crie um projeto Spring Boot  
2️⃣ Execute a aplicação  
3️⃣ Crie um endpoint `/status`  
4️⃣ Retorne `"API rodando"`

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

> Spring Boot cuida da infraestrutura  
> você cuida da **regra de negócio**.

---
## 🧪 Mini Desafio

Crie:
- Um controller com:
    - `/ola`
    - `/data`
- Cada endpoint retorna uma String diferente

✅ Não use `System.out.println`  
✅ Apenas retorno HTTP

---
## 🧭 Checklist de Conclusão

Antes de avançar:

```Markdown
- [ ] Sei o que é Spring Boot
- [ ] Sei criar um projeto
- [ ] Sei rodar a aplicação
- [ ] Criei endpoints REST
- [ ] Entendo IoC
```

---
## ✅ Conclusão

🎉 Parabéns!  
Você entrou oficialmente no **Java de mercado**.

➡️ Próximo arquivo: [[02-API-REST]]

---

## 📝 Anotações Pessoais

Use este espaço para registrar suas primeiras impressões com Spring:
```Markdown

```
