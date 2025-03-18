## 📌 **1. Introdução ao Java**

- O que é Java? (história e propósito)
- Características principais (portabilidade, orientação a objetos, tipagem forte, etc.)
- Instalação e configuração (JDK, JRE, JVM)
## 🏛 O que é Java?

Java é uma linguagem de programação **orientada a objetos**, **portável** e **segura**, criada pela Sun Microsystems em 1995 e atualmente mantida pela Oracle. Ela é amplamente utilizada para desenvolvimento de aplicações desktop, web, mobile e sistemas embarcados.

### 🎯 **Principais características do Java:**

✅ **Plataforma independente** → O código Java é compilado para **bytecode**, executado na **Java Virtual Machine (JVM)**, permitindo rodar em qualquer sistema operacional com JVM instalada.  
✅ **Linguagem orientada a objetos** → Utiliza conceitos como classes, objetos, encapsulamento, herança e polimorfismo.  
✅ **Gerenciamento automático de memória** → O **Garbage Collector (GC)** remove objetos não utilizados da memória.  
✅ **Multithreading** → Permite a execução de múltiplas tarefas simultaneamente.  
✅ **Segurança** → Proteção contra execução de códigos maliciosos dentro da JVM.

---

## 🔧 Instalação e Configuração

### 🔹 **Passo 1 - Baixar o JDK**

O **Java Development Kit (JDK)** contém tudo o que é necessário para desenvolver e executar aplicações Java.

📥 Faça o download do JDK mais recente no site oficial da Oracle ou utilize versões open-source como OpenJDK:  
🔗 [https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)

### 🔹 **Passo 2 - Configurar as variáveis de ambiente** (Windows)

Após instalar o JDK, configure a variável de ambiente `JAVA_HOME`:  
1️⃣ Abra o **Painel de Controle** → **Sistema** → **Configurações Avançadas do Sistema**  
2️⃣ Clique em **Variáveis de Ambiente**  
3️⃣ Em **Variáveis do Sistema**, clique em **Novo** e adicione:

- Nome: `JAVA_HOME`
- Valor: `C:\Program Files\Java\jdk-XX` (substitua `XX` pela versão instalada)  
    4️⃣ No campo **Path**, adicione:


`%JAVA_HOME%\bin`

5️⃣ Teste a instalação abrindo o terminal (CMD ou PowerShell) e digitando:


`java -version`

Se tudo estiver certo, aparecerá a versão instalada do Java.

---

## ⚙️ Componentes do Java

O Java é composto por três partes principais:

### 📦 1️⃣ JDK (Java Development Kit)

- Pacote necessário para **desenvolver** aplicações Java.
- Contém o **compilador (javac)**, a JVM e várias bibliotecas essenciais.

### 🎭 2️⃣ JRE (Java Runtime Environment)

- Ambiente que permite **executar** aplicações Java, mas **não inclui** o compilador.
- Contém apenas a JVM e as bibliotecas necessárias para rodar código Java.

### 🚀 3️⃣ JVM (Java Virtual Machine)

- Responsável por executar o **bytecode** gerado pelo compilador Java.
- Cada sistema operacional tem sua implementação específica da JVM.

📌 **Fluxo de execução de um programa Java:**

1. O código fonte (`.java`) é escrito pelo programador.
2. O compilador (`javac`) transforma esse código em **bytecode (`.class`)**.
3. A JVM interpreta e executa esse bytecode.

mermaid

CopiarEditar

`graph TD;     A[Código Fonte .java] -->|Compilação (javac)| B[Bytecode .class];     B -->|Execução (JVM)| C[Programa em execução];`

---

## 📌 **2. Fundamentos da Linguagem**

- Sintaxe básica
- Tipos de dados primitivos (int, double, boolean, etc.)
- Operadores (aritméticos, relacionais, lógicos, etc.)
- Estruturas de controle (if, else, switch, loops)
- Entrada e saída de dados (`Scanner`, `System.out.println`)

# 📌 **2.1 Sintaxe Básica no Java**

O Java é uma linguagem **fortemente tipada**, o que significa que todas as variáveis precisam ter um tipo definido antes de serem usadas. Além disso, todo programa Java segue uma estrutura específica.

