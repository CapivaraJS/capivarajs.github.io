## Utilização
```js
@Component({
    tag: 'simple-component',
    template: `
        <h1 cp-if=""></h1>
        <h1 cp-else></h1>`
})
```
## Descrição

O `cp-else` deve ser utilizado logo após a diretiva `cp-if` ou `cp-else-if`, ela é visível quando todas as outras condicionais forem falsas. O `cp-else` é único, ele **obrigatoriamente** deve acompanhar um `cp-if`, e não possui condições, ou seja, não existe comparação a serem feitas para que o fluxo de execução entre em seu escopo.

## Exemplos

```HTML
<simple-component></simple-component>
```

Exemplo de utilização junto com `cp-if`.

```js
const {Component, Controller, OnInit} = capivara.core

@Component( {
  tag: 'simple-component',
  template: `
    <h1 cp-if="$ctrl.showText">A simple text</h1>
    <h1 cp-else>Other simple text</h1>
  `
})

class simpleComponent extends Controller implements OnInit {
  $onInit() {
    this.showText = false
  }
}
```
Disponibilizamos o exemplo em diferentes ambientes.
* [CapivaraJS](https://jsfiddle.net/jcanabarro/zf8gqh0d/371/)
* [VueJS](http://jsfiddle.net/jcanabarro/ygznj9mt/69/)
* [React](http://jsfiddle.net/jcanabarro/td4v7qqd/356/)
* [Angular](https://jsfiddle.net/t0b8xxfj/134/)

Exemplo de utilização junto com `cp-if` e `cp-else-if`.

```js
const {Component, Controller, OnInit} = capivara.core

@Component( {
  tag: 'simple-component',
  template: `
    <h1 cp-if="$ctrl.firstValue > $ctrl.secondValue">A simple text</h1>
    <h1 cp-else-if="$ctrl.firstValue === $ctrl.secondValue">Other simple text</h1>
    <h1 cp-else>Last condition</h1>
  `
})

class simpleComponent extends Controller implements OnInit {
  $onInit() {
    this.firstValue = 10;
    this.secondValue = 20;
  }
}
```
Disponibilizamos o exemplo em diferentes ambientes.
* [CapivaraJS](https://jsfiddle.net/jcanabarro/zf8gqh0d/371/)
* [VueJS](http://jsfiddle.net/jcanabarro/ygznj9mt/71/)
* [React](http://jsfiddle.net/jcanabarro/td4v7qqd/358/)
* [Angular](https://jsfiddle.net/t0b8xxfj/135/)