# Interfaces


> Fase 2 — Programação Orientada a Objetos (POO) 
> Aqui você aprende a **programar para contratos, não para implementações**. 
> Interfaces são fundamentais para código profissional e escalável.


---

## 🎯 Objetivo deste arquivo  

Ao finalizar este material, você deve ser capaz de:
- Entender o que é uma interface
- Criar interfaces em Java
- Implementar interfaces em classes
- Usar interfaces com polimorfismo
- Entender quando usar interface em vez de herança

✅ **Se herança é “é um”, interface é “se comporta como”.**  

---

## 🧠 O que é uma Interface?

Uma interface é:

> Um **contrato** que define **o que uma classe deve fazer**, mas não **como**.

  

Ela define:

- Métodos (assinaturas)

- Comportamentos esperados

  

📌 Interface **não possui estado** (atributos mutáveis).

  

---

  

## 🧱 Criando uma Interface

  

```Java
public interface Pagamento {
    void pagar(double valor);
}
```
📌 Métodos em interfaces são `public` por padrão.

---

## 🧩 Implementando uma Interface

```Java
public class PagamentoCartao implements Pagamento {

	@Override
	public void pagar(double valor) {
		System.out.println("Pagamento com cartão: " + valor);
	}
	
}
```

Outra implementação:

```Java
public class PagamentoPix implements Pagamento {

	@Override
	public void pagar(double valor) {
		System.out.println("Pagamento via PIX: " + valor);
	}
}
```
✅ Mesma interface  
✅ Implementações diferentes

---

## ▶️ Interface + Polimorfismo

```Java
Pagamento pagamento1 = new PagamentoCartao();
Pagamento pagamento2 = new PagamentoPix();

pagamento1.pagar(100);  
pagamento2.pagar(50);
```
📌 O código **não sabe** qual é a implementação concreta — e isso é ótimo.

---

## 🧠 Por que Interfaces são importantes?

Sem interfaces ❌:

- Código acoplado
- Difícil de mudar
- Muitos `if / else`

Com interfaces ✅:

- Código flexível
- Fácil de estender
- Testável
- Profissional

---

## 🔄 Interface x Herança

|Herança|Interface|
|---|---|
|`extends`|`implements`|
|Reutiliza código|Define contrato|
|Classe única|Múltiplas interfaces|
|“É um”|“Se comporta como”|

📌 Uma classe pode:

- Herdar **uma** classe
- Implementar **várias** interfaces

---

## 🧠 Interface com Métodos Default

```Java
public interface Notificavel {
	default void notificar() {
		System.out.println("Notificação padrão");
	}
}
```
📌 Útil para evolução de interfaces sem quebrar código antigo.

---

## ⚠️ Erros Comuns de Iniciantes

❌ Usar interface como classe  
❌ Colocar lógica complexa em interface  
❌ Criar interfaces genéricas demais  
❌ Confundir interface com herança

✅ Interface define **o que**, classe define **como**.

---

## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:

1️⃣ Crie uma interface `Imprimivel`

```Java
void imprimir();
```

2️⃣ Crie classes:

- `Relatorio`
- `Contrato`

3️⃣ Implemente `imprimir()` em cada uma  
4️⃣ Use polimorfismo para chamar o método

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

> Interfaces reduzem dependências  
> e **preparam o código para o futuro**.

---

## 🧪 Mini Desafio

Crie:

- Interface `Autenticavel`
    - método `autenticar(String senha)`
- Classes:
    - `Usuario`
    - `Administrador`

Cada uma valida a senha de forma diferente.

Depois:

```Java
Autenticavel a = new Usuario();
a.autenticar("1234");
```

✅ Use interface  
✅ Nenhum `if` no código cliente

---

## 🧭 Checklist de Conclusão

Antes de avançar:

```Markdown
- [ ] Sei o que é interface
- [ ] Sei criar interfaces
- [ ] Sei implementar interfaces
- [ ] Sei usar interfaces com polimorfismo
- [ ] Resolvi o mini desafio

```

---

## ✅ Conclusão da Fase 2

🎉 **Parabéns!**  
Você agora domina os **4 pilares da POO**:

- Classes e Objetos
- Encapsulamento
- Herança
- Polimorfismo
- Interfaces

➡️ Próximo passo recomendado: 📁 [[Projeto-POO.md]] (integra tudo em um projeto prático)

---

## 📝 Anotações Pessoais

Use este espaço livremente:
```Markdown

```
