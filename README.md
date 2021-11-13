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
* 📑 Formatação no geral
* 🤔 Aspas simples vs Aspas Duplas
* 👯‍♀️ Anotação de Tipos para Array
* ⚙️ Uso de ponto e vírgula ao final de linhas **" ; "**
* 📂 Uma sugestão para uma boa nomeação de Arquivos
* 🤨 Tipo vs Interface
* ⚠️ Comparadores, "==" vs "==="

## ⭐️​ Variáveis e Funções:

{% hint style="success" %}
Use _**camelCase**_ para nomear variáveis e funções
{% endhint %}

#### &#x20;Má nomenclatura 🚫

```typescript
let FulanoVariavel: string = "#ForaBolsonaro";
function CiclanoFuncao(){}
```

#### Boa nomenclatura ✅​&#x20;

```typescript
let fulanoVariavel: string = "#ForaBolsonaro";
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
if (error != null) // Garante que é um valor de tipo primitivo.

```
