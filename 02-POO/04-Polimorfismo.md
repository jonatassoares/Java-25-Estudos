# Polimorfismo


> Fase 2 — Programação Orientada a Objetos (POO) 
> Aqui você aprende a **usar objetos diferentes da mesma forma**. 
> Polimorfismo é o que torna a POO realmente poderosa.

---

## 🎯 Objetivo deste arquivo
  

Ao finalizar este material, você deve ser capaz de:
- Entender o que é polimorfismo
- Usar herança + sobrescrita de métodos
- Tratar objetos diferentes de forma uniforme
- Entender por que polimorfismo é essencial em sistemas grandes

✅ **Se herança organiza, polimorfismo flexibiliza.**

---

## 🧠 O que é Polimorfismo?

  

Polimorfismo significa:

> **Muitas formas**.

  

Em POO:

> Objetos de classes diferentes podem ser tratados **como se fossem do mesmo tipo**, mas se comportam de forma diferente.

  

---

  

## 🌍 Exemplo do Mundo Real

  

- Animal faz som 

- Cachorro → late 

- Gato → mia 

  

Todos fazem som, mas **cada um à sua maneira**.

  

---

  

## 🧱 Classe Pai com Método

  

```Java
public class Animal {
    public void fazerSom() {
        System.out.println("O animal faz um som");
    }
}
```

---

## 👶 Classes Filhas Sobrescrevendo o Método

### Cachorro

```Java
public class Cachorro extends Animal {

	@Override
	public void fazerSom() {
		System.out.println("Au au!");
	}
	
}
```

### Gato

```Java
public class Gato extends Animal {

	@Override
	public void fazerSom() {
		System.out.println("Miau!");
	}
	
}
```
📌 `@Override` indica que estamos **alterando o comportamento herdado**.

---

## ▶️ Polimorfismo em Ação

```Java
Animal a1 = new Cachorro();
Animal a2 = new Gato();

a1.fazerSom();  
a2.fazerSom();
```

Saída:
```Plain Text
Au au!
Miau!
```
✅ Mesmo tipo (`Animal`)  
✅ Comportamentos diferentes

---

## 🧠 O que está acontecendo aqui?

- O tipo da variável é `Animal`
- O objeto real é `Cachorro` ou `Gato`
- Java decide **em tempo de execução** qual método chamar

📌 Isso se chama **polimorfismo dinâmico**.

---

## ⚠️ Sem Polimorfismo (Código Ruim)

```Java
if (animal instanceof Cachorro) {
	// comportamento
} else if (animal instanceof Gato) {
	// outro comportamento
}
```
❌ Código frágil  
❌ Difícil de manter  
❌ Viola princípios da POO

---

## ✅ Com Polimorfismo (Código Bom)

```Java
animal.fazerSom();
```
✅ Código simples  
✅ Fácil de estender  
✅ Aberto para novas classes

---

## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:

1️⃣ Crie uma classe `Funcionario`

- método `calcularSalario()`

2️⃣ Crie classes:

- `FuncionarioCLT`
- `FuncionarioPJ`

3️⃣ Sobrescreva `calcularSalario()` em cada uma

4️⃣ Use:

```Java
Funcionario f = new FuncionarioCLT();
```

5️⃣ Chame o método e observe o comportamento

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

> Polimorfismo elimina condicionais  
> e **centraliza o comportamento no lugar certo**.

---

## 🧪 Mini Desafio

Crie:

- Classe `Forma`
    
    - método `calcularArea()`
- Classes:
    
    - `Quadrado`
    - `Circulo`

Cada uma calcula a área corretamente.

Depois:

```Java
Forma f1 = new Quadrado();
Forma f2 = new Circulo();
```

✅ Use polimorfismo  
✅ Nenhum `if` ou `instanceof`

---

## 🚨 Erros Comuns de Iniciantes

❌ Não usar `@Override`  
❌ Misturar polimorfismo com condicionais  
❌ Métodos diferentes com mesmo objetivo  
❌ Quebrar encapsulamento

---

## 🧭 Checklist de Conclusão

Antes de avançar:

```Markdown
- [ ] Sei o que é polimorfismo
- [ ] Sei sobrescrever métodos
- [ ] Sei usar o tipo da classe pai
- [ ] Evitei condicionais desnecessários
- [ ] Resolvi o mini desafio

```

---

## ✅ Conclusão

Agora você entende **por que Java é tão usado em sistemas grandes** ✅  
O próximo passo é **desacoplar ainda mais usando interfaces**.

➡️ Próximo arquivo: [[05-Interfaces]]

---

## 📝 Anotações Pessoais

Use este espaço livremente:
```Markdown

```
