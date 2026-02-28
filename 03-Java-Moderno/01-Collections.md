# Collections Framework

> Fase 3 — Java Moderno 
> Aqui você aprende a **trabalhar com grupos de dados de forma profissional**. 
> Collections é um dos assuntos mais importantes do Java moderno.


---

## 🎯 Objetivo deste arquivo

  
Ao finalizar este material, você deve ser capaz de:
- Entender o que é o Collections Framework
- Saber quando usar List, Set e Map
- Percorrer coleções corretamente
- Evitar estruturas antigas como arrays fixos
- Escrever código mais limpo e flexível
  

✅ **Quem domina Collections, domina 80% do Java do dia a dia.**

  

---

  

## 🧠 O que é o Collections Framework?

  

O Collections Framework é:

> Um conjunto de **interfaces e classes** prontas para trabalhar com **coleções de objetos**.

  

Ele resolve problemas como:
- Tamanho dinâmico
- Busca
- Ordenação
- Organização de dados
  

---


## 🧱 Principais Interfaces

  

```text
Collection
├── List
├── Set
└── Queue

Map (fora da hierarquia Collection)
```
📌 **List, Set e Map** são o coração do Java moderno.

---

## 📋 List — Lista Ordenada

Características:

- Mantém ordem de inserção
- Permite elementos duplicados
- Acesso por índice

### Exemplo com `ArrayList`

```Java
List<String> nomes = new ArrayList<>();

nomes.add("Ana");
nomes.add("Carlos");
nomes.add("Ana");

System.out.println(nomes);
```

Saída:

```Plain Text
[Ana, Carlos, Ana]
```

✅ Uso comum:

- Listas
- Resultados de busca
- Sequências

---

## 🔁 Percorrendo uma List

### For tradicional

```Java
for (int i = 0; i < nomes.size(); i++) {
	System.out.println(nomes.get(i));
}
```

### For-each (recomendado)

```Java
for (String nome : nomes) {
	System.out.println(nome);
}
```

---

## 🧠 Set — Conjunto (Sem Duplicatas)

Características:

- Não permite elementos duplicados
- Não garante ordem (depende da implementação)

### Exemplo com `HashSet`

```Java
Set<String> emails = new HashSet<>();

emails.add("a@email.com");
emails.add("b@email.com");
emails.add("a@email.com");

System.out.println(emails);
```

✅ Uso comum:

- Evitar duplicação
- Listas únicas
- Validações

---

## 🧠 List x Set

|List|Set|
|---|---|
|Permite duplicados|Não permite|
|Mantém ordem|Ordem variável|
|Usa índice|Não usa índice|

---

## 🗺️ Map — Chave e Valor

Características:

- Cada valor possui uma **chave única**
- Não permite chave duplicada

### Exemplo com `HashMap`

```Java
Map<String, Integer> idades = new HashMap<>();

idades.put("Ana", 30);
idades.put("Carlos", 25);

System.out.println(idades.get("Ana"));

```
📌 Se a chave não existir, retorna `null`.

✅ Uso comum:

- Dicionários
- Configurações
- Associações

---

## 🔁 Percorrendo um Map

```Java
for (Map.Entry<String, Integer> entry : idades.entrySet()) {
	System.out.println(entry.getKey() + " - " + entry.getValue());
}
```

---

## ⚠️ Erros Comuns de Iniciantes

❌ Usar array quando precisa de List  
❌ Usar List quando precisa evitar duplicação  
❌ Percorrer Map errado  
❌ Não usar interfaces (`List`, `Set`, `Map`)

✅ Sempre programe para a **interface**, não para a implementação.

---

## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:

1️⃣ Crie uma `List` de nomes  
2️⃣ Crie um `Set` de números  
3️⃣ Crie um `Map` com nome → idade  
4️⃣ Percorra todas as coleções

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

> Collections substituem quase todos os usos de arrays em Java moderno.

---

## 🧪 Mini Desafio

Crie um programa que:

- Receba vários nomes
- Armazene em um `Set`
- Imprima apenas nomes únicos

✅ Use Set  
✅ Não use if para validar duplicação

---

## 🧭 Checklist de Conclusão

Antes de avançar:

```Markdown
- [ ] Sei quando usar List
- [ ] Sei quando usar Set
- [ ] Sei quando usar Map
- [ ] Sei percorrer coleções
- [ ] Resolvi o mini desafio

```

---

## ✅ Conclusão

Agora você já trabalha com **estruturas de dados profissionais** ✅  
O próximo passo é **simplificar código com Lambdas**.

➡️ Próximo arquivo: [[02-Lambdas]]

---

## 📝 Anotações Pessoais

Use este espaço livremente:
```Markdown

```
