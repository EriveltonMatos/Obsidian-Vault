### 🔹 **1. Conceitos Básicos do React**

- Criando um projeto com **Vite** (`npm create vite@latest`).
- JSX (JavaScript + HTML dentro do JS).
- Componentes funcionais (`function MeuComponente() {}`).
- Props e Children.
- Estado com `useState`.

### 🔹 **2. Gerenciamento de Estados e Eventos**

- Eventos no React (`onClick`, `onChange`).
- Hook `useState` (estado local).
- Hook `useEffect` (efeitos colaterais, como chamadas de API).
- Lifting State Up (compartilhamento de estado entre componentes).
- Context API para estados globais simples.

### 🔹 **3. Trabalhando com Listas e Renderização Condicional**

- `map()` para renderizar listas.
- `key` em listas no React.
- Renderização condicional (`&&`, ternário e `if`).

### 🔹 **4. Hooks Mais Avançados**

- `useRef` (manipular elementos diretamente).
- `useMemo` e `useCallback` (performance).
- `useReducer` (estado complexo).

### 🔹 **5. Comunicação com APIs**

- Fetching de dados com `fetch` e `axios`.
- Tratamento de loading e erros.
- Renderização baseada em dados dinâmicos.

### 🔹 **6. Roteamento com React Router**

- Instalação e configuração (`react-router-dom`).
- Rotas dinâmicas (`useParams`).
- Navegação entre páginas (`useNavigate`).

### 🔹 **7. Gerenciamento de Estado Global**

Se o projeto crescer, use algo além de `useContext`:

- **Zustand** (leve e fácil).
- **Redux Toolkit** (mais estruturado).

### 🔹 **8. Estilização no React**

- CSS Modules.
- Tailwind CSS (você já usa).
- Styled Components.

### 🔹 **9. Boas Práticas e Performance**

- Code splitting e lazy loading.
- React Profiler.
- Otimização de re-renderizações.


### 🚀 **O que é o React?**

**React** é uma **biblioteca JavaScript** para criar interfaces de usuário (UIs). Ele foi criado pelo **Facebook** e se tornou muito popular para desenvolvimento de aplicações web dinâmicas, ou seja, aquelas que precisam interagir com o usuário de forma rápida e fluida, como redes sociais, dashboards, e-commerce, etc.

### 💡 **Principais características do React:**

1. **Componentes**: O React é baseado em componentes, que são pedaços de código que representam partes da interface de usuário. Eles podem ser reutilizados e podem ter seu próprio **estado** (dados internos) e **props** (dados passados de um componente pai).
    
    - **Componente de Classe**: Antigo padrão do React (menos utilizado atualmente).
    - **Componente Funcional**: Forma moderna de escrever componentes, geralmente utilizando Hooks como `useState`, `useEffect`, etc.
    
2. **Virtual DOM**: O React usa o **Virtual DOM** (Document Object Model) para melhorar o desempenho. Ele mantém uma cópia leve da interface do usuário na memória e, quando o estado de um componente muda, ele compara essa cópia com a versão anterior, identificando as mudanças e atualizando apenas as partes que foram alteradas na tela. Isso torna a renderização muito mais eficiente.
    
3. **Unidirecionalidade**: O fluxo de dados no React é **unidirecional**, ou seja, os dados fluem de um componente **pai** para os componentes **filhos**. Isso ajuda a manter a lógica mais previsível e fácil de entender. Se você precisar alterar o estado de um componente, você pode fazer isso usando funções de **callback** passadas como **props**.
    
4. **JSX (JavaScript XML)**: O React usa uma sintaxe chamada **JSX**, que é uma mistura de **JavaScript** e **HTML**. A sintaxe parece com HTML, mas na verdade é JavaScript. Isso permite escrever a interface de forma declarativa, tornando o código mais legível e organizado.
    
    Exemplo de JSX:
    
![[Pasted image 20250220161114.png]]
    
5. **React Hooks**: Antes dos **hooks**, o React usava apenas componentes de classe para gerenciar o estado e o ciclo de vida. Porém, com os hooks, você pode fazer tudo isso em **componentes funcionais**, tornando o código mais simples e reutilizável. O `useState` e o `useEffect` são os mais comuns, mas existem outros também.

### 🎯 **Por que usar o React?**

