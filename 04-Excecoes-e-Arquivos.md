# Exceções e Arquivos

> Fase 4 — Robustez e IO
> Aqui você aprende a **lidar com erros corretamente** e a **trabalhar com arquivos**. 
> Código profissional não quebra silenciosamente.

---
## 🎯 Objetivo deste arquivo

Ao finalizar este material, você deve ser capaz de:
- Entender o que são exceções
- Tratar erros com `try / catch`
- Criar exceções customizadas
- Ler e escrever arquivos
- Evitar falhas inesperadas em tempo de execução

✅ **Erro tratado é sistema confiável.**

---
# 🔹 PARTE 1 — Exceções

## 🧠 O que é uma Exceção?

Uma exceção é:
> Um **evento inesperado** que ocorre durante a execução do programa.


Exemplos:
- Divisão por zero
- Arquivo não encontrado
- Acesso inválido a dados

---
## 💥 Exemplo de Erro sem Tratamento

```Java
int x = 10 / 0;
```

Resultado:
```Plain Text
Exception in thread "main" java.lang.ArithmeticException
```
❌ Programa quebra  
❌ Nenhuma recuperação

---
## ✅ Tratando Exceções com try/catch

```Java
try {
	int x = 10 / 0;
} catch (ArithmeticException e) {
	System.out.println("Erro: divisão por zero");
}  

```
✅ Programa não quebra  
✅ Erro controlado

---
## 🔁 Estrutura Completa

```Java
try {
	// código que pode falhar
} catch (Exception e) {
	// tratamento
} finally {
	// sempre executa (opcional)
}
```
📌 `finally` é usado para liberar recursos.

---
## 🧠 Hierarquia de Exceções

```Plain Text
Throwable
├── Error  
└── Exception  
	├── RuntimeException  
	└── Checked Exceptions
```
- **RuntimeException** → erro de lógica
- **Checked** → exige tratamento explícito

---
## ⚠️ Checked x Unchecked

### Checked Exception

```Java
FileReader fr = new FileReader("arquivo.txt");
```
❌ Não compila sem tratamento

---
### Unchecked Exception

```Java
int x = 10 / 0;
```
❌ Erro só em tempo de execução

---
## 🛠️ Criando Exceção Customizada

```Java
public class SaldoInsuficienteException extends RuntimeException {
	
	public SaldoInsuficienteException(String mensagem) {
		super(mensagem);
	}
}
```

Uso:
```Java
if (saldo < valor) {
	throw new SaldoInsuficienteException("Saldo insuficiente");
}
``
```

---

## ⚠️ Erros Comuns com Exceções
❌ Capturar `Exception` genérico  
❌ Ignorar exceção  
❌ Usar exceção para controle de fluxo  
❌ Não logar erro

✅ Exceção é para **situação excepcional**.

---

## 🧪 Experimentos Obrigatórios (Exceções)

Faça **todos digitando**:
1️⃣ Gere uma divisão por zero  
2️⃣ Trate com `try/catch`  
3️⃣ Crie uma exceção customizada  
4️⃣ Lance a exceção manualmente

Anote abaixo:
```Markdown
## ⚠️ Erros que aconteceram
- 
- 
  
## ✅ O que aprendi com esses erros
- 
```

---
# 🔹 PARTE 2 — Arquivos

## 🧠 Por que trabalhar com arquivos?

Arquivos permitem:

- Persistir dados
- Ler configurações
- Importar/exportar informações

---

## 📖 Lendo Arquivos (java.nio)

```Java
Path caminho = Path.of("dados.txt");
List<String> linhas = Files.readAllLines(caminho);  

linhas.forEach(System.out::println);
```
✅ Simples  
✅ Moderno

---
## ✍️ Escrevendo Arquivos

```Java
Path caminho = Path.of("saida.txt");
List<String> dados = List.of("Linha 1", "Linha 2");

Files.write(caminho, dados);
```
📌 Sobrescreve o arquivo por padrão.

---
## 🔐 Try-with-resources

```Java
try (BufferedReader br = Files.newBufferedReader(Path.of("dados.txt"))) {
	String linha;
	while ((linha = br.readLine()) != null) {
		System.out.println(linha);
	}
}
```

✅ Fecha recursos automaticamente  
✅ Evita vazamentos

---
## ⚠️ Erros Comuns com Arquivos
❌ Não tratar IOException  
❌ Caminho errado  
❌ Esquecer encoding  
❌ Não fechar recurso

✅ Use `java.nio` sempre que possível.

---

## 🧪 Experimentos Obrigatórios (Arquivos)

Faça **todos digitando**:
1️⃣ Crie um arquivo `.txt`  
2️⃣ Escreva dados nele  
3️⃣ Leia os dados  
4️⃣ Trate exceções corretamente

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

> Exceções protegem o sistema  
> Arquivos conectam o sistema ao mundo real

---
## 🧪 Mini Desafio Final

Crie um programa que:
- Leia um arquivo com números
- Ignore linhas inválidas
- Some apenas números válidos
- Trate todas as exceções

✅ Programa não pode quebrar  
✅ Mensagens claras de erro

---

## 🧭 Checklist de Conclusão

Antes de avançar:
```Markdown
- [ ] Sei tratar exceções
- [ ] Sei criar exceções customizadas
- [ ] Sei ler arquivos
- [ ] Sei escrever arquivos
- [ ] Resolvi o mini desafio
```

---
## ✅ Conclusão da Fase 4

🎉 Parabéns!  
Agora seu código é **mais seguro, confiável e profissional**.

➡️ Próxima fase: 📁 **[[05-Testes-e-Boas-Praticas]]**

---
## 📝 Anotações Pessoais

Use este espaço para registrar aprendizados:
```Markdown

```
