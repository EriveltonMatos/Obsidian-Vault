
### **INTERFACES**

## 📌 O que é uma interface no TypeScript?

Uma **interface** no TypeScript é uma forma de definir a estrutura de um objeto, especificando quais propriedades ele deve ter e quais são seus tipos.

No seu código, a interface foi usada para definir os tipos das `props` do componente `UserName`:

![[Pasted image 20250221145607.png]]
Isso significa que o componente `UserName` **só pode receber** valores do tipo `string` para `name` e `modelo`.

## 🤔 Por que adicionar uma interface?

Usar uma interface traz **segurança e organização** ao código. Algumas vantagens:

✅ **Ajuda a evitar erros**: O TypeScript avisa se tentarmos passar um valor inválido para `UserName`.  
✅ **Facilita a manutenção**: Se o componente precisar de novas propriedades, basta atualizar a interface.  
✅ **Melhora a leitura do código**: Outros desenvolvedores (ou você no futuro) entenderão melhor quais dados são esperados.

## 🔄 Dá para trocar `interface` por `type`?

Sim! No TypeScript, também podemos usar `type` para definir a estrutura dos objetos.

A alternativa usando `type` ficaria assim:

![[Pasted image 20250221145702.png]]

E o componente continuaria funcionando normalmente:

![[Pasted image 20250221145721.png]]

## 🆚 Qual a diferença entre `interface` e `type`?

| Característica                                          | `interface`       | `type`            |
| ------------------------------------------------------- | ----------------- | ----------------- |
| **Pode ser estendida (herança)**                        | ✅ Sim (`extends`) | ✅ Sim (união `&`) |
| **Pode definir funções**                                | ✅ Sim             | ✅ Sim             |
| **Pode ser usada para definir objetos complexos**       | ✅ Sim             | ✅ Sim             |
| **Pode definir tipos primitivos (string, number etc.)** | ❌ Não             | ✅ Sim             |

Na maioria dos casos, **`type` e `interface` funcionam da mesma forma** para definir objetos simples como esse.

👉 Se precisar estender a estrutura no futuro, `interface` pode ser mais útil.  
👉 Se quiser um código mais compacto, `type` pode ser uma boa opção.

### 🔥 Conclusão

- **`interface`** e **`type`** são parecidos, e ambos podem ser usados nesse caso.
- Se for apenas para definir um objeto simples, tanto faz qual usar.
- `interface` é melhor para estruturas mais complexas e reutilizáveis.