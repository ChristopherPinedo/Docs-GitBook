# Funciones

## Funciones Puras e Impuras



Las funciones puras no dependen de factores externos y son predecibles, trabajan con los argumentos que asignamos y constantes como números, o PI.

```javascript
// función pura
function priceAfterTax(productPrice) {
  return (productPrice * 0.20) + productPrice;
}
```

En el caso de que nuestra función utilice variables externas, se considera impura, si otro desarrollador o proceso puede cambiar el valor de `tax` en el siguiente ejemplo, el valor de retorno no sería predecible.

```javascript
// función impura
var tax = 20;

function calculateTax(productPrice) {
 return (productPrice * (tax/100)) + productPrice; 
}
```

