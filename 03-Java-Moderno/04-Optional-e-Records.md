# Optional e Records

> Fase 3 — Java Moderno 
> Aqui você aprende a **eliminar NullPointerException** e a criar **classes simples e imutáveis**.
> Optional e Records são marcas claras de Java moderno.
  

---

## 🎯 Objetivo deste arquivo


Ao finalizar este material, você deve ser capaz de:
- Entender o problema do `null`
- Usar `Optional` corretamente
- Evitar `NullPointerException`
- Criar e usar `record`
- Saber quando usar classes tradicionais ou records
  

✅ **Java moderno é sobre segurança e clareza.**

  

---

# 🔹 PARTE 1 — Optional  

## 🧠 O problema do `null`

Em Java clássico:

```Java
String nome = null;
System.out.println(nome.length()); // NullPointerException
```
❌ Erro em tempo de execução  
❌ Difícil de prever  
❌ Muito comum em sistemas grandes

---

## ✅ O que é Optional?

`Optional` é:
> Um **container** que pode ou não conter um valor.

Ele força você a:
- Pensar na ausência de valor
- Tratar o caso corretamente

---

## 🧱 Criando Optional

```Java
Optional<String> nome = Optional.of("João");
```
⚠️ Nunca use `Optional.of(null)`.

### Valor que pode ser nulo

```Java
Optional<String> nome = Optional.ofNullable(possivelNome);
```

### Optional vazio

```Java
Optional<String> nome = Optional.empty();
```

---

## 🔍 Verificando Valor

### `isPresent()`

```Java
if (nome.isPresent()) {
	System.out.println(nome.get());
}
```
⚠️ Evite `get()` sem verificar.

---

## ✅ Forma Moderna (Recomendada)

### `ifPresent`
```Java
nome.ifPresent(n -> System.out.println(n));
```

---

### `orElse`
```Java
String resultado = nome.orElse("Valor padrão");
```

---

### `orElseGet`
```Java
String resultado = nome.orElseGet(() -> "Gerado sob demanda");
```

---

### `orElseThrow`

```Java
String resultado = nome.orElseThrow(() -> new RuntimeException("Nome ausente"));
```

---

## ⚠️ Erros Comuns com Optional

❌ Usar Optional como atributo de classe  
❌ Chamar `get()` direto  
❌ Usar Optional para tudo  
❌ Ignorar o caso vazio

✅ Use Optional principalmente em **retornos de métodos**.

---

## 🧪 Experimentos Obrigatórios (Optional)

Faça **todos digitando**:

1️⃣ Crie um método que retorna `Optional<String>`  
2️⃣ Teste com valor presente e vazio  
3️⃣ Use `ifPresent`  
4️⃣ Use `orElse`

Anote abaixo:

```Markdown
## ⚠️ Erros que aconteceram
- 
- 

## ✅ O que aprendi com esses erros
- 
```

---

# 🔹 PARTE 2 — Records

## 🧠 O que é um Record?

Um `record` é:
> Uma forma curta de criar **classes imutáveis de dados**.

Ele gera automaticamente:
- Construtor
- Getters
- `equals()`
- `hashCode()`
- `toString()`

---

## 🧱 Criando um Record

```Java
public record Pessoa(String nome, int idade) {
}
```

Uso:

```Java
Pessoa p = new Pessoa("Ana", 30);
System.out.println(p.nome());
System.out.println(p.idade());
```
✅ Imutável  
✅ Simples  
✅ Legível

---

## 🧠 Record x Classe Tradicional

| Classe       | Record        |
| ------------ | ------------- |
| Muito código | Código mínimo |
| Mutável      | Imutável      |
| Boilerplate  | Limpo         |
📌 Use record para **DTOs**, **dados de retorno**, **objetos simples**.

---

## 🔒 Imutabilidade

Em record:

```Java
p.nome = "Carlos"; // ❌ não compila
```
✅ Estado protegido  
✅ Código previsível  
✅ Ideal para Streams e APIs

---

## 🧪 Record com Validação

```Java
public record Produto(String nome, double preco) {
	public Produto {
		if (preco < 0) {
			throw new IllegalArgumentException("Preço inválido");
		}
	}
}
```
✅ Construtor compacto  
✅ Regras garantidas

---

## ⚠️ Erros Comuns com Records

❌ Usar record quando precisa mutar estado  
❌ Colocar lógica pesada  
❌ Usar record como entidade JPA  
❌ Confundir record com classe normal

---

## 🧪 Experimentos Obrigatórios (Records)

Faça **todos digitando**:
1️⃣ Crie um record `Livro(titulo, autor)`  
2️⃣ Imprima os dados  
3️⃣ Teste `toString()` automático  
4️⃣ Tente alterar um atributo (veja o erro)

---

## 🧠 Insight Importante
> Optional evita erros  
> Records evitam verbosidade  
> Ambos aumentam a **qualidade do código**.

---

## 🧪 Mini Desafio Final

Crie:
- Um método que retorna `Optional<Pessoa>`
- Use um `record Pessoa`
- Trate o retorno sem usar `null`

✅ Sem `if` desnecessário  
✅ Sem `NullPointerException`

---

## 🧭 Checklist de Conclusão

Antes de avançar:

```
- [ ] Sei usar Optional
- [ ] Sei evitar NullPointerException
- [ ] Sei criar records
- [ ] Sei quando usar record
- [ ] Resolvi o mini desafio
```

---

## ✅ Conclusão da Fase 3

🎉 **Parabéns!**  
Você agora domina os principais recursos do **Java moderno**:
- Collections
- Lambdas
- Streams
- Optional
- Records

➡️ Próxima fase: 📁 **[[04-Excecoes-e-Arquivos]]**

---

## 📝 Anotações Pessoais

Use este espaço para registrar aprendizados e dúvidas:
```Markdown

```
