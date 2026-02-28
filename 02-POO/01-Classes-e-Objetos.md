# Classes e Objetos  

> Fase 2 — Programação Orientada a Objetos (POO) 
> Aqui acontece a **virada de chave**: você começa a pensar em objetos, não mais só em código solto.

  

---

## 🎯 Objetivo deste arquivo

Ao finalizar este material, você deve ser capaz de:
- Explicar o que é uma **classe**
- Explicar o que é um **objeto**
- Criar classes simples
- Instanciar objetos
- Entender a relação entre mundo real e código
  

✅ **Se isso não ficar claro, POO inteira fica confusa.**

---


## 🧠 O que é Programação Orientada a Objetos?

  

POO é um paradigma que organiza o código em:

- **Objetos** → coisas do mundo real

- **Classes** → modelos desses objetos

  

Exemplo do mundo real:
- Pessoa
- Conta bancária
- Produto

No Java, quase **tudo é objeto**.

  

---

  

## 🧱 O que é uma Classe?

  
Uma classe é:

> Um **modelo**, um **molde**, uma **planta**.

  

Ela define:
- Quais dados o objeto terá
- Quais comportamentos ele terá

Exemplo:

```java
public class Pessoa {
    String nome;
    int idade;
}
```
📌 A classe **não é a pessoa**, é o **modelo da pessoa**.

---

## 🧍 O que é um Objeto?

Um objeto é:

> Uma **instância** de uma classe.

Exemplo:
```Markdown
Pessoa p1 = new Pessoa();
p1.nome = "João";
p1.idade = 30;
```
📌 Agora sim existe uma **Pessoa concreta**.

---

## 🧠 Classe x Objeto (Analogia)

| Mundo Real         | Java   |
| ------------------ | ------ |
| Planta de uma casa | Classe |
| Casa construída    | Objeto |
| Receita de bolo    | Classe |
| Bolo pronto        | Objeto |

---

## 🧩 Atributos

Atributos são:

> As **características** do objeto.

Exemplo:

```Java
public class Carro {
	String modelo;
	int ano; 
	boolean ligado;
}
```

---

## 🛠️ Criando Vários Objetos

```Java
Carro c1 = new Carro();
c1.modelo = "Fiat";  
c1.ano = 2020;

Carro c2 = new Carro();  
c2.modelo = "Toyota";  
c2.ano = 2023;
```
📌 Todos seguem o mesmo **modelo (classe)**.

---

## ⚠️ Erros Comuns de Iniciantes

❌ Confundir classe com objeto  
❌ Criar tudo dentro do `main`  
❌ Não dar significado aos atributos  
❌ Pensar só em código, não no problema

✅ Sempre pense:

> “Isso existe no mundo real?”

---

## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:

1️⃣ Crie uma classe `Pessoa`  
2️⃣ Adicione:
- nome
- idade
- altura
3️⃣ Crie dois objetos diferentes  
4️⃣ Imprima os dados no console

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

> Classes **organizam o pensamento**, não apenas o código.

---

## 🧪 Mini Desafio

Crie uma classe `ContaBancaria` com:
- numero
- saldo

Depois:
- Crie duas contas
- Atribua valores diferentes
- Imprima os dados

✅ Ainda sem métodos complexos  
✅ Foque no conceito de objeto

---

## 🧭 Checklist de Conclusão

Antes de avançar:

```Markdown
- [ ] Sei o que é classe
- [ ] Sei o que é objeto
- [ ] Sei criar atributos
- [ ] Sei instanciar objetos
- [ ] Resolvi o mini desafio

```

---

## ✅ Conclusão

Se isso ficou claro, você **entrou oficialmente na POO** 🎉  
Agora vamos **proteger os dados** e organizar melhor o acesso.

➡️ Próximo arquivo: [[02-Encapsulamento]]

---

## 📝 Anotações Pessoais

Use este espaço para suas próprias observações:
```Markdown

```
