## Utilização
```js
capivara.component('simple-component', {
    template: `<input cp-focus="">`,
});
```
## Descrição

O elemento com o atributo `focus` refere-se ao elemento que atualmente recebe eventos de `<input>`. Se houver múltiplos `<input>` de texto, a que tem o foco é aquela na qual o usuário pode inserir texto. Apenas um elemento tem o foco de cada vez.
A diretiva `cp-focus` fará com que seja possível executar funções ou ações quando o elemento `<input>` for selecionado através do clique do usuário.

## Exemplos

```HTML
<simple-component></simple-component>
```

Exemplo de utilização do `cp-focus` para execução de uma função.

```js
class simpleComponent {
  onFocus() {
    console.log('Focused');
  }
}

capivara.component('simple-component', {
  template: `<input type="text" placeholder="Click Here" cp-focus="$ctrl.onFocus()">`,
  controller: simpleComponent
});
```