1. **Desempenho**: O uso do **Virtual DOM** faz com que o React seja mais rápido ao atualizar a interface do usuário. Ele só atualiza as partes da UI que realmente mudaram.
2. **Reusabilidade**: Os componentes são modulares e podem ser reutilizados em diferentes partes da aplicação, o que ajuda a economizar tempo e esforço.
3. **Grande Comunidade**: O React tem uma enorme comunidade de desenvolvedores que contribuem com bibliotecas, ferramentas e tutoriais.
4. **Popularidade e Suporte**: É utilizado por grandes empresas como Facebook, Instagram, Netflix, Airbnb, etc., o que significa que você tem muitas chances de encontrar recursos e resolver problemas.


---
---

## **Criando um Projeto React**

### Vite

### 💡 **O que é o Vite?**

**Vite** é um **build tool** (ferramenta de construção) extremamente rápido e moderno para o desenvolvimento de aplicações web. O nome **Vite** vem do francês, que significa **rápido**. Ele foi criado por **Evan You**, o mesmo criador do **Vue.js**, e é projetado para melhorar a experiência de desenvolvimento e otimizar o processo de construção de aplicações front-end.

### 🌟 **Principais vantagens do Vite:**

1. **Velocidade**: O Vite se destaca pela velocidade no desenvolvimento, com tempo de inicialização muito mais rápido e recarregamento instantâneo graças ao HMR eficiente.
    
2. **Simplicidade**: O Vite tem uma configuração simples e usa **ES Modules** de maneira nativa, sem a necessidade de configurações complexas. Isso facilita a integração com outras ferramentas e tecnologias.
    
3. **Suporte para Vue, React e outros frameworks**: O Vite oferece suporte nativo para **Vue**, **React**, **Preact** e outras bibliotecas e frameworks populares.
    
4. **Otimização para produção**: Para produção, o Vite utiliza o **Rollup**, que gera pacotes altamente otimizados, com árvore de dependências eliminada (tree-shaking) e minimização de código.
    
5. **Plug-ins**: O Vite possui uma arquitetura de **plug-ins** flexível, e muitos plug-ins estão disponíveis para diferentes necessidades, como suporte a TypeScript, PostCSS, Sass, etc.

Para criar o projeto basta executar: npm create vite@latest

### **2. Estrutura de Pastas do Projeto React com Vite**

📋 **Explicação:** Após criar o projeto, a estrutura de pastas terá:

`meu-projeto/ 
│── node_modules/   # Dependências do projeto 
│── public/         # Arquivos estáticos 
│── src/            # Código principal do app │   
├── assets/     # Imagens e outros recursos │   
├── components/ # Componentes reutilizáveis │   
├── App.jsx     # Componente principal │   
├── main.jsx    # Ponto de entrada do app 
│── index.html      # HTML principal 
│── package.json    # Configuração do projeto e dependências 
│── vite.config.js  # Configuração do Vite`


---
---

## **Componentes**

### 🔥 **O que são componentes no React?**

**Componentes** são a base do React. Eles são pedaços de código que descrevem como a interface de usuário (UI) de uma aplicação deve aparecer em um dado momento. Em vez de criar uma página inteira como um único arquivo, você pode dividir a interface em partes menores e reutilizáveis chamadas **componentes**.

### 🔍 **Por que usar componentes?**

- **Reusabilidade**: Você pode reutilizar um componente em diferentes partes da sua aplicação. Por exemplo, se você tiver um botão com um estilo específico, pode usar esse componente em várias páginas.
- **Organização**: Facilita a organização do seu código, permitindo que você divida a aplicação em partes menores, mais gerenciáveis e compreensíveis.
- **Isolamento de funcionalidades**: Cada componente pode ser responsável por uma funcionalidade específica da interface. Isso facilita a manutenção e a atualização da aplicação.

### 🧩 **Tipos de Componentes no React**

No React, os componentes podem ser de dois tipos principais:

1. **Componentes Funcionais** (mais comuns atualmente)
2. **Componentes de Classe** (uma abordagem mais antiga)

### 🧩 **Como criar Componentes? Export Default vs Export**

### 📦 **1. `export default function`**

- Quando você usa `export default` para exportar uma função, está dizendo que **essa função será a principal exportação** do arquivo. Isso significa que, quando outro arquivo importar o componente, não será necessário usar chaves `{}` ao fazer a importação.

![[Pasted image 20250220163206.png]]

Aqui, **Componente** é exportado como a exportação padrão do arquivo, e quando o outro arquivo importa, ele pode usar o nome diretamente, sem as chaves.

### 📦 **2. `export function`**

- Quando você usa `export` (sem o `default`), a função é **exportada nomeadamente**. Isso significa que, para importar o componente em outro arquivo, você precisa usar o **mesmo nome** da função entre chaves `{}`.