## 🔹 **Estrutura de um Programa Java**

Um programa Java básico contém os seguintes elementos:

- **Declaração do pacote** _(opcional)_
    
- **Importação de bibliotecas** _(opcional)_
    
- **Definição de uma classe**
    
- **Método `main`** _(ponto de entrada do programa)_
    
- **Instruções dentro do `main`** _(código executável)_
    

### ✅ **Exemplo de um programa Java completo**

![[Pasted image 20250318155020.png]]

## 🔹 **Explicação da Estrutura**

### ✅ **1. Declaração do pacote (opcional)**

`package meu.pacote;`

- Se o código fizer parte de um pacote específico, ele deve ser declarado na primeira linha.
    
- Se o programa não usar pacotes personalizados, essa linha pode ser omitida.
    

### ✅ **2. Importação de bibliotecas (opcional)**

`import java.util.Scanner;`

- Importamos classes de outras bibliotecas para uso no programa.
    
- No exemplo, importamos `Scanner` para ler dados do teclado.
    

### ✅ **3. Definição da classe**

`public class MeuPrograma {`

- Todo código Java precisa estar dentro de uma **classe**.
    
- O nome da classe deve ser o mesmo nome do arquivo `.java`.
    

### ✅ **4. Método `main` (ponto de entrada)**

`public static void main(String[] args) {`

- Esse é o **método principal** do programa, onde a execução começa.
    
- **Explicação de cada palavra-chave:**
    
    - `public` → Pode ser acessado de qualquer lugar.
        
    - `static` → Pertence à classe e pode ser chamado sem criar um objeto.
        
    - `void` → Não retorna nenhum valor.
        
    - `String[] args` → Parâmetros do programa (opcional).
        

### ✅ **5. Instruções dentro do `main`**

`System.out.println("Olá, Mundo!");`

- `System.out.println()` exibe uma mensagem no console.
    

`Scanner scanner = new Scanner(System.in); String nome = scanner.nextLine();`

- Criamos um objeto `Scanner` para ler entrada do usuário.
    

`scanner.close();`

- Sempre fechamos o `Scanner` após o uso para evitar vazamento de recursos.
    

## 🎯 **Resumo**

| Elemento                                 | Descrição                                                |
| ---------------------------------------- | -------------------------------------------------------- |
| `package`                                | Define o pacote do código (opcional).                    |
| `import`                                 | Importa classes de outras bibliotecas (opcional).        |
| `class`                                  | Declara uma classe, que é o bloco principal do programa. |
| `public static void main(String[] args)` | Método principal do programa.                            |
| `System.out.println()`                   | Exibe mensagens no console.                              |
| `Scanner`                                | Permite entrada de dados do usuário.                     |

---

# 📌 **Entrada e Saída de Dados em Java**

Em Java, a entrada e saída de dados podem ser feitas de várias formas, dependendo do contexto. Aqui, veremos os métodos mais comuns para **entrada de dados (input)** e **saída de dados (output)**.

---

## 🔹 **1. Saída de Dados (`System.out`)**

Para exibir informações no console, utilizamos a classe `System.out`.

### ✅ **`System.out.print()`**

Exibe um texto no console, **sem** quebra de linha.

![[Pasted image 20250318155523.png]]
🔹 **Saída:**

![[Pasted image 20250318155547.png]]

### ✅ **`System.out.println()`**

Exibe um texto no console **com** quebra de linha.

![[Pasted image 20250318155609.png]]
🔹 **Saída:**

![[Pasted image 20250318155623.png]]

### ✅ **`System.out.printf()`**

Permite formatar a saída de dados.

![[Pasted image 20250318155653.png]]

📌 **Explicação:**

- `%.2f` → Formata um número decimal com 2 casas decimais.
    
- `%n` → Representa uma nova linha (substitui `\n`).

## 🔹 **2. Entrada de Dados com `Scanner`**

A classe `Scanner` permite ler diferentes tipos de entrada do teclado.

### ✅ **Passo 1: Importar `Scanner`**

Antes de usar o `Scanner`, devemos importá-lo:

![[Pasted image 20250318155739.png]]

✅ **Criando um Objeto `Scanner`**

![[Pasted image 20250318155757.png]]

✅ **Lendo Diferentes Tipos de Dados**

![[Pasted image 20250318155814.png]]
🔹 **Saída (exemplo de entrada do usuário):**

![[Pasted image 20250318155828.png]]

### ✅ **Principais Métodos do `Scanner`**

|Método|Tipo de Dado|Exemplo|
|---|---|---|
|`next()`|String (uma palavra)|`String nome = scanner.next();`|
|`nextLine()`|String (linha inteira)|`String frase = scanner.nextLine();`|
|`nextInt()`|Número inteiro|`int idade = scanner.nextInt();`|
|`nextDouble()`|Número decimal|`double altura = scanner.nextDouble();`|
|`nextBoolean()`|Booleano (`true/false`)|`boolean ativo = scanner.nextBoolean();`|

📌 **Observação importante:**  
Depois de usar `nextInt()`, `nextDouble()`, etc., sempre use `scanner.nextLine()` para consumir a quebra de linha pendente, evitando erros.

## 🎯 **Conclusão**

| Método                 | Tipo          | Uso                                              |
| ---------------------- | ------------- | ------------------------------------------------ |
| `System.out.print()`   | Saída         | Exibe texto **sem** quebra de linha.             |
| `System.out.println()` | Saída         | Exibe texto **com** quebra de linha.             |
| `System.out.printf()`  | Saída         | Exibe texto formatado.                           |
| `Scanner`              | Entrada       | Lê dados do teclado (int, double, String, etc.). |
| `BufferedReader`       | Entrada       | Lê dados mais rápido (precisa de conversão).     |
| `JOptionPane`          | Entrada/Saída | Usa janelas gráficas para entrada e saída.       |
| `PrintWriter`          | Saída         | Grava texto em arquivos.                         |

---

## 🔢 **Tipos de Dados Primitivos**

O Java possui **8 tipos primitivos**, que são os blocos fundamentais para armazenar valores:

|Tipo|Tamanho|Valor Padrão|Exemplo|
|---|---|---|---|
|`byte`|8 bits|0|`byte idade = 25;`|
|`short`|16 bits|0|`short ano = 2024;`|
|`int`|32 bits|0|`int numero = 1000;`|
|`long`|64 bits|0L|`long populacao = 7800000000L;`|
|`float`|32 bits|0.0f|`float preco = 3.99f;`|
|`double`|64 bits|0.0d|`double altura = 1.75;`|
|`char`|16 bits|`'\u0000'`|`char letra = 'A';`|
|`boolean`|1 bit|`false`|`boolean ativo = true;`|

📌 **Observações:**

- `char` representa **um único caractere** e usa aspas simples (`'A'`).
- `boolean` pode armazenar apenas `true` ou `false`.
- `float` e `double` armazenam números decimais, mas `float` exige um **"f"** no final (`3.14f`).

---

## ➗ **2.3 Operadores**

Os operadores em Java são usados para realizar operações matemáticas, comparações e lógica.

### 🔹 **Operadores Aritméticos**

|Operador|Descrição|Exemplo (`a = 10, b = 5`)|Resultado|
|---|---|---|---|
|`+`|Adição|`a + b`|`15`|
|`-`|Subtração|`a - b`|`5`|
|`*`|Multiplicação|`a * b`|`50`|
|`/`|Divisão|`a / b`|`2`|
|`%`|Módulo (resto)|`a % b`|`0`|

### 🔹 **Operadores Relacionais**

|Operador|Descrição|Exemplo (`a = 10, b = 5`)|Resultado|
|---|---|---|---|
|`==`|Igual|`a == b`|`false`|
|`!=`|Diferente|`a != b`|`true`|
|`>`|Maior que|`a > b`|`true`|
|`<`|Menor que|`a < b`|`false`|
|`>=`|Maior ou igual|`a >= b`|`true`|
|`<=`|Menor ou igual|`a <= b`|`false`|

### 🔹 **Operadores Lógicos**

|Operador|Descrição|Exemplo (`a = true, b = false`)|Resultado|
|---|---|---|---|
|`&&`|AND (E)|`a && b`|`false`|
|`||`|OR (OU)|
|`!`|NOT (Negação)|`!a`|`false`|

---

# 📌 **Estruturas Condicionais em Java**

Estruturas condicionais permitem que o programa tome decisões e execute diferentes blocos de código com base em certas condições.

## 🔹 **1. `if`, `else if`, `else`**

A estrutura `if-else` é usada para executar código condicionalmente, com base em uma expressão booleana (`true` ou `false`).

### 📝 **Sintaxe:**

![[Pasted image 20250318150533.png]]

### ✅ **Exemplo prático:**

![[Pasted image 20250318150556.png]]

🔹 **Explicação:**

- Se `idade` for menor que 18, a primeira condição será executada.
    
- Se `idade` for exatamente 18, a segunda condição será executada.
    
- Caso contrário, o bloco `else` será executado.

## 🔹 **2. Operador Ternário (`? :`)**

O operador ternário é uma forma reduzida do `if-else`, útil para atribuições rápidas.

### 📝 **Sintaxe:**

![[Pasted image 20250318150622.png]]

✅ **Exemplo prático:**

![[Pasted image 20250318150638.png]]

🔹 **Explicação:**  
Se `idade` for maior ou igual a 18, `status` recebe `"Maior de idade"`, caso contrário, recebe `"Menor de idade"`.


## 🔹 **3. `switch-case`**

O `switch-case` é útil quando há múltiplas opções e queremos evitar vários `if-else`.

### 📝 **Sintaxe:**

![[Pasted image 20250318150706.png]]

✅ **Exemplo prático:**

![[Pasted image 20250318150722.png]]

🔹 **Explicação:**

- O programa verifica `dia` e imprime o dia correspondente.
    
- O `break` impede que os próximos `case` sejam executados.
    
- Se `dia` não corresponder a nenhum `case`, o `default` será executado.

📌 **Atenção:**

- Desde o Java 14, o `switch` pode ser usado de forma mais compacta com `->`:

![[Pasted image 20250318150744.png]]

## 🔹 **4. Comparação de Strings em Condições**

No Java, Strings devem ser comparadas usando `.equals()`, pois `==` verifica a referência de memória e não o conteúdo.

### ✅ **Exemplo prático:**

![[Pasted image 20250318150802.png]]

🔹 **Explicação:**  
O método `.equals()` verifica se o conteúdo da `String` é igual a `"Java"`.

📌 **Cuidado com a comparação errada!**

![[Pasted image 20250318150815.png]]

## 🔹 **5. Operadores Relacionais e Lógicos**

Podemos usar operadores relacionais e lógicos em condições.

### 📝 **Operadores Relacionais:**

| Operador | Significado    |
| -------- | -------------- |
| `==`     | Igualdade      |
| `!=`     | Diferente      |
| `>`      | Maior que      |
| `<`      | Menor que      |
| `>=`     | Maior ou igual |
| `<=`     | Menor ou igual |

### 📝 **Operadores Lógicos:**

| Operador | Significado                                             |
| -------- | ------------------------------------------------------- |
| `&&`     | E lógico (true se ambas as condições forem verdadeiras) |
| `        |                                                         |
| `!`      | NÃO lógico (inverte o valor booleano)                   |

✅ **Exemplo prático:**

![[Pasted image 20250318150955.png]]

🔹 **Explicação:**

- O código só executará `"Pode dirigir."` se ambas as condições forem verdadeiras.

## 🔹 **6. Comparação de Objetos (`equals` e `==`)**

Quando usamos `==`, estamos comparando referências de objetos, não os valores dentro deles.

### ✅ **Exemplo prático:**

![[Pasted image 20250318151021.png]]

🔹 **Explicação:**

- `==` verifica se `nome1` e `nome2` apontam para o mesmo objeto na memória (falso).
    
- `.equals()` verifica se o conteúdo das Strings é igual (verdadeiro).

# 🎯 **Conclusão**

- Use `if-else` para verificações simples.
    
- Prefira `switch` quando há muitas comparações com valores fixos.
    
- Use operadores lógicos (`&&`, `||`, `!`) para combinar condições.
    
- Compare Strings sempre com `.equals()`.
    
- Use `==` para comparar referências e `.equals()` para comparar valores.

---

# 📌 **Laços de Repetição em Java (`for`, `while`, `do-while`)**

Os laços de repetição são usados para executar um bloco de código várias vezes enquanto uma condição for verdadeira.

---

## 🔹 **1. `for` (Laço com Controle)**

O `for` é utilizado quando sabemos **quantas vezes** um bloco de código precisa ser executado.

### 📝 **Sintaxe:**

![[Pasted image 20250318151146.png]]

- **Inicialização:** Define uma variável de controle (executado apenas uma vez).
    
- **Condição:** Mantém o loop ativo enquanto for `true`.
    
- **Incremento:** Atualiza a variável de controle a cada repetição.

✅ **Exemplo 1 – Contagem de 1 a 5:**

![[Pasted image 20250318152048.png]]

🔹 **Saída:**

![[Pasted image 20250318152114.png]]

![[Pasted image 20250318152720.png]]

![[Pasted image 20250318152730.png]]

## 🔹 **2. `for-each` (Loop Melhorado)**

Usado para percorrer coleções (arrays, listas) de maneira simplificada.

### ✅ **Exemplo – Percorrendo um Array**

![[Pasted image 20250318152744.png]]

🔹 **Saída:**

![[Pasted image 20250318152758.png]]

📌 **Vantagens:**

- Código mais limpo e fácil de entender.
    
- Evita erros ao acessar índices.
    

📌 **Limitação:**

- Não pode modificar os valores do array diretamente.

## 🔹 **3. `while` (Laço de Repetição Condicional)**

O `while` é útil quando **não sabemos** exatamente quantas vezes o código será executado.

### 📝 **Sintaxe:**

![[Pasted image 20250318153213.png]]

✅ **Exemplo – Contagem regressiva**

![[Pasted image 20250318153229.png]]

🔹 **Saída:**

![[Pasted image 20250318153253.png]]

✅ **Exemplo – Entrada de Usuário (Simulação)**

![[Pasted image 20250318153308.png]]

📌 **Explicação:**

- O loop continua até que o usuário digite `"sair"`.
    
- O `scanner.nextLine()` lê a entrada do usuário.

## 🔹 **4. `do-while` (Executa Pelo Menos Uma Vez)**

O `do-while` funciona como o `while`, mas **garante** que o código será executado ao menos uma vez.

### 📝 **Sintaxe:**

![[Pasted image 20250318153337.png]]

### ✅ **Exemplo – Solicitação de Senha**

![[Pasted image 20250318153357.png]]

📌 **Explicação:**

- O usuário será solicitado a digitar a senha pelo menos **uma vez**.
    
- O loop **só para** quando a senha correta for inserida.
    

🔹 **Diferença entre `while` e `do-while`:**

| `while`                                          | `do-while`                                                        |
| ------------------------------------------------ | ----------------------------------------------------------------- |
| Testa a condição **antes** de executar o código. | Executa o código pelo menos **uma vez**, depois testa a condição. |

## 🔹 **5. Controle de Fluxo em Laços (`break` e `continue`)**

### ✅ **`break` (Interrompe o Loop)**

Usado para sair imediatamente do laço.

![[Pasted image 20250318153429.png]]

🔹 **Saída:**

![[Pasted image 20250318153450.png]]

### ✅ **`continue` (Pula uma Iteração)**

Usado para **ignorar** uma iteração e continuar o loop.

![[Pasted image 20250318153526.png]]

**Saída:**

![[Pasted image 20250318153540.png]]

## 🎯 **Conclusão**

| Laço       | Quando Usar                                               |
| ---------- | --------------------------------------------------------- |
| `for`      | Quando o número de repetições é conhecido.                |
| `for-each` | Para percorrer arrays e coleções de forma simples.        |
| `while`    | Quando não sabemos quantas repetições ocorrerão.          |
| `do-while` | Quando queremos executar o código **pelo menos uma vez**. |
| `break`    | Para sair de um loop antes da condição normal.            |
| `continue` | Para pular uma iteração e continuar o loop.               |

---

## 📌 **3. Programação Orientada a Objetos (POO) em Java**

- Classes e objetos
- Construtores
- Modificadores de acesso (`public`, `private`, `protected`)
- Encapsulamento
- Herança
- Polimorfismo
- Classes abstratas e interfaces


## **O que é `public` em Java?**

A palavra `public` em Java **define quem pode acessar** algo (como uma classe ou um método).  
Se algo é **public**, ele pode ser acessado de **qualquer lugar** do código.

Exemplo:
![[Pasted image 20250318111829.png]]

Isso significa que **outras classes podem acessar `nome` diretamente**.

Se fosse `private`, **ninguém fora da classe poderia acessar**:

![[Pasted image 20250318111852.png]]

## **O que é uma Classe em Java?**

Pensa na classe como um **molde** para criar objetos.  
Ela define **como algo deve ser e o que ele pode fazer**.

Exemplo de classe `Carro`:

![[Pasted image 20250318111914.png]]

Aqui, `Carro` é um **molde**. Ele ainda não faz nada sozinho.  
Precisamos **criar um objeto** baseado nesse molde.

Exemplo de uma classe em Java, a entidade nesse caso é um triângulo com 3 atributos e 1 método para calcular a área do triângulo:

![[Pasted image 20250318130711.png]]

## **1. Diagrama de Classes**

Um **diagrama de classes** representa as classes de um sistema, seus atributos, métodos e como elas se relacionam.

### **Exemplo: Representação UML de uma Classe**

Uma classe em UML é representada assim:

![[Pasted image 20250318131955.png]]

![[Pasted image 20250318132008.png]]

## **2. Relações entre Classes**

No diagrama UML, podemos mostrar como as classes se relacionam.  
As relações mais comuns são:

### **1️⃣ Associação (↔)**

Quando uma classe usa outra **sem ser dona dela**.

**Exemplo:**

![[Pasted image 20250318132142.png]]

Isso significa que **uma Pessoa tem um Endereço**.

**Código Java**:

![[Pasted image 20250318132206.png]]

### **2️ Herança (↥)**

Quando uma classe **herda** outra.

**Exemplo UML:**

![[Pasted image 20250318132250.png]]

Isso significa que `Carro` **herda** de `Veiculo`.

**Código Java**:

![[Pasted image 20250318132306.png]]

### **Classe Object**

Toda classe em Java é uma subclasse da classe Object

Object possui os seguintes métodos
* getClass - retorna o tipo do objeto
* equals - compara se o objeto é igual a outro
* hashCode - retorna um código hash do objeto
* toString - converte o objeto para string

## **O que é Instanciar um Objeto?**

**Criar um objeto** significa "dar vida" à classe, transformando-a em algo real.  
Isso se chama **instanciar** a classe.

Ao instanciar um objeto, a memória é alocada em uma parte da memória chamada heap.

![[Pasted image 20250318111942.png]]

### **Explicação Simples**

1. **Criamos a classe `Carro`** (o molde).
    
2. **Criamos um objeto `meuCarro`** baseado nesse molde.
    
3. **Definimos os valores do carro (`marca` e `modelo`)**.
    
4. **Chamamos o método `exibirInfo()`** para mostrar os dados do carro.


## **O que são parâmetros?**

Parâmetros são **valores que passamos para métodos ou construtores** para que possam processar informações.  
Eles funcionam como **variáveis temporárias** que recebem um valor quando o método ou o construtor é chamado.

Exemplo básico de **método com parâmetro**:

![[Pasted image 20250318130023.png]]

Quando chamamos `apresentar("João");`, o método recebe `"João"` como parâmetro e exibe:
Olá, meu nome é João


## **O que é um Método em Java?**

Um método é como uma **função**, ou seja, **um bloco de código que executa algo**.

### **Exemplo de método sem retorno (`void`)**

![[Pasted image 20250318114918.png]]

Esse método **apenas imprime um texto**, mas **não retorna nenhum valor**.

### **Exemplo de método com retorno (`return`)**

![[Pasted image 20250318114954.png]]


### **O que é `this` em Java?**

A palavra-chave **`this`** em Java é usada dentro de uma classe para **se referir ao próprio objeto** da classe.

Ela é útil quando precisamos diferenciar atributos de variáveis locais, chamar métodos da própria classe ou até passar o objeto atual como argumento.

## **1️ `this` para Diferenciar Atributos e Parâmetros**

Quando um parâmetro tem o mesmo nome de um atributo da classe, **`this` é usado para referenciar o atributo do objeto**.

### **Exemplo Sem `this` (Dá Erro!)**

![[Pasted image 20250318140503.png]]

Aqui, Java entende que o `nome = nome;` está apenas atribuindo o valor do parâmetro `nome` a ele mesmo, sem modificar o atributo da classe.

Exemplo Usando `this` (Correto ✅)

![[Pasted image 20250318140534.png]]

🔹 **`this.nome = nome;`** → O `this` indica que estamos falando do **atributo da classe** e não do parâmetro recebido pelo método.

## **2️ `this` para Chamar Outro Construtor**

Podemos usar `this()` para chamar um **outro construtor** dentro da mesma classe.

### **Exemplo**

![[Pasted image 20250318140623.png]]

🔹 O **segundo construtor** chama o primeiro usando `this(marca, "Modelo Padrão")`, evitando repetição de código.

## **3️ `this` para Chamar Métodos da Própria Classe**

Também podemos usar `this` para chamar um método dentro da própria classe.

![[Pasted image 20250318140713.png]]

Saída

![[Pasted image 20250318140746.png]]

🔹 Aqui, `this.comer();` chama o próprio método `comer()` antes de executar `dormir()`.

## **4️ `this` para Passar o Objeto Atual como Argumento**

Podemos usar `this` para passar o **próprio objeto da classe** como argumento para outro método ou classe.

### **Exemplo**

![[Pasted image 20250318140824.png]]

🔹 **`this` aqui representa o objeto `Jogador` atual**, que está sendo passado para o método `exibir()`.

## **Resumo**

|Uso do `this`|Explicação|
|---|---|
|**Diferenciar atributos e parâmetros**|`this.atributo = parâmetro;`|
|**Chamar outro construtor**|`this();` chama outro construtor na mesma classe|
|**Chamar método da própria classe**|`this.metodo();` evita repetição de código|
|**Passar o próprio objeto como argumento**|`outroMetodo(this);`|


---

## 📌 **4. Manipulação de Coleções e Arrays**

- Arrays (`int[]`, `String[]`)
- `ArrayList`, `LinkedList`
- `HashMap`, `HashSet`, `TreeMap`

### **O que são operações bitwise?**

As operações **bitwise** trabalham diretamente nos **bits** de um número inteiro, manipulando-os individualmente. Essas operações são úteis para otimizações, manipulação de bits e certas operações matemáticas eficientes.

### **Principais Operadores Bitwise em Java**

|Operador|Nome|Descrição|
|---|---|---|
|`&`|AND bitwise|Retorna 1 se ambos os bits forem 1.|
|`|`|OR bitwise|
|`^`|XOR bitwise|Retorna 1 se os bits forem diferentes.|
|`~`|NOT bitwise|Inverte todos os bits do número.|
|`<<`|Shift à esquerda|Desloca os bits para a esquerda (multiplica por potência de 2).|
|`>>`|Shift à direita|Desloca os bits para a direita (divide por potência de 2).|
|`>>>`|Shift à direita lógico|Igual ao `>>`, mas preenche com 0 ao invés do bit de sinal.|

---

### **Exemplos Práticos em Java**

java

CopiarEditar

![[Pasted image 20250318141328.png]]


---

## 📌 **5. Tratamento de Exceções**

- `try`, `catch`, `finally`
- Criando exceções personalizadas
- `throw` e `throws`

---

## 📌 **6. Java e APIs Nativas**

- `java.time` (trabalhando com datas)
- `java.io` (leitura e escrita de arquivos)
- `java.util` (utilitários, Random, Scanner, etc.)

---

## 📌 **7. Java Avançado**

- Programação concorrente (`Thread`, `ExecutorService`)
- Expressões Lambda
- Streams API
- Anotações (`@Override`, `@Deprecated`, `@FunctionalInterface`)

---

## 📌 **8. Desenvolvimento Web com Java**

- Introdução ao Spring Boot
- Criando APIs REST
- Banco de Dados com JPA e Hibernate

---

## 📌 **9. Ferramentas e Boas Práticas**

- Uso de Maven/Gradle
- Testes unitários com JUnit
- Design Patterns em Java

---

## 📌 **10. Dicas e Truques para Iniciantes**

- Melhores práticas de código
- Depuração no IntelliJ/Eclipse
- Como organizar projetos em Java