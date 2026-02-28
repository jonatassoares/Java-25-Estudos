# Expressões Lambda

> Fase 3 — Java Moderno 
> Aqui você aprende a **escrever menos código e expressar melhor a intenção**. 
> Lambdas são essenciais para Streams, APIs modernas e código limpo.


---

## 🎯 Objetivo deste arquivo
  

Ao finalizar este material, você deve ser capaz de:
- Entender o que é uma expressão lambda
- Substituir classes anônimas por lambdas
- Ler e escrever lambdas com segurança
- Entender a relação entre lambdas e interfaces funcionais

✅ **Lambda não é mágica — é apenas sintaxe mais simples.**

  

---

  

## 🧠 O que é uma Expressão Lambda?

  

Uma expressão lambda é:

> Uma **forma curta de escrever uma função**, normalmente passada como parâmetro.

  

Ela representa:
- Um comportamento
- Uma ação
- Um bloco de código executável
  

---

  

## 🔙 Antes das Lambdas (Código Verboso)

  

```Java
List<String> nomes = List.of("Ana", "Carlos", "Bruno");

Collections.sort(nomes, new Comparator<String>() {

    @Override
    public int compare(String a, String b) {
        return a.compareTo(b);
    }
});
```
❌ Muito código  
❌ Difícil de ler

---

## ✅ Com Lambda (Java Moderno)

```Java
nomes.sort((a, b) -> a.compareTo(b));
```
✅ Mais curto  
✅ Mais claro  
✅ Mesma lógica

---

## 🧱 Estrutura de uma Lambda

```Java
(parametros) -> { corpo }  
```

Exemplos:

```Java
() -> System.out.println("Olá")

x -> x * 2

(a, b) -> a + b
```
📌 Se houver **uma única linha**, `{}` e `return` são opcionais.

---

## 🧩 Interfaces Funcionais

Lambdas **sempre trabalham com interfaces funcionais**.

Interface funcional:

> Interface com **apenas um método abstrato**.

Exemplo:

```Java
@FunctionalInterface  
public interface Operacao {
	int executar(int a, int b);
}
```

Uso:

```Java
Operacao soma = (a, b) -> a + b;
System.out.println(soma.executar(2, 3));
```

---

## 🧠 @FunctionalInterface

```Java
@FunctionalInterface
```
✅ Garante que a interface terá **apenas um método abstrato**  
✅ Evita erros futuros

---

## 🔁 Lambdas com Collections

### ForEach

```Java
nomes.forEach(nome -> System.out.println(nome));
```

Ou ainda mais curto:

```Java
nomes.forEach(System.out::println);
```
📌 Isso é **method reference**.

---

## 🧠 Method Reference

Forma curta de lambda:

```Java
System.out::println
```

Equivale a:

```Java
x -> System.out.println(x)
```

---

## ⚠️ Erros Comuns de Iniciantes

❌ Achar que lambda substitui métodos  
❌ Usar lambda sem entender o tipo  
❌ Lambdas longas demais  
❌ Medo da sintaxe

✅ Se ficou confuso, escreva a versão longa primeiro.

---

## 🧪 Experimentos Obrigatórios

Faça **todos digitando**:

1️⃣ Crie uma lista de números  
2️⃣ Use `forEach` com lambda para imprimir  
3️⃣ Crie uma interface funcional simples  
4️⃣ Implemente usando lambda

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

> Lambdas deixam o código **mais declarativo**:  
> você diz **o que** quer fazer, não **como**.

---

## 🧪 Mini Desafio

Crie uma interface funcional:

```Java
int calcular(int x);
```

Implemente:

- Uma lambda que retorna o dobro
- Outra que retorna o quadrado

Use ambas no `main`.

✅ Use lambdas  
✅ Não crie classes extras

---

## 🧭 Checklist de Conclusão

Antes de avançar:

```Markdown
- [ ] Sei o que é lambda
- [ ] Sei escrever lambdas simples
- [ ] Sei usar forEach com lambda
- [ ] Entendo interface funcional
- [ ] Resolvi o mini desafio  

```

---

## ✅ Conclusão

Agora você escreve Java **mais limpo e moderno** ✅  
O próximo passo é usar lambdas em **Streams**, onde o poder aparece de verdade.

➡️ Próximo arquivo: [[03-Streams]]

---

## 📝 Anotações Pessoais

Use este espaço livremente:
```Markdown

```
