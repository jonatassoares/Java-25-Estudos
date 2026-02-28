# Introdução ao Java

> Fase 1 — Fundamentos 
> Este arquivo é seu **primeiro contato real com Java**. 
> Leia com calma e **digite todos os códigos**.

  

---

  

## 🎯 Objetivo deste arquivo

  

Ao finalizar este material, você deve ser capaz de:

- Explicar o que é Java com suas próprias palavras
- Entender como um programa Java funciona
- Criar e executar seu primeiro programa Java
- Saber diferenciar JDK, JRE e JVM
  

✅ **Não avance se não conseguir escrever o código do zero.**

  

---

  

## ☕ O que é Java?

  

Java é uma linguagem de programação que possui as seguintes características:

  

- ✅ Orientada a Objetos
- ✅ Fortemente tipada
- ✅ Multiplataforma (Write Once, Run Anywhere)
- ✅ Muito usada no mercado (back-end, APIs, sistemas corporativos)
  

Java **não é só uma linguagem**, é um **ecossistema**.

  

---

  

## 🧠 Como Java funciona (Visão Geral)

  

Fluxo simplificado:

  

```text
Código Java (.java)
        ↓
Compilador (javac)
        ↓
Bytecode (.class)
        ↓
JVM
        ↓
Sistema Operacional
```

### Conceitos importantes

- **Código-fonte**: o que você escreve
- **Bytecode**: código intermediário
- **JVM**: máquina virtual que executa o bytecode

---

## 🧩 JDK, JRE e JVM

### ✅ JVM (Java Virtual Machine)

- Executa o bytecode
- Torna Java multiplataforma

### ✅ JRE (Java Runtime Environment)

- JVM + bibliotecas
- Necessário apenas para **rodar** programas

### ✅ JDK (Java Development Kit)

- JRE + compilador + ferramentas
- Necessário para **desenvolver**

📌 **Para estudar Java, você SEMPRE usa o JDK.**

---

## 🛠️ Preparando o Ambiente

### O que você precisa

- JDK instalado (Java 21 LTS ou Java 25)
- Editor ou IDE:
    - IntelliJ IDEA (recomendado)
    - VS Code
    - Eclipse

✅ Verifique no terminal:

```Shell
java --version

javac --version  

```

---

## 🧪 Seu Primeiro Programa Java

### Código mínimo funcional

```Java
public class Main {

    public static void main(String[] args) {
        System.out.println("Olá, Java!");
    }

}
```

---

## 🔍 Entendendo o código linha por linha

```Java
public class Main {
```

- Define uma **classe**
- O nome da classe deve ser igual ao nome do arquivo (`Main.java`)

```Java
public static void main(String[] args) {
```

- Método principal
- **Ponto de entrada do programa**
- Sempre igual (por enquanto)

```Java
System.out.println("Olá, Java!");  
```

- Exibe texto no console

---

## 📌 Regras importantes (grave isso)

- ✅ Todo programa Java começa pelo `main`
- ✅ Java diferencia maiúsculas e minúsculas
- ✅ Cada instrução termina com `;`
- ✅ Código Java vive dentro de classes

---

## 🧪 Experimentos Obrigatórios

Faça **todos**, sem copiar e colar.

1️⃣ Troque o texto exibido  
2️⃣ Exiba seu nome  
3️⃣ Exiba duas linhas diferentes  
4️⃣ Gere um erro de propósito (remova `;`) e veja o que acontece

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

> Java parece verboso no começo, mas essa “chatice” vira **clareza e segurança** em projetos grandes.

---

## 🧪 Mini Desafio

Crie um programa que exiba:

```Plain Text
=====================
Meu primeiro programa
em Java
=====================
```

✅ Sem copiar código pronto  
✅ Apenas usando `System.out.println`

---

## 🧭 Checklist de Conclusão

Antes de avançar, confirme:

```Markdown
- [ ] Sei explicar o que é Java
- [ ] Sei o que é JVM, JRE e JDK
- [ ] Criei e executei um programa Java
- [ ] Entendi a estrutura do main
- [ ] Cometi erros e aprendi com eles
```

---

## ✅ Conclusão

Se você chegou até aqui **digitando código**, parabéns 🎉  
Você deu o passo mais importante: **começou corretamente**.

➡️ Próximo arquivo: [[02-Tipos-e-Variaveis]]

---

## 📝 Anotações Pessoais

Use este espaço livremente:
```Markdown

```