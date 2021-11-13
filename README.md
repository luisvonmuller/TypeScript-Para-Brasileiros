# 🇧🇷 Guia de Estilos 🎨

🔥 Este é um **Guia não oficial** e você pode opinar através do repositório de GitHub para juntos chegarmos a melhor definição do Ideal! **Vamos colaborar? 💪**

## 👉 Navegação por tópico facilitada!

* ⭐️ Variáveis & Funções
* 📦 Classes
* 🔌 Interfaces
* 🌟 Tipos
* 😳 Namespaces
* 🔢 Enum
* <mark style="background-color:purple;">📭 null</mark> vs  <mark style="background-color:purple;">😱 undefined</mark>
* 📑 Formatação
* 🤔 Aspas simples vs Aspas Duplas
* ⚙️ Uso de ponto e vírgula ao final de linhas **" ; "**
* 👯‍♀️ Anotação de Tipos para Array
* 📂 Uma sugestão para uma boa nomeação de Arquivos
* 🤨 Tipo vs Interface
* ⚠️ Comparadores, "==" vs "==="

## ⭐️​ Variáveis e Funções:

{% hint style="success" %}
Use _**camelCase**_ para nomear variáveis e funções
{% endhint %}

#### &#x20;Má nomenclatura 🚫

```typescript
let FulanoVariavel: string = '#ForaBolsonaro';
function CiclanoFuncao(){}
```

#### Boa nomenclatura ✅​&#x20;

```typescript
let fulanoVariavel: string = '#ForaBolsonaro';
function ciclanoFuncao(){}
```

## 📦 Class

{% hint style="success" %}
Use _**PascalCase**_ para nomear suas classes! (Ou use programação funcional 👀)
{% endhint %}

#### &#x20;Má nomenclatura 🚫

```typescript
class fulano {}
```

#### Boa nomenclatura ✅​&#x20;

```typescript
class Fulano {}
```

{% hint style="success" %}
Use _**camelCase**_ para as propriedades e métodos de suas classes! 🔥
{% endhint %}

#### Má nomenclatura 🚫

```typescript
class fulano {
    DeTal: string; 
    Ciclano( ){ }
} 
```

#### Boa nomenclatura ✅​&#x20;

```typescript
class Fulano {
    deTal: string; 
    ciclano( ){ }
} 
```

## 🔌​ Interfaces:

{% hint style="success" %}
Use _**PascalCase**_ para nomear a Interface ⚙️

* Use _**camelCase**_ para nomear seus membros 🥰
{% endhint %}

{% hint style="danger" %}
Não use o Prefixo "I", exemplo: IfuncaoFulano... 😡&#x20;
{% endhint %}

#### &#x20;Má nomenclatura 🚫

```typescript
interface IFulano { 
    DeTal: string;
} 
```

#### Boa nomenclatura ✅​&#x20;

```typescript
interface Fulano { 
    deTal: string;
} 
```

## 🌟 Tipos&#x20;

{% hint style="success" %}
Use _**PascalCase**_ para nomear o seu Tipo ⚙️

* Use _**camelCase**_ para nomear as propriedades do seu tipo! 🥰
{% endhint %}

#### &#x20;Má nomenclatura 🚫

```typescript
type fulano = {
    DeTal: string;
}
```

#### Boa nomenclatura ✅​&#x20;

```typescript
type Fulano = {
    deTal: string;
}
```

## 😳 Namespaces&#x20;

{% hint style="success" %}
Use**`PascalCase `**`para nomear os "Namespaces" - ⭐️ Padrão do time do TS.`
{% endhint %}

#### Má nomenclatura 🚫

```typescript
namespace fulanoDeTal {
}
```

#### Boa nomenclatura ✅​&#x20;

```typescript
namespace FulanoDeTal {
}
```

## 🔢 Enum&#x20;

{% hint style="success" %}
Use_**`PascalCase`**_`para nomear os Enums.`

* Use _**`PascalCase`**_`para nomear seus subtipos/valores.`
{% endhint %}

#### Má nomenclatura 🚫

```typescript
enum jogodoBicho {
    avestruz,
    borboleta,
    cachorro
}

```

#### Boa nomenclatura ✅​&#x20;

```typescript
enum JogoDoBicho {
    Avestruz,
    Borboleta,
    Cachorro
}
```

## 😅 <mark style="color:blue;">Null</mark> vs <mark style="color:green;">Undefined</mark> 👀

{% hint style="success" %}
Tente não usar nenhum deles para indisponibilidade explícita! ⭐️
{% endhint %}

#### Mal caso de uso 🚫

```typescript
let pontos : {x: number, y: number | null | undefined }  = {x: 1, y: undefined } 
```

#### Bom caso de uso  ✅​&#x20;

```typescript
let pontos: {x: number, y?: number } = { x: 777 } //  
```

{% hint style="info" %}
Em suma: Precisa informar que uma propriedade é pode ser "indefinida"? Use o operador "?" antecedendo o seu tipo! 🥰
{% endhint %}

### 👉 Retorno de funções? 🤔

Mal caso de uso 🚫

```typescript
return null;
```

Bom caso de uso  ✅​&#x20;

