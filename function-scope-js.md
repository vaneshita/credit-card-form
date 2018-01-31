### LEER CODIGO EN JS

*Identificar las funciones globales, locales, funciones de callback, expresions, statement, clousure, scope, contextos de ejecucion, que funciones forman parte de la pila de ejecucion (stack execution) y que funciones forman parte de la cola de eventos (event queue). Para ello crearan un archivo markdown(.md) titulado function-scope-js*
___

## Funciones globales

*Es una función global con respecto al contexto de ejecución "document" y con respecto al contexto de ejecución "window" es una función local.*
* (**línea1**)
funcion anónima
  ```javascript
$(document).ready(function() {});
};
  ```
___

## Variables globales

*Variables globales con respecto al contexto de ejecución "document" y son locales para el contexto de ejecución global "window".*

```javascript
var $inputCard = $('#card-number');
var $inputMonth = $('.input-month');
var $inputYear = $('.input-year');
var $buttonNext = $('#next');
var regexOnlyNumbers = /^[0-9]+$/;
var labelErrorOrSuccessMessages = $('label[for="card-number"]');
```
___

## Funciones locales y Pila de ejecucion

*Para el contexto de ejecucion "window" son locales pero para el contexto de ejecucion "document" son globales".*   

* (**línea19**) function activeButton() {}
* (**línea24**) function desactiveButton() {}
* (**línea29**) function longitud(input) {}
* (**línea36**) function soloNumeros(input) {}
* (**línea44**) function isValidCreditCar(numberCard){}

  ___

## Variables locales

* (**línea37**) regex
* (**línea45**) creditCardNumber
* (**línea47**) arr
* (**línea48**) sumaTotal
* (**línea49**) index

___

## Funciones callback
*Es una “llamada de vuelta”. Llamo a una funcion y le envío por parámetro otra función (un callback) esperando que la función que llamé se encargue de ejecutar esa función *

 - **(Linea 44-45)**
 ```javascript
 function isValidCreditCard(numberCard) {
   var creditCardNumber = soloNumeros(longitud(numberCard));
};
   ```

 - **(Linea 29-33)**  
```javascript
  function longitud(input) {
     if (input.trim().length === 16) {
       return input;
     }
   }
  ```

  - **(Linea 36-41)**  
 ```javascript
 function soloNumeros(input) {
  var regex = /^[0-9]+$/;
  if (regex.test(input)) {
    return input;
  }
}
   ```
___

## Cola de eventos
*Es un mecanismo que permite manejar los eventos para un determinado elemento.*

 -  **(Linea 14)**

 ```javascript
  $inputCard.on('input', function() {});
   ```
___

### **Alumnas**

>##### Vanessa Mendoza Inoñan
