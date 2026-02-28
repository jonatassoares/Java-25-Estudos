# Métodos
  

> Fase 1 — Fundamentos 
> Aqui você aprende a **organizar a lógica**, evitar repetição e escrever código limpo. 
> Métodos são um dos pilares da programação profissional.


---
  

## 🎯 Objetivo deste arquivo

  

Ao finalizar este material, você deve ser capaz de:
- Entender o que são métodos
- Criar métodos com e sem retorno
- Passar parâmetros corretamente
- Reutilizar código
- Ler métodos e entender o que eles fazem

✅ **Se você copia código repetido, está na hora de aprender métodos.**

  

---

  

## 🧠 O que é um método?

  

Um método é:

> Um **bloco de código nomeado** que executa uma tarefa específica.

  

Ele serve para:
- Organizar o código
- Evitar repetição
- Facilitar manutenção
- Tornar o código legível
  

---

  

## 🧱 Estrutura de um Método

  
```Java
modificador retorno nome(parametros) {
    // corpo do método
}
```

Exemplo:

```Java
public static void saudacao() {
	System.out.println("Olá!");
}
```

---

## 🧩 Partes do Método

```Java
public static void saudacao() {
```

- `public` → quem pode acessar
- `static` → pertence à classe (por enquanto)
- `void` → não retorna valor
- `saudacao` → nome do método
- `()` → parâmetros (vazio neste caso)

---

## ▶️ Chamando um Método

```Java
public static void main(String[] args) {
	saudacao();
}
```
📌 **Criar o método não executa ele**.  
📌 É preciso chamá-lo.

---

## 🔁 Métodos sem Retorno (`void`)

```Java
public static void imprimirMensagem() {
	System.out.println("Estudando Java!");
}
```

Usado quando:

- Apenas executa uma ação
- Não precisa devolver resultado

---

## 🔢 Métodos com Retorno

```Java
public static int somar(int a, int b) {
	return a + b;
}
```

Uso:

```Java
int resultado = somar(2, 3);  

System.out.println(resultado);  
```
📌 O tipo do `return` deve bater com o tipo do método.

---

## 📥 Parâmetros

Parâmetros são:

> Valores que o método recebe para trabalhar.

```Java
public static void exibirNome(String nome) {
	System.out.println(nome);
}
```

Chamada:

```Java
exibirNome("João");
```

---

## 🔄 Vários Parâmetros

```Java
public static double calcularMedia(double n1, double n2) {
	return (n1 + n2) / 2;
}
```

---

## ⚠️ Erros Comuns de Iniciantes

❌ Esquecer de chamar o método  
❌ Retornar valor em método `void`  
❌ Criar métodos gigantes  
❌ Nomes genéricos (`metodo1`, `teste`)

✅ Use nomes claros e objetivos.

---

## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:

1️⃣ Crie um método que exiba seu nome  
2️⃣ Crie um método que receba dois números e exiba a soma  
3️⃣ Crie um método que retorne o dobro de um número  
4️⃣ Chame todos no `main`

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

> Um bom método faz **uma coisa só** — e faz bem.

---

## 🧪 Mini Desafio

Crie um programa que:

- Tenha um método `ehPar(int numero)`
- Retorne `true` se o número for par
- Retorne `false` caso contrário
- Use o retorno no `main`

✅ Não imprima direto no método  
✅ Use o retorno corretamente

---

## 🧭 Checklist de Conclusão

Antes de avançar:

```Markdown
- [ ] Sei criar métodos
- [ ] Sei usar parâmetros
- [ ] Sei retornar valores
- [ ] Evitei código repetido
- [ ] Consegui resolver o mini desafio

```

---

## ✅ Conclusão

Se métodos ficaram claros, você **subiu de nível**.  
Agora você está pronto para **organizar programas maiores**.

➡️ Próximo arquivo: [[Exercicios]]

---

## 📝 Anotações Pessoais

Espaço livre:
```Markdown

```