```typescript
return undefined;
```

{% hint style="info" %}
Por quê? Sugiro você consultar a página Sobre False, True, Truthy & Falsy. 🥰

&#x20;\- Talvez ela ainda não esteja disponível ainda, foi mal gurizada hahaha! 😅
{% endhint %}

### 🤨​ Callbacks?

{% hint style="warning" %}
Use _**null**_ quando for parte da API ou de sua convenção usar.&#x20;

É quase em um consenso em Node.js, por exemplo: **`error`** é **`null`**`em chamadas do` _**NodeBack.**_
{% endhint %}

Mal caso de uso 🚫

```typescript
callbackDeAlgo(undefined);
```

Bom caso de uso  ✅​&#x20;

```typescript
callbackDeAlgo(null);
```

### E como verificar isso aí? 😅

{% hint style="success" %}
Cheque por  "Truthy" em objetos sendo <mark style="color:blue;">**null**</mark> ou <mark style="color:green;">**undefined**</mark>.
{% endhint %}

Mal caso de uso 🚫

```typescript
if (error === null) // e se for undefined? 
```

Bom caso de uso  ✅​&#x20;

```typescript
if (error) // é Válido tanto para undefined quanto para o null
```

### 👉 Um exemplo um pouco mais completo sobre verificação 🔥

{% hint style="success" %}
Use "==" null ou "!=" null. Não use "===" ou "!==" para checar por <mark style="color:blue;">null</mark> ou <mark style="color:green;">undefined</mark> quando querendo verificar tipos primitivos porque funciona apenas nos tipos primitivos supracitados e não para valores "Falseáveis", como por exemplo: 0, false, etc.&#x20;
{% endhint %}

Mal caso de uso 🚫

```typescript
if (error !== null) // Não garante que seja apenas nullo. Pode ser um valor Falseável.
```

Bom caso de uso  ✅​&#x20;

```typescript
if (error != null) // Garante que é um valor de tipo primitivo (ou seja, null ou undefined mas não falsy).
```

## 📑 Formatação

{% hint style="info" %}
O Compilador do _<mark style="color:blue;background-color:blue;">**TypeScript**</mark>_ já fornece um bom serviço de formatação estrutural, o que já é bom o suficiente para diminuir o esforço mental do desenvolvedor (ou do time). Todavia, você também pode usar o <mark style="color:blue;background-color:blue;">**tsfmt**</mark> no terminal (linha de comando para formatar seu código) - e também está disponível como plugin para várias **IDES (vscode, etc).**&#x20;
{% endhint %}

👉 Só um exemplo que eu acho pertinente, ou melhor, uma boa prática:

```typescript
let fora: string = 'Bolsonaro';
```

{% hint style="success" %}
No caso, usamos um espaço depois da definição do tipo...&#x20;

* <mark style="color:blue;">let</mark> variavel:<mark style="color:green;">(espaço)</mark>tipo<mark style="color:green;">(espaço)</mark>=<mark style="color:green;">(espaço)</mark>valor<mark style="color:blue;">(ponto e virgula)</mark>
{% endhint %}

## 💬 Sobre Aspas...

{% hint style="success" %}
Prefira usar aspas simples (single quotes) ao invés de aspas duplas.

* Times grandes que usam JS/TS o fazem. É uma convenção quasae que de mercado, também é o sugerido pelo time do "Prettier".
{% endhint %}

```typescript
let foraQuem: string = 'Jair Messias Bolsonaro';
```

Todavia, muita vezes em inglês precisamos usar o a single quote para conjugar um verbo: <mark style="color:green;">"I'm"</mark>

{% hint style="danger" %}
Se a aspas simples não lhe cabe. Use então "\`"&#x20;

* Faça o uso do <mark style="color:green;">string template</mark> do <mark style="color:yellow;">JS</mark> ao invés de concatenar variáveis strings através var + "..."  + var2.
{% endhint %}

```typescript
let foraQuem: string = 'Bolsonaro';
console.log(`Fora ${foraQuem}`)
```

{% hint style="warning" %}
Sobre outras coisas como usar "tabs" ou espaço. O sugerido para JS é 2 espaços (e muitas companias como Facebook, Airbnb, google seguem esse padrão. Mas o time do TS usa 4 e o do VScode também 😅. Isso é variável e de gosto muito mais pessoal ou convenção própria e do teu time 🥰
{% endhint %}

_(Mas eu uso tabs configuradas como 4 espaços)_ 🤗

## ⚙️​ Ponto & Vírgula;

{% hint style="success" %}
Use ponto e vírgulas, por quê?&#x20;

* Pontos e vírgulas explícitos ajudam os identadores (tsfmt/prettier) a identificar e "estruturar" seu código.&#x20;
* A falta de ponto e vírgula pode ser incômodo para novos desenvolvedores em TS. Já que a maioria das linguagens o implementa. (Houve um debate sobre como isso pode ser "incomodo" para novos desenvolvedores e outros. [https://github.com/tc39/ecma262/pull/1062](https://github.com/tc39/ecma262/pull/1062))
* Empresas grandes usam em suas implementações, ex: Google/Angular - Facebook/React - Microsoft/VScode...
{% endhint %}
