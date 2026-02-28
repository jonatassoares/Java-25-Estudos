# Streams API

> Fase 3 — Java Moderno 
> Aqui você aprende a **processar coleções de forma declarativa e poderosa**. 
> Streams mudam completamente a forma de escrever Java.

  

---

  

## 🎯 Objetivo deste arquivo

  

Ao finalizar este material, você deve ser capaz de:

- Entender o que é uma Stream
- Criar pipelines com Streams
- Usar operações intermediárias e terminais
- Combinar Streams com Lambdas
- Escrever código mais legível e expressivo
  

✅ **Streams não armazenam dados — elas processam dados.**

  

---

  

## 🧠 O que é uma Stream?

  

Uma Stream é:

> Um **fluxo de dados** que permite processar coleções passo a passo.

  

Características importantes:

- Não altera a coleção original

- Executa operações em sequência (pipeline)

- Pode ser reutilizada **apenas uma vez**

  

---

  

## 🧱 Stream x Collection

  

| Collection           | Stream         |
| -------------------- | -------------- |
| Armazena dados       | Processa dados |
| Pode ser reutilizada | Uso único      |
| Estrutura            | Pipeline       |

📌 Collection = dados 

📌 Stream = processamento 

  

---

  

## 🔄 Criando uma Stream

  

A partir de uma coleção:

  

```Java
List<Integer> numeros = List.of(1, 2, 3, 4, 5);

numeros.stream();
```
📌 Sozinha, a stream **não faz nada**.

---

## 🧩 Pipeline de Stream

Uma Stream funciona assim:

```Plain Text
Fonte → Operações Intermediárias → Operação Terminal
```

Exemplo:

```Java
numeros.stream()
	   .filter(n -> n % 2 == 0)
	   .map(n -> n * 2)
	   .forEach(System.out::println);
```

---

## 🔧 Operações Intermediárias

São operações que:

- Retornam outra Stream
- Não executam imediatamente

### `filter`
```Java
.filter(n -> n > 3)
```

### `map`
```Java
.map(n -> n * 2)
```

### `sorted`
```Java
.sorted()
```

---

## ✅ Operações Terminais

São operações que:

- Executam a Stream
- Produzem um resultado final

### `forEach`
```Java
.forEach(System.out::println);
```

### `collect`
```Java
.collect(Collectors.toList());
```

### `count`
```Java
.count();
```

---

## 🧠 Exemplo Completo

```Java
List<String> nomes = List.of("Ana", "Bruno", "Carlos", "Amanda");  

List<String> resultado = nomes.stream()  
	.filter(n -> n.startsWith("A"))
	.map(String::toUpperCase)
	.sorted()
	.collect(Collectors.toList());

System.out.println(resultado);  

```

Saída:
```Plain Text
[AMANDA, ANA]  
```

---

## 🔁 Streams NÃO substituem loops sempre

✅ Use Stream quando:

- Transformar dados
- Filtrar
- Mapear
- Agrupar

❌ Evite Stream quando:

- Lógica muito complexa
- Muitos efeitos colaterais
- Código fica ilegível

---

## ⚠️ Erros Comuns de Iniciantes

❌ Tentar reutilizar Stream  
❌ Colocar lógica complexa no lambda  
❌ Usar Stream para tudo  
❌ Alterar estado externo dentro da Stream

✅ Streams funcionam melhor com **imutabilidade**.

---

## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:

1️⃣ Crie uma lista de números  
2️⃣ Filtre apenas pares  
3️⃣ Multiplique por 10  
4️⃣ Imprima o resultado

Depois:

- Conte quantos números sobraram

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

> Streams fazem você pensar em **transformação de dados**, não em controle de fluxo.

---

## 🧪 Mini Desafio

Crie uma lista de pessoas (String com nomes) e:

- Filtre nomes com mais de 4 letras
- Converta para maiúsculo
- Ordene alfabeticamente
- Retorne uma nova lista

✅ Use Stream  
✅ Não altere a lista original

---

## 🧭 Checklist de Conclusão

Antes de avançar:

```Markdown
- [ ] Sei o que é Stream
- [ ] Sei usar filter e map
- [ ] Sei usar collect
- [ ] Sei criar pipelines
- [ ] Resolvi o mini desafio
```

---

## ✅ Conclusão

Agora você domina a **base do processamento funcional em Java** ✅  
O próximo passo é tratar **ausência de valor** de forma segura.

➡️ Próximo arquivo: [[04-Optional-e-Records]]

---

## 📝 Anotações Pessoais

Use este espaço livremente:
```Markdown

```
