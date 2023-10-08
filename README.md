# Hoisting en JavaScript

El hoisting es un comportamiento en JavaScript que puede parecer confuso al principio, pero es importante entenderlo para escribir código más efectivo y evitar errores inesperados. En esencia, el hoisting se refiere a cómo JavaScript mueve las declaraciones de variables y funciones al principio del ámbito en el que se encuentran durante la fase de compilación.

## Variables en JavaScript

Cuando declaras una variable en JavaScript utilizando la palabra clave `var`, `let`, o `const`, la declaración se "eleva" (hoisting) al principio del ámbito en el que se encuentra. Sin embargo, la asignación de valor permanece en su lugar. Veamos un ejemplo:

```javascript
console.log(x); // Resultado: undefined
var x = 5;
console.log(x); // Resultado: 5
```

Aunque pareciera que `x` no está definido en el primer `console.log`, en realidad JavaScript lo lleva al principio del ámbito de la función o bloque, por lo que no se produce un error. Sin embargo, su valor aún no se ha asignado, por lo que obtendrás `undefined`.

Con `let` y `const`, se comportan de manera similar, pero la diferencia clave es que `let` y `const` no permiten acceder a la variable antes de su declaración (esto se llama "temporalmente muerto"), lo que puede ayudar a prevenir errores sutiles.

## Funciones en JavaScript

Las funciones en JavaScript también se ven afectadas por el hoisting. Puedes llamar a una función antes de declararla en tu código. Por ejemplo:

```javascript
sayHello(); // Resultado: "Hola, mundo!"

function sayHello() {
  console.log("Hola, mundo!");
}
```

JavaScript mueve la declaración de la función `sayHello` al principio de su ámbito, lo que permite que la llamada a la función se realice antes de la declaración real.

Sin embargo, es importante tener en cuenta que esto solo se aplica a las declaraciones de funciones y no a las expresiones de funciones.

## Video Explicativo.

[![](http://img.youtube.com/vi/41YZTg8sjyM/0.jpg)](https://www.youtube.com/watch?v=41YZTg8sjyM "")



## Resumen

El hoisting es un comportamiento fundamental en JavaScript que afecta a cómo las variables y las funciones se tratan durante la fase de compilación. Aunque puede parecer confuso, comprender cómo funciona el hoisting te ayudará a escribir un código más claro y evitar errores inesperados en tu desarrollo JavaScript.

