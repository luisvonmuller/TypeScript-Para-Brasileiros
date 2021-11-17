# 🤔 False, true, "Falsy" & "Truthy" 👀

## ⚙️ Entendendo um pouco do contexto Geral.

Na computação temos um Tipo chamado: "Booleano". O que é: Booleano?&#x20;

{% hint style="success" %}
Aqui estamos falando tipo primitivo do TypeScript: "Boolean". (⊙.☉)7
{% endhint %}

Ser do tipo (Booleano) significa que algum valor, isto é, alguma variável, constante ou qualquer coisa que possuí em si um valor desse **tipo** pode ser:&#x20;

* **Verdadeiro** (Isto é, _true_) 👍
* **Falso** (Isto é, _false_) 👎

{% hint style="info" %}
O nome "Booleano" (_Boolean_ em **TypeScript**) faz uma homenagem ao Matemático & Filósofo **George Boole**, ele "construiu" a base algébrica necessária para a criação Lógica Algébrica que podemos usar para: Operações lógicas **(em booleanos)** como [conjunção](https://pt.wikipedia.org/wiki/Conjun%C3%A7%C3%A3o\_l%C3%B3gica) (**||**), [disjunção](https://pt.wikipedia.org/wiki/Disjun%C3%A7%C3%A3o\_l%C3%B3gica) **(&&)**, [disjunção exclusiva](https://pt.wikipedia.org/wiki/Disjun%C3%A7%C3%A3o\_exclusiva) (**(p && !q) || (!p && q)**), [equivalência lógica](https://pt.wikipedia.org/wiki/Equival%C3%AAncia\_l%C3%B3gica) (**==**) e [negação](https://pt.wikipedia.org/wiki/Nega%C3%A7%C3%A3o) **(!)**, que correspondem a algumas das operações da [álgebra booliana](https://pt.wikipedia.org/wiki/%C3%81lgebra\_booleana) (É a parte da do conceito da **Matemática Discreta**).&#x20;
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

## :thinking: Por que existe: "Falsy" ou "Truthy"?

Na [lógica](https://pt.wikipedia.org/wiki/L%C3%B3gica), afirmações **diferentes** são **logicamente equivalentes** se tiverem o mesmo conteúdo lógico. Isto é, se elas tiverem o mesmo [valor de verdade](https://pt.wikipedia.org/wiki/Valor\_de\_verdade) em todos os modelos. Também conhecido por "Tautologia", isto é, algo que é correspondente em termos lógicos.

## :thumbsdown: O que é o "<mark style="color:yellow;">Falsy</mark>" ou _Errôneo/_Falseáveis ?&#x20;

<mark style="color:yellow;">****</mark>:arrow\_right: <mark style="color:yellow;">**Falsy**</mark> é um **"**_**pseudo tipo**_**"  **logicamente equivalente ao **Valor Primitivo  **<mark style="color:red;background-color:red;">**false**</mark> para o <mark style="background-color:orange;">**JavaSript.**</mark>

#### Os valores que seriam aceitos como <mark style="color:red;background-color:red;">**false**</mark> seriam:&#x20;

* **0** - (O valor numérico Zero).
* **0n** - (Um inteiro de GIGANTE cujo valor numérico é zero - um _**bigInt**_).
* **null** - (O tipo primitivo **Nulo**).
* **undefined** - (Algo que não possui valor atribuído, isto é, **indefinido**).
* **NaN** (_**Not-a-Number**_** -** algo que não é um número **pertencente** ao conjuntos dos reais)
* **"" ou '' ** (Uma cadeia de **caracteres vazia**)

### Segue a  prova do supracitado (☞ﾟヮﾟ)☞&#x20;

```typescript
const inteiroDeValorNumericoZero: number = 0;
const floatDeValorNumericoZero: number = 0.0;
const inteiroGrandeComValorNumericoZero: bigint = BigInt(0);
const nulo: null = null;
let indefinido;
const naoNumero: number = Number.NaN; //Sim, o tipo de NaN é "numero" ¯\_(ツ)_/¯
const cadeiaDeCaracteresVazia = '';

let valoresInexatos: unknown[] = [
    inteiroDeValorNumericoZero,
    floatDeValorNumericoZero,
    inteiroGrandeComValorNumericoZero,
    nulo,
    indefinido,
    naoNumero,
    cadeiaDeCaracteresVazia
]

valoresInexatos.forEach((valor) => console.log(valor ? "Verídico" : "Errôneo/Falseáveis"));
```

## &#x20;O que é "<mark style="color:green;">Truthy</mark>" ou Verídico?&#x20;

<mark style="color:green;">**Truthy**</mark> é um **"**_**pseudo tipo**_**"  **logicamente equivalente ao **Valor Primitivo  **<mark style="color:blue;background-color:green;">**true**</mark> para o <mark style="background-color:orange;">**JavaSript.**</mark>

#### Os valores que seriam aceitos como <mark style="color:blue;background-color:green;">**true**</mark> seriam:&#x20;

* **'0'** ou **"0"** - (Uma **cadeia de caracteres** com o Valor numérico **zero** dentro dela).
* **'false'** ou **"false"** (...) - (Uma cadeira de caracteres com a palavra _**"false"**)._
* **\[]**_ - _(Um** vetor **(**"**_**array**_**" **vazio), isto é,** **sem elementos presentes dentro dele)
* {} - (Um **objeto** sem nenhuma propriedade.)
* ()=>{} - (Uma definição de função anônima ou não.



****

