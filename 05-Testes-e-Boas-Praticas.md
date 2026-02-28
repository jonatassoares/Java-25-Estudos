# Testes e Boas Práticas

> Fase 5 — Qualidade de Código
> Aqui você aprende a **confiar no seu código** e a **facilitar a manutenção**.
> Código que não é testado é código frágil.

---
## 🎯 Objetivo deste arquivo

Ao finalizar este material, você deve ser capaz de:
- Entender por que testes são importantes
- Criar testes unitários com JUnit 5
- Escrever código mais limpo
- Aplicar princípios básicos de boas práticas
- Pensar em manutenção e evolução do sistema

✅ **Código bom funciona hoje. Código testado funciona amanhã.**

---

# 🔹 PARTE 1 — Testes Unitários

## 🧠 O que é um Teste Unitário?

  
Um teste unitário:
> Testa **uma pequena parte do código** (unidade) de forma isolada.


Objetivos:
- Garantir funcionamento
- Evitar regressões
- Documentar comportamento

---

## ✅ Por que testar?

Sem testes ❌:
- Medo de alterar código
- Bugs reaparecem
- Difícil evoluir

Com testes ✅:
- Confiança
- Código mais limpo
- Refatoração segura  

---
## 🧪 JUnit 5 — Introdução

JUnit é o framework padrão de testes em Java.

Exemplo básico:

  

```Java
import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

class CalculadoraTest {

    @Test
    void somaDeveRetornarValorCorreto() {
        int resultado = Calculadora.somar(2, 3);
        assertEquals(5, resultado);
    }
}
```
✅ Teste claro  
✅ Fácil de entender

---
## 🧱 Estrutura de um Teste

```Java
@Test
void nomeDoTeste() {
	// preparação
	// execução
	// verificação
}  

```

📌 Esse padrão é conhecido como **AAA**:
- Arrange
- Act
- Assert

---

## ✅ Principais Asserts

```Java
assertEquals(esperado, atual);
assertTrue(condicao);
assertFalse(condicao);
assertNotNull(objeto);
assertThrows(Exception.class, () -> metodo());
```

---
## ⚠️ Erros Comuns com Testes

❌ Testar tudo no `main`  
❌ Testes dependentes entre si  
❌ Testes confusos  
❌ Não rodar testes regularmente

✅ Testes devem ser **simples e rápidos**.

---

## 🧪 Experimentos Obrigatórios (Testes)

Faça **todos digitando**:

1️⃣ Crie uma classe `Calculadora`  
2️⃣ Crie métodos de soma e subtração  
3️⃣ Crie testes unitários para cada método  
4️⃣ Force um erro e veja o teste falhar

Anote abaixo:

```Markdown
## ⚠️ Erros que aconteceram
- 
- 

## ✅ O que aprendi com esses erros
- 
```

---
# 🔹 PARTE 2 — Boas Práticas

## 🧠 Clean Code (Código Limpo)

Código limpo é:
> Código fácil de **ler**, **entender** e **manter**.

---
## ✅ Boas Práticas Essenciais

### 🔹 Nomes claros

❌ `x`, `tmp`, `teste`  
✅ `totalPedido`, `idadeCliente`

---
### 🔹 Métodos pequenos

- Um método → uma responsabilidade
- Evite métodos longos

---
### 🔹 Evite duplicação

> Código duplicado = bug duplicado

Use métodos, herança ou composição.

---
### 🔹 Comentários com moderação

❌ Comentários explicando código confuso  
✅ Código claro que se explica sozinho

---
## 🧠 Introdução ao SOLID (Visão Geral)

### ✅ S — Single Responsibility

Uma classe deve ter **uma única responsabilidade**.

---
### ✅ O — Open/Closed

Aberta para extensão  
Fechada para modificação

---
### ✅ L — Liskov Substitution

Subclasses devem funcionar como a classe pai.

---
### ✅ I — Interface Segregation

Interfaces pequenas e específicas.

---
### ✅ D — Dependency Inversion

Dependa de abstrações, não de implementações.

📌 Não decore agora — **entenda aos poucos**.

---
## ⚠️ Armadilhas Comuns

❌ Overengineering  
❌ Criar abstrações sem necessidade  
❌ Ignorar testes  
❌ Misturar responsabilidades

✅ Simplicidade é uma virtude.

---
## 🧪 Mini Desafio Final

Pegue um código antigo seu e:
- Escreva testes
- Renomeie variáveis
- Quebre métodos grandes
- Remova duplicações

✅ Sem mudar comportamento  
✅ Apenas melhorar qualidade

---

## 🧭 Checklist de Conclusão

Antes de avançar:

```Markdown
- [ ] Sei escrever testes unitários
- [ ] Sei usar asserts
- [ ] Sei melhorar legibilidade do código
- [ ] Entendo a importância de boas práticas
- [ ] Refatorei um código real
```

---
## ✅ Conclusão da Fase 5

🎉 Parabéns!  
Você agora escreve código **mais confiável, limpo e profissional**.

➡️ Próxima fase: 📁 **06-Spring-Boot** - [[01-Introducao-Spring]], [[02-API-REST]], [[03-JPA-e-Banco]] e o [[Projeto-Final]]

---

## 📝 Anotações Pessoais

Use este espaço para registrar aprendizados e reflexões:
```Markdown

```
