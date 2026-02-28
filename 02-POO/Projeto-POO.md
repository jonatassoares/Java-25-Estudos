# Projeto Integrador — Programação Orientada a Objetos (POO)

> Fase 2 — Projeto Prático 
> Este projeto existe para **fixar POO de verdade**. 
> Se você conseguir fazer isso sozinho, você ENTENDE POO.

---

## 🎯 Objetivo do Projeto

  

Construir um **sistema simples, porém bem modelado**, aplicando:

  
- ✅ Classes e Objetos
- ✅ Encapsulamento
- ✅ Herança
- ✅ Polimorfismo
- ✅ Interfaces
  

📌 **Não é sobre telas ou banco de dados.** 
📌 É sobre **modelagem e código limpo**.

  

---


## 🧠 Contexto do Sistema

  

Você irá criar um **Sistema de Gestão de Funcionários**, onde:

- Existem diferentes tipos de funcionários
- Cada um calcula salário de forma diferente
- O sistema deve ser flexível para novos tipos no futuro
  

---

  

## 🧱 Regras Gerais

  

✅ Cada classe em seu próprio arquivo 

✅ Atributos sempre `private` 

✅ Acesso apenas via métodos 

✅ Evitar `if / else` desnecessários 

✅ Usar polimorfismo sempre que possível 

  

---

  

## 🧩 Modelagem do Sistema

  

### 📌 Interface `Pagavel`

  

```Java
public interface Pagavel {
    double calcularPagamento();
}
```
📌 Define um **contrato** para qualquer entidade pagável.

---

## 👤 Classe Abstrata `Funcionario`

```Java
public abstract class Funcionario implements Pagavel {

	private String nome;
	private double salarioBase;

	public Funcionario(String nome, double salarioBase) {
		this.nome = nome;
		this.salarioBase = salarioBase;
	}

	public String getNome() {
		return nome;
	}

	public double getSalarioBase() {
		return salarioBase;
	}
}
```
✅ Encapsulamento  
✅ Reaproveitamento  
✅ Classe base da hierarquia

---

## 👷 Funcionário CLT

```Java
public class FuncionarioCLT extends Funcionario {

	public FuncionarioCLT(String nome, double salarioBase) {
		super(nome, salarioBase);
	}

	@Override
	public double calcularPagamento() {
		return getSalarioBase() * 1.1; // bônus de 10%
	}
}
```

---

## 🧑‍💻 Funcionário PJ

```Java
public class FuncionarioPJ extends Funcionario {

	public FuncionarioPJ(String nome, double salarioBase) {
		super(nome, salarioBase);
	}

	@Override  
	public double calcularPagamento() {
		return getSalarioBase(); // sem bônus
	}
}
```

---

## ▶️ Classe Principal (`Main`)

```Java
public class Main {  

	public static void main(String[] args) {

		Funcionario f1 = new FuncionarioCLT("João", 3000);
		Funcionario f2 = new FuncionarioPJ("Maria", 4000);

		imprimirPagamento(f1);
		imprimirPagamento(f2);
	}

	public static void imprimirPagamento(Pagavel pagavel) {
		System.out.println("Pagamento: " + pagavel.calcularPagamento());
	}
}
```
✅ Polimorfismo  
✅ Programação orientada a interface  
✅ Código desacoplado

---

## 🧠 O que esse projeto demonstra?

- ✅ **Encapsulamento**  
    → Atributos protegidos e acessados corretamente
    
- ✅ **Herança**  
    → CLT e PJ herdam de Funcionario
    
- ✅ **Polimorfismo**  
    → Cada funcionário calcula pagamento diferente
    
- ✅ **Interface**  
    → Código trabalha com contratos (`Pagavel`)
    

---

## 🧪 Desafios Extras (Opcional, mas recomendado)

### 🔹 Desafio 1

Criar uma nova classe:

- `FuncionarioEstagiario`
- Pagamento = salário base * 0.8

✅ Sem alterar código existente

---

### 🔹 Desafio 2

Criar interface:

```Java
interface Bonificavel {
	double calcularBonus();
}
```

Implementar apenas em:

- `FuncionarioCLT`

---

### 🔹 Desafio 3

Criar uma lista de funcionários e:

- Percorrer usando `for`
- Imprimir nome e pagamento

---

## ⚠️ Armadilhas Comuns

❌ Usar `if (instanceof ...)`  
❌ Colocar lógica no `main`  
❌ Quebrar encapsulamento  
❌ Misturar responsabilidades

✅ Cada classe faz **uma coisa só**.

---

## 🧭 Checklist de Conclusão — Fase 2

Antes de avançar, confirme:

```Markdown
- [ ] Usei encapsulamento corretamente
- [ ] Usei herança sem exagerar
- [ ] Usei polimorfismo
- [ ] Usei interface como contrato
- [ ] Código está organizado
- [ ] Consegui explicar o projeto em voz alta

```

---

## 🎓 Conclusão da Fase 2

🎉 **Parabéns!**  
Se você concluiu este projeto **sem copiar**, você:

✅ Entende POO  
✅ Está pronto para Java moderno  
✅ Pode ler código profissional sem medo

➡️ Próxima fase: 📁 **03-Java-Moderno** - [[01-Collections]], [[02-Lambdas]], [[03-Streams]], [[04-Optional-e-Records]] e [[Pattern-Matching]]

---

## 📝 Anotações Pessoais

Registre aqui:
- Dificuldades
- Decisões de design
- O que faria diferente
```Markdown

```