![[Pasted image 20250220163243.png]]

Aqui, a função **Componente** é exportada com o nome dela, e ao importar, você precisa usar o nome exato do componente entre chaves.

###  **Diferenças principais entre `export default` e `export`**

| Aspecto                   | **`export default function`**                         | **`export function`**                                    |
| ------------------------- | ----------------------------------------------------- | -------------------------------------------------------- |
| **Forma de exportar**     | A função é a **exportação padrão** do arquivo.        | A função é **exportada nomeadamente**.                   |
| **Importação**            | Não usa chaves ao importar o componente.              | Usa chaves `{}` ao importar o componente.                |
| **Exemplo de importação** | `import Componente from './Componente';`              | `import { Componente } from './Componente';`             |
| **Flexibilidade**         | Só pode haver uma exportação **default** por arquivo. | Pode haver várias exportações nomeadas no mesmo arquivo. |

**A maioria dos desenvolvedores React usa `export default function`**, especialmente para arquivos que têm um único componente funcional. Essa abordagem é simples, direta e amplamente adotada, o que facilita a importação e organização do código.

### Recomendação:

- **Se o arquivo contém um único componente**, **use `export default function`**. Ele é mais limpo e segue a prática comum.
- **Se o arquivo contém vários componentes ou funções**, considere **usar `export function` (nomeado)** para ter mais controle e clareza nas importações.

Essa escolha é bastante subjetiva, mas seguir as convenções da comunidade pode tornar o código mais legível e alinhado com os projetos em que você trabalha!

---
---


### **ESTADO - STATE**
## 🎯 **O que é Estado (State) no React?**

O **estado** é uma informação que **muda ao longo do tempo** e que faz com que o componente **re-renderize** sempre que essa informação for atualizada.

### 🏠 Exemplo simples de estado na vida real:

Imagine um interruptor de luz. Ele tem **dois estados possíveis**:

- **Ligado (`ON`)**
- **Desligado (`OFF`)**

Sempre que você aperta o botão do interruptor, o **estado da luz muda**. No React, o estado funciona da mesma forma.

Se um componente tem um **contador**, seu estado pode ser:

- `0`, depois `1`, depois `2`, conforme o usuário clica em um botão.

Se um componente tem um **input de formulário**, seu estado pode ser:

- `"João"`, depois `"Maria"`, conforme o usuário digita.

O React **re-renderiza** o componente sempre que o estado muda para mostrar a informação atualizada.


---
---


## **Hooks**

### **O que são Hooks no React?**

Hooks são funções especiais do React que permitem **usar estados e outras funcionalidades** dentro de componentes funcionais. Antes dos hooks, era necessário usar **componentes de classe** para lidar com estado e ciclos de vida.

Desde o React 16.8, os **componentes funcionais** podem ter estados e efeitos colaterais, graças aos hooks.

## **Por que Hooks são úteis?**

- **Eliminam a necessidade de classes** → Código mais limpo e fácil de entender.
- **Facilitam o reaproveitamento de lógica** → Podemos criar nossos próprios hooks.
- **Permitem trabalhar com estado e efeitos colaterais** sem precisar de `this`.

Todos os hooks começam com use, por exemplo: useState.
Podemos criar os nossos hooks, isso é chamado de custom hook.

## useState 

Utilizamos para gerenciar o estado de algum dado, variáveis não funcionam corretamente, o componente não re-renderiza.

Sintaxe básica do useState:

![[Pasted image 20250220143648.png]]

📌 **Explicação:**

- `estado` → É a variável que guarda o valor do estado.
- `setEstado` → É a função que **atualiza o estado** e **re-renderiza** o componente.
- `useState(valorInicial)` → Define um **valor inicial** para o estado.

📝 **Exemplo 1: Contador simples**

![[Pasted image 20250220144138.png]]

📌 **O que acontece aqui?**

1. `useState(0)` cria um estado chamado `contador`, começando com `0`.
2. `setContador(contador + 1)` aumenta o valor do estado em 1 quando o botão é clicado.
3. O React **re-renderiza o componente** para mostrar o novo valor.

## 🎭 **Como o React re-renderiza o componente?**

Sempre que o estado é atualizado com `setEstado(novoValor)`, o React:

1. **Compara o novo valor com o valor antigo**.
2. Se for **diferente**, ele **re-renderiza** o componente.
3. Se for **igual**, ele **não re-renderiza** para evitar trabalho desnecessário.

## 📝 **Exemplo 2: Atualizando Estado com Função**

