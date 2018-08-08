## Utilização
```js
capivara.component('simple-component', {
    template: ` <button cp-mouse=""></button>`,
});
```

## Descrição

A diretiva `cp-mouse` é utilizada para disparar eventos com o mouse, utilizando a sua movimentação, caso você queira uma diretiva que dispare eventos utilizando o `click`, clique [aqui](/Directives/cp-click), a diretiva `cp-mouse` possui algumas variantes, sendo elas:
 
| Atributo | Descrição  |
|  ----- | ----  |
| `cp-mouseover` | Dispara uma ação quando o ponteiro do mouse está sobre um elemento |
|` cp-mouseout`  | Dispara uma ação quando o ponteiro do mouse se move para fora do elemento |
| `cp-mousedown` | Dispara uma ação quando o mouse é pressionado sobre um elemento |
| `cp-mouseup` |  Dispara uma ação quando o mouse é solto sobre um elemento |
| `cp-mousemove` | Dispara uma ação quando o mouse está se movendo sobre o elemento | 
| `cp-mouseleave` | Similar ao `mouseout`, a única diferença é que o evento **não** cria bolha |
| `cp-mouseenter` | Similar ao `mouseover`, a única diferença é que o evento **não** cria bolha |


## Exemplos
```HTML
<simple-component></simple-component>
```

Utilização das diretivas `cp-mouseover` e `cp-mouseout`.

```js
class simpleComponent {
  constructor() {
    this.text = "mouse"
  }
  mousein() {
    this.test = 'mousein';
  }
  mouseout() {
    this.test = 'mouseout';
  }
}

capivara.component('simple-component', {
  template: `
   <input cp-mouseover="$ctrl.mousein()" cp-mouseout="$ctrl.mouseout()" cp-model="$ctrl.test">
  `,
  controller: simpleComponent
});
```
Se quiser dar uma olhada, esse exemplo está no [JSFiddle](https://jsfiddle.net/zf8gqh0d/73/)