# Herança

> Fase 2 — Programação Orientada a Objetos (POO) 
> Aqui você aprende a **reutilizar código** e criar relações claras entre classes. 
> Herança é poderosa — e perigosa se usada errado.

---

## 🎯 Objetivo deste arquivo

Ao finalizar este material, você deve ser capaz de:
- Entender o que é herança
- Usar `extends`
- Criar classes pai e filho
- Reutilizar atributos e métodos
- Saber quando **usar** e quando **evitar** herança
  

✅ **Herança resolve reutilização, não bagunça.**
  

---

## 🧠 O que é Herança?

  

Herança é o conceito que permite:

> Uma classe **herdar características e comportamentos** de outra.

- Classe **pai** (superclasse)

- Classe **filha** (subclasse)

  

Exemplo do mundo real:
- Animal → Cachorro
- Veículo → Carro
- Pessoa → Aluno

---

## 🧱 Classe Pai (Superclasse)

  

```Java
public class Animal {
    protected String nome;

    public void dormir() {
        System.out.println("Dormindo...");
    }

}
```
📌 A classe pai contém o que é **comum**.

---

## 👶 Classe Filha (Subclasse)

```Java
public class Cachorro extends Animal {
	public void latir() {
		System.out.println("Au au!");
	}
}
```
📌 `extends` cria a relação de herança.

---

## ▶️ Usando a Herança

```Java
Cachorro dog = new Cachorro();
dog.nome = "Rex";
dog.latir();
dog.dormir();
```

✅ `latir()` → da classe filha  
✅ `dormir()` → herdado da classe pai

---

## 🧠 protected vs private

- `private` → só a própria classe acessa
- `protected` → classe + subclasses

📌 Em herança, `protected` é comum para atributos compartilhados.

---

## 🔄 Reutilização de Código

Sem herança ❌:

- Código duplicado
- Manutenção difícil

Com herança ✅:

- Código centralizado
- Alterações em um só lugar

---

## ⚠️ Herança NÃO é “tem um”

Herança representa **“é um”**, não **“tem um”**.

✅ Correto:

- Cachorro **é um** Animal

❌ Errado:

- Carro **é um** Motor (não!)

📌 Se for “tem um”, use **composição**, não herança.

---

## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:

1️⃣ Crie uma classe `Pessoa` com:

- nome
- idade
- método `apresentar()`

2️⃣ Crie uma classe `Aluno` que:

- Estenda `Pessoa`
- Tenha atributo `matricula`

3️⃣ Crie um objeto `Aluno` e:

- Acesse dados herdados
- Chame métodos herdados

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

> Use herança para **especializar**, não para reaproveitar qualquer coisa.

---

## 🧪 Mini Desafio

Crie:

- Classe `Funcionario`
    - nome
    - salario
    - método `calcularBonus()`
- Classe `Gerente` que herda de `Funcionario`
    
    - bônus maior que o padrão

✅ Use herança corretamente  
✅ Evite código duplicado

---

## 🚨 Armadilhas Comuns

❌ Herança profunda demais  
❌ Usar herança só para reutilizar código  
❌ Acessar atributos sem controle  
❌ Ignorar encapsulamento

✅ Prefira hierarquias simples.

---

## 🧭 Checklist de Conclusão

Antes de avançar:

```Markdown
- [ ] Sei o que é herança
- [ ] Sei usar extends
- [ ] Sei diferenciar classe pai e filha
- [ ] Sei quando usar herança
- [ ] Resolvi o mini desafio

```

---

## ✅ Conclusão

Agora você sabe **reutilizar e especializar comportamentos** ✅  
O próximo passo é aprender a **alterar comportamentos herdados**.

➡️ Próximo arquivo: [[04-Polimorfismo]]

---

## 📝 Anotações Pessoais

Espaço livre para suas observações:
```Markdown

```
