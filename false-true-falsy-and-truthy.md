# 🤔 False, true, "Falsy" & "Truthy" 👀

## ⚙️ Entendendo um pouco do contexto Geral.

Na computação temos um Tipo chamado: "Booleano". O que é: Booleano?&#x20;

{% hint style="success" %}
Aqui vamos falar sobre o tipo primitivo do TypeScript: "Boolean". (⊙.☉)7
{% endhint %}

Ser do tipo (Booleano) significa que algum valor, isto é, alguma variável, constante ou qualquer coisa que possuí em si um valor desse tipo pode ser:&#x20;

* Verdadeiro (Isto é, true) 👍
* Falso (Isto é, false) 👎

{% hint style="info" %}
O nome "Booleano" (Boolean em TypeScript) faz uma homenagem ao Matemático & Filósofo George Boole, ele "construiu" a base algébrica necessária para a Lógica Algébrica que podemos usar para: operações lógicas como [conjunção](https://pt.wikipedia.org/wiki/Conjun%C3%A7%C3%A3o\_l%C3%B3gica), [disjunção](https://pt.wikipedia.org/wiki/Disjun%C3%A7%C3%A3o\_l%C3%B3gica), [disjunção exclusiva](https://pt.wikipedia.org/wiki/Disjun%C3%A7%C3%A3o\_exclusiva), [equivalência lógica](https://pt.wikipedia.org/wiki/Equival%C3%AAncia\_l%C3%B3gica) e [negação](https://pt.wikipedia.org/wiki/Nega%C3%A7%C3%A3o), que correspondem a algumas das operações da [álgebra booliana](https://pt.wikipedia.org/wiki/%C3%81lgebra\_booleana) (É a parte da do conceito da Matemática Discreta).&#x20;
{% endhint %}

### Fornecendo um exemplo básico ԅ(≖‿≖ԅ):

```typescript
/** Vamos iniciar uma constante "Booleana" verdadeira */
const constanteVerdadeira: Boolean = true;
/** Vamos iniciar uma constante "Booleana" falsa através da inversão do seu valor boleano com o operador "!" */
const constanteFalsa: Boolean = !constanteVerdadeira;

if(constanteFalsa && constanteVerdadeira ) {
    console.log("Ambas as constantes são verdadeiras. ヽ(´▽`)/")
} else if (constanteFalsa || constanteVerdadeira) {
    console.log("Ao menos uma das constantes são falsas ( ಠ ʖ̯ ಠ )")
} else {
    console.warn("Nenhuma constante é verdadeira (҂◡_◡)")
}
```
