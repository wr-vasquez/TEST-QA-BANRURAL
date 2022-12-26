# Plan de Ataque
## Ejecucion del proyecto
Como primer punto siguiendo las instrucciones dadas en la prueba, se abrió el archivo index.html en el cual se realiza la ejecución del programa, el cual no funcionó según lo requerido.
## Inspeccion de errores
Se procede a inspeccionar los erroes abriendo la consola del navegador  y el primer error encontrado fue que el evento  en la linea 88 estaba mal escrito
<div>
 <img src="https://postimg.cc/vDVxmDtC" alt="errordeEvento" width="600" height="400"/>
</div>

la cual se procede acorregir de la siguiente manera: addEventListener
<img src="https://postimg.cc/xq15cv4q" alt="errordeEvento" width="600" height="400"/>

## Se verifica el color de la Notificacion de error
Una vez corregido el primer error se ejecuta de nuevo el programa y se verifica que la Notificacion de incorrecto esta mal ya que lo solicitado es que sino se adivina la notificacion debe ser de color negro y se muestra incorrecto en color verde. de igual forma se corrigen las demas notificaciones de color segun lo solicitado

## Se corrige el Error de la Notificacion de Aprobado
Una vez se Prueba el juego la Notificacion es de color Rojo y se modifica a color Verde .

## Se corrige el numero de intentos 
Se corrige el numero de intentos de 5 a 10 en la linea 46   const ATTEMPS = 10;

## Correccion de linea 87
Al inspeccionar la consola nos arroja el siguiente error 
Uncaught TypeError: Cannot set properties of null (setting 'textContent')
    at HTMLInputElement.checkGuess (index.html:87)
Este error se da porque las clases de css deben iniciar con un punto por 
eso se debe corregir la linea 49 para que quede de la siguiente manera
const lowOrHi = document.querySelector('.lowOrHi');


## Correccion del evento addEventListener y funcion setGameOver
Uncaught TypeError: resetButton.addeventListener is not a function
    at setGameOver (index.html:102:16)
    at HTMLInputElement.checkGuess (index.html:77:7)
Para este caso se corrigen ambas lineas de codigo 

## El sisttema solo debe aceptar numeros 
Se agrega la siguiente alerta en la linea  99 de lo contrario el juego acepta letras
else{
        alert("Porfavor, ingrese un numero entero ");
      }


## Error en el numero aleatorio
Se corrige que el rango de numeros sea de 1  a 100 de la siguiente manera 
  let randomNumber =  Math.floor(Math.random() * (100 - 1)) + 1;