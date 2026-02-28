# Controle de Fluxo    

> Fase 1 — Fundamentos  
> Aqui você aprende a **tomar decisões e repetir ações** em Java.  
> Esse arquivo é crucial para pensar como programador.  


---  

  

## 🎯 Objetivo deste arquivo  

  

Ao finalizar este material, você deve ser capaz de:  
- Tomar decisões com `if`, `else` e `switch` 
- Repetir ações com `for`, `while` e `do-while`  
- Entender quando usar cada estrutura  
- Evitar erros lógicos comuns  
  

✅ **Se você não entende o fluxo do código, o programa controla você.**  

  

---  

  

## 🧠 O que é Controle de Fluxo?  

  

Controle de fluxo define:  

> **Qual caminho o programa segue** durante a execução.  

  

Exemplo do mundo real:  

- Se estiver chovendo → levo guarda-chuva  
- Senão → não levo  

  

Em Java, isso vira código.  

  

---  

  

## 🔀 Estruturas Condicionais  

  

### ✅ `if` 

```java
int idade = 20;  

if (idade >= 18) {  
	System.out.println("Maior de idade");  
}  

```
📌 O bloco só executa se a condição for `true`.

---

### ✅ `if / else`

```Java
int idade = 16;  


if (idade >= 18) {  
	System.out.println("Maior de idade");
} else {
	System.out.println("Menor de idade");
}
```
📌 Um caminho **ou** outro.

---

### ✅ `else if`

```Java
int nota = 7;  

if (nota >= 9) {  
	System.out.println("Excelente");  
} else if (nota >= 7) {  
	System.out.println("Aprovado");  
} else {  
	System.out.println("Reprovado");  
}
```
📌 Avaliação em cascata.

---

## 🧠 Operadores Relacionais e Lógicos

### Relacionais

- `>` maior que
- `<` menor que
- `>=` maior ou igual
- `<=` menor ou igual
- `==` igual
- `!=` diferente

### Lógicos

- `&&` (E)
- `||` (OU)
- `!` (NÃO)

Exemplo:

```Java
if (idade >= 18 && temDocumento) {  
	System.out.println("Pode entrar");
}
```

---

## 🔁 Estruturas de Repetição

### ✅ `for` (quando sabe quantas vezes)

```Java
for (int i = 0; i < 5; i++) {
	System.out.println(i);
}  
```
📌 Muito usado para contadores.

---

### ✅ `while` (condição antes)

```Java
int contador = 0;  

while (contador < 5) {
	System.out.println(contador);
	contador++;
}  
```
📌 Pode não executar nenhuma vez.

---

### ✅ `do-while` (executa ao menos uma vez)

```Java
int contador = 0;  

do {
	System.out.println(contador);
	contador++;
} while (contador < 5);
```
📌 Executa **pelo menos uma vez**.

---

## 🔄 `switch`

```Java
int dia = 3;  

switch (dia) {
	case 1 -> System.out.println("Segunda");
	case 2 -> System.out.println("Terça");
	case 3 -> System.out.println("Quarta");
	default -> System.out.println("Dia inválido");
}
```
📌 Sintaxe moderna (Java 14+).

---

## ⚠️ Erros Comuns de Iniciantes

❌ Esquecer `{}`  
❌ Usar `=` em vez de `==`  
❌ Loop infinito  
❌ Condições confusas demais

✅ Prefira código **simples e legível**.

---

## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:

1️⃣ Verifique se um número é par ou ímpar  
2️⃣ Imprima números de 1 a 10  
3️⃣ Conte regressivamente de 10 até 1  
4️⃣ Use `switch` para exibir um menu simples

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

> Programar é **controlar decisões e repetições**, não decorar sintaxe.

---

## 🧪 Mini Desafio

Crie um programa que:

- Leia uma idade
- Informe se:
    - Criança
    - Adolescente
    - Adulto
    - Idoso

✅ Use `if / else if / else`  
✅ Não escreva textos duplicados

---

## 🧭 Checklist de Conclusão

Antes de avançar:

```Markdown
- [ ] Sei usar if / else 
- [ ] Sei quando usar for ou while 
- [ ] Sei usar switch
- [ ] Evitei loops infinitos
- [ ] Consegui resolver o mini desafio
```

---

## ✅ Conclusão

Se você domina controle de fluxo, **você domina a lógica**.  
O próximo passo é **organizar essa lógica em métodos**.

➡️ Próximo arquivo: [[04-Metodos]]

---

## 📝 Anotações Pessoais

Espaço livre:
```Markdown

```
