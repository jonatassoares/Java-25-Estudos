# Tipos e Variáveis  

> Fase 1 — Fundamentos 
> Aqui você começa a **dar significado aos dados** no Java. 
> Leia, teste e **digite cada exemplo**.

---

## 🎯 Objetivo deste arquivo

  
Ao finalizar este material, você deve ser capaz de:
- Entender o que são **tipos** e **variáveis**
- Saber quando usar cada tipo primitivo
- Declarar e inicializar variáveis corretamente
- Evitar erros comuns de iniciantes
  

✅ **Não avance se ainda confunde tipo com valor.**
  

---
  
## 🧠 O que é uma variável?

  

Uma variável é:

> Um **espaço na memória** que guarda um valor de um **tipo específico**.

  

Em Java, toda variável tem:
1. **Tipo**
2. **Nome**
3. **Valor**

Exemplo:

```java
int idade = 25;
```

- `int` → tipo
- `idade` → nome
- `25` → valor

---

## 📦 Tipos Primitivos em Java

Java possui **8 tipos primitivos**.

|Tipo|Exemplo|Uso comum|
|---|---|---|
|byte|`byte x = 10;`|Dados muito pequenos|
|short|`short x = 300;`|Pouco usado|
|int|`int x = 1000;`|Inteiros (mais comum)|
|long|`long x = 100L;`|Inteiros grandes|
|float|`float x = 2.5f;`|Decimais simples|
|double|`double x = 2.5;`|Decimais (padrão)|
|char|`char c = 'A';`|Um caractere|
|boolean|`boolean ativo = true;`|Verdadeiro/Falso|

📌 **Regra prática**:

- Inteiros → `int`
- Decimais → `double`
- Verdadeiro/Falso → `boolean`

---

## 🔢 Inteiros (int, long)

```Java
int idade = 30;  

long populacao = 214000000L;  
```

📌 O `L` no `long` é obrigatório quando o número é grande.

---

## 🔢 Decimais (float, double)

```Java
double salario = 2500.75;  

float altura = 1.75f;
```

📌 Use `double` como padrão.  
📌 `float` exige `f` no final.

---

## 🔤 Caracteres (char)

```Java
char letra = 'A';

char numero = '1';
```

⚠️ `char` usa **aspas simples**  
⚠️ Apenas **um caractere**

---

## ✅ Boolean (boolean)

```Java
boolean ativo = true;  

boolean maiorDeIdade = false;
```

Muito usado em:

- Condições
- Validações
- Regras de negócio

---

## 🧱 Declarando Variáveis

### Declaração simples

```Java
int numero;

numero = 10;  

```

### Declaração + inicialização

```Java
int numero = 10;
```

✅ Prefira sempre **declarar e inicializar juntos**.

---

## 🧠 Tipagem Forte (Importante!)

Java é **fortemente tipado**.

❌ Isso NÃO é permitido:

```Java
int idade = "vinte";
```

✅ Isso é permitido:

```Java
int idade = 20;
```

📌 O tipo define **o que a variável pode armazenar**.

---

## 🧪 Experimentos Obrigatórios

Faça todos **digitando**, não copiando.

1️⃣ Crie uma variável para:

- Seu nome
- Sua idade
- Sua altura
- Se você está estudando Java

2️⃣ Altere os valores  
3️⃣ Imprima tudo no console

Exemplo:

```Java
System.out.println(nome);
```

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

> Em Java, **escolher o tipo certo** deixa o código mais seguro e legível.

---

## 🧪 Mini Desafio

Crie um programa que exiba no console:

```
Nome: João
Idade: 30
Altura: 1.75
Estuda Java: true  

```

✅ Use variáveis  
✅ Não escreva os valores direto no `println`

---

## 🧭 Checklist de Conclusão

```Markdown
Antes de avançar:
- [ ] Sei o que é uma variável
- [ ] Sei a diferença entre int e double
- [ ] Sei quando usar boolean
- [ ] Entendo erro de tipo
- [ ] Criei variáveis sem copiar código

```  


---

## ✅ Conclusão

Se isso ficou claro, você **dominou a base de qualquer linguagem**.  
Daqui em diante, tudo se constrói sobre isso.

➡️ Próximo arquivo: [[03-Controle-de-Fluxo]]

---

## 📝 Anotações Pessoais

Use este espaço para suas próprias observações:
```Markdown

```