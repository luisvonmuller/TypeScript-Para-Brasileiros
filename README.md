# 🇧🇷 Guia de Estilos 🎨

🔥 Este é um **Guia não oficial** e você pode opinar através do repositório de GitHub para juntos chegarmos a melhor definição do Ideal! **Vamos colaborar? 💪**

## 👉 Navegação por tópico facilitada!

* ⭐️ Variáveis & Funções
* 📦 Classes
* 🔌 Interfaces
* 🌟 Tipos
* 😳 Namespaces
* 🔢 Enum
* <mark style="background-color:purple;">\*\* 📭 null\*\*</mark> vs <mark style="background-color:purple;">\*\* 😱 \*\*undefined</mark>
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
Use _**PascalCase**_ para nomear o seu conjunto nomenclatural ⚙️
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

##