Em alguns casos, o estado **atual** pode mudar antes do React atualizar a interface. Para evitar bugs, podemos usar uma **função dentro do `setEstado`**.

![[Pasted image 20250220150242.png]]

📌 **Por que usar `prev`?**

- Se o React ainda não atualizou o estado e você tentar modificar ele **diretamente**, pode acabar sobrescrevendo um valor errado.
- `setContador(prev => prev + 1)` garante que **pegamos sempre o valor mais recente** do estado.

## 📝 **Exemplo 3: Estado com Strings**

O `useState` também pode armazenar **textos**, como no caso de um campo de input.

![[Pasted image 20250220151051.png]]

📌 **Explicação:**

- `useState("")` começa com uma string vazia.
- `onChange={(e) => setNome(e.target.value)}` atualiza o estado sempre que o usuário digita algo.

## 📝 **Exemplo 4: Estado com Objetos**

Podemos armazenar **objetos inteiros** dentro do estado.

![[Pasted image 20250220151137.png]]

📌 **Explicação:**

- `useState({ nome: "Ana", idade: 25 })` começa com um objeto.
- `setUsuario({ ...usuario, idade: usuario.idade + 1 })` mantém o restante do objeto (`...usuario`) e **muda apenas a idade**.

⚠ **Importante!**

- Sempre use o operador **spread (`...`)** para não perder propriedades do objeto!

## ✅ **Resumo do `useState`**

| Tipo de Estado | Exemplo                                 |
| -------------- | --------------------------------------- |
| Número         | `useState(0)`                           |
| String         | `useState("Olá")`                       |
| Booleano       | `useState(false)`                       |
| Objeto         | `useState({ nome: "João", idade: 30 })` |
| Array          | `useState([])`                          |

## 🎯 **Conclusão**

- O `useState` permite **armazenar e atualizar dados** dentro de componentes funcionais.
- Quando o estado muda, **o React re-renderiza o componente** automaticamente.
- Sempre use `setEstado(novoValor)` para modificar o estado corretamente.

---
---
### **Renderização de Lista

A renderização de listas é essencial no React para exibir vários itens dinamicamente, como produtos, postagens, usuários, etc. Vamos entender como isso funciona!

## 🔹 **1. Como Renderizar uma Lista no React?**

No React, utilizamos a função `.map()` para transformar um array de dados em elementos JSX.

### 📝 **Exemplo Simples: Renderizando uma Lista de Nomes**

![[Pasted image 20250220151937.png]]

📌 **Explicação:**

1. Criamos um array `nomes` com alguns valores.
2. Usamos `.map()` para percorrer o array e gerar um `<li>` para cada nome.
3. **Usamos a propriedade `key`** para identificar cada item de forma única.


## 🔹 **2. Por que a `key` é importante?**

A propriedade `key` no React **ajuda o React a identificar quais itens mudaram, foram adicionados ou removidos**. Ela é obrigatória.
Iterar listas sem a propriedade key nos gera um warning, podemos verificar isso no console;
O React precisa de uma chave única em cada um dos itens iterados;
Isso serve para ajudá-lo na renderização do componente.
Geralmente teremos um array de objetos e podemos colocar key como alguma chave única, como o id de algum dado;
Em último caso devemos utilizar o index do método map;

✅ **Correto:** Cada item da lista tem uma `key` única.  
❌ **Errado:** Usar o `index` como `key` pode causar problemas quando a ordem da lista muda.

### 📝 **Exemplo Correto (com `id`)**

![[Pasted image 20250220152021.png]]

📌 **Explicação:**

- Agora usamos `id` como `key`, o que evita problemas ao reordenar a lista.

## 🔹 **3. Renderizando Listas de Objetos com Mais Informações**

Quando trabalhamos com listas de objetos, podemos exibir várias informações por item.

### 📝 **Exemplo: Lista de Produtos**

![[Pasted image 20250220152047.png]]

📌 **Explicação:**

- Criamos um array de produtos, onde cada item tem `id`, `nome` e `preco`.
- Usamos `.map()` para gerar uma `<li>` para cada produto.

## 🔹 **4. Renderizando Listas com Componentes**

É uma boa prática criar **componentes separados** para itens da lista, tornando o código mais organizado.

### 📝 **Exemplo: Criando um Componente `Produto`**

![[Pasted image 20250220152127.png]]

📌 **Vantagens de usar um componente separado:** ✅ Melhor organização do código.  
✅ Facilita a reutilização.  
✅ Melhora a manutenção do projeto.

Exemplo Prático:

![[Pasted image 20250220154816.png]]

