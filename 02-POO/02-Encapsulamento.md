# Encapsulamento

> Fase 2 — Programação Orientada a Objetos (POO)
> Aqui você aprende a **proteger os dados** e controlar como eles são acessados. 
> Encapsulamento é um dos pilares da POO.

---
## 🎯 Objetivo deste arquivo

  
Ao finalizar este material, você deve ser capaz de:
- Entender o que é encapsulamento
- Usar modificadores de acesso corretamente
- Criar atributos privados
- Criar getters e setters
- Proteger o estado interno de um objeto


✅ **Sem encapsulamento, qualquer código pode quebrar seu objeto.**  

---

## 🧠 O que é Encapsulamento?

  
Encapsulamento é o princípio que diz:

> **Os dados internos de um objeto não devem ser acessados diretamente.**

  

Em vez disso:
- O acesso é feito por **métodos controlados**
- O objeto decide **como** seus dados podem mudar

---

  

## 🧱 Problema: Acesso Direto (Errado)
  

```java
public class Conta {
    double saldo;
}
```

Uso:
```Java
Conta c = new Conta();
c.saldo = -1000;
```
❌ Qualquer valor pode ser atribuído  
❌ Nenhuma regra de negócio  
❌ Objeto inseguro

---

## ✅ Solução: Encapsulamento

### 1️⃣ Tornar atributos `private`

```Java
public class Conta {
	private double saldo;
}
```
📌 Agora o atributo **não pode ser acessado diretamente**.

---

## 🔐 Modificadores de Acesso

|Modificador|Acesso|
|---|---|
|`public`|Acessível por qualquer classe|
|`private`|Acessível apenas na própria classe|
|`protected`|Classe + subclasses|
|_(default)_|Mesmo pacote|

📌 No início, foque em:

> **atributos `private` + métodos `public`**

---

## 🔁 Getters e Setters

Getters e setters são:

> Métodos que **controlam o acesso** aos atributos.

### Getter

```Java
public double getSaldo() {
	return saldo;
}
```

### Setter

```Java
public void setSaldo(double saldo) {  
	this.saldo = saldo;
}
```
📌 `this` refere-se ao atributo da classe.

---

## 🛡️ Encapsulamento com Regra de Negócio

```Java
public void setSaldo(double saldo) {
	if (saldo >= 0) {
		this.saldo = saldo;
	}  
}
```
✅ Agora o objeto **se protege**.

---

## 🧠 Exemplo Completo

```Java
public class Conta {  

	private double saldo;  

	public double getSaldo() {
		return saldo;
	}  

	public void depositar(double valor) {
		if (valor > 0) {
			saldo += valor;
		}
	}

	public void sacar(double valor) {
		if (valor > 0 && valor <= saldo) {
			saldo -= valor;
		}
	}

}  
```

Uso:
```Java
Conta c = new Conta();  
c.depositar(100);  
c.sacar(30);  
System.out.println(c.getSaldo());
```

---

## ⚠️ Erros Comuns de Iniciantes

❌ Deixar tudo `public`  
❌ Criar getter/setter sem sentido  
❌ Colocar regras fora da classe  
❌ Permitir estados inválidos

✅ **O objeto deve se proteger sozinho.**

---

## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:

1️⃣ Crie uma classe `Pessoa` com:

- nome
- idade

2️⃣ Torne os atributos `private`  
3️⃣ Crie getters e setters  
4️⃣ No setter de idade:

- Não permitir idade negativa

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

> Encapsular é **esconder o que não importa**  
> e **expor apenas o necessário**.

---

## 🧪 Mini Desafio

Crie uma classe `Produto` com:
- nome
- preco
Regras:
- Preço não pode ser negativo
- Criar método `aplicarDesconto(double percentual)`
- O desconto não pode deixar o preço negativo

✅ Toda regra deve ficar dentro da classe  
✅ Não altere atributos diretamente

---

## 🧭 Checklist de Conclusão

Antes de avançar:
```Markdown
- [ ] Sei o que é encapsulamento
- [ ] Sei usar private e public
- [ ] Sei criar getters e setters
- [ ] Sei aplicar regras de negócio
- [ ] Resolvi o mini desafio

```

---

## ✅ Conclusão

Agora seus objetos estão **seguros e bem definidos** ✅  
O próximo passo é **reutilizar comportamento** usando herança.

➡️ Próximo arquivo: [[03-Heranca]]

---

## 📝 Anotações Pessoais

Espaço livre para suas observações:
```Markdown

```