## ✅ **Resumo**

|Conceito|Explicação|
|---|---|
|`.map()`|Itera sobre um array e retorna elementos JSX|
|`key`|Identificador único para cada item da lista|
|Componentes separados|Melhor organização do código|
|Estado (`useState`)|Permite adicionar/remover itens dinamicamente|
|Renderização condicional|Exibe mensagens quando a lista está vazia|

## 🚀 **Conclusão**

- No React, usamos `.map()` para renderizar listas.
- Sempre usamos `key` para evitar problemas de re-renderização.
- Podemos criar listas interativas com `useState`.
- Separar componentes melhora a organização do código.



---
---


## **Public x Assets**

No React, há uma diferença importante entre colocar imagens e arquivos na **pasta `public`** e na **pasta `src/assets`** (ou apenas `assets` dentro de `src`).

## 1. `public/` → Acessível diretamente via URL

### Quando usar?

- Para **arquivos estáticos** que **não serão processados pelo Webpack**, como imagens, PDFs, fontes e JSONs que você quer acessar diretamente.
- Quando precisar referenciar um arquivo **via URL absoluta** no navegador.
### Como acessar os arquivos?

Os arquivos dentro de `public/` podem ser acessados diretamente na URL do navegador usando `/` como referência.

![[Pasted image 20250220134652.png]]

## 2. `src/assets/` → Processado pelo Webpack

###  Quando usar?

- Para **imagens e arquivos que fazem parte do código-fonte**, como logos, ícones e assets usados dentro dos componentes.
- Para **importar imagens diretamente dentro do código** e se beneficiar da otimização do Webpack.

### Como acessar os arquivos?

Os arquivos em `src/assets/` precisam ser importados dentro do código React.

![[Pasted image 20250220135000.png]]

📝 **Observação:**

- O Webpack processa essas imagens, gerando versões otimizadas para produção.
- Não é possível acessá-las diretamente via URL no navegador como no `public/`.
- 
## 🆚 Comparação rápida:

|Característica|`public/`|`src/assets/`|
|---|---|---|
|**Acesso via URL direta**|✅ Sim (`/logo.png`)|❌ Não|
|**Importação no código**|❌ Não funciona|✅ Sim (`import img from ...`)|
|**Otimizado pelo Webpack**|❌ Não|✅ Sim|
|**Bom para imagens dinâmicas**|✅ Sim (ex.: via API)|❌ Não|
|**Bom para assets usados no código**|❌ Não|✅ Sim|

---

## **Events:**

Em várias situações vamos precisar do click, como ao enviar formulários.
No React os eventos já estão prontos, podemos utilizar onClick para ativar uma função ao clicar em um elemento.
As funções geralmente tem o padrão handleAlgumaCoisa;
Em React, eventos funcionam de forma semelhante aos eventos do JavaScript, mas com algumas diferenças importantes.

O `e` (ou `event`) que geralmente aparece como parâmetro em manipuladores de eventos no React representa o **evento sintético** gerado pelo React. Esse evento é uma abstração sobre o evento nativo do navegador e é chamado de **SyntheticEvent**.

![[Pasted image 20250220132136.png]]

### Explicação:

- `handleClick(e)` é a função que lida com o evento.
- `e` contém informações sobre o evento, como o tipo (`e.type`), o elemento que disparou o evento (`e.target`), etc.
- No caso do `onClick`, quando o botão for clicado, `handleClick` será executado e o evento será registrado no console.

### Diferença entre SyntheticEvent e eventos nativos:

O `SyntheticEvent` do React é uma camada de compatibilidade que faz com que os eventos funcionem de maneira uniforme em todos os navegadores. Ele também melhora a performance ao reutilizar objetos de evento sempre que possível.

### Eventos comuns no React:

- `onClick` → Quando um elemento é clicado.
- `onChange` → Quando um valor de input muda.
- `onSubmit` → Quando um formulário é enviado.
- `onMouseEnter` → Quando o mouse entra em um elemento.
- `onKeyDown` → Quando uma tecla é pressionada.

### Exemplo 2: Passando argumentos com arrow function

Se precisar passar argumentos para a função dentro do `onClick`, a arrow function é uma ótima solução:

![[Pasted image 20250220132843.png]]

**Por que usar uma arrow function nesse caso?**

- Se fizéssemos `onClick={handleClick("Velton")}`, a função seria chamada imediatamente ao renderizar o componente, o que não queremos.
- A arrow function `() => handleClick("Velton")` faz com que `handleClick` seja executada **somente quando o botão for clicado**.