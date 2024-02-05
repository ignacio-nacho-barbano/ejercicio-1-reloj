# Ejercicio 1 - Reloj Alarma

## Propuesta

Este ejercicio consiste en construir una web-app de reloj alarma sencillo similar a los que podemos encontrar en nuestros teléfonos, el mismo tendrá las funciones de ver la hora, marcar un temporizador y una alarma.

## Tecnologías

El mismo deberá ser construido para funcionar en la web utilizando HTML, CSS y JavaScript. Debe funcionar y verse bien, tanto en clientes de escritorio como dispositivos móviles. Está permitido utilizar la clase Date de javascript para las soluciones, pero no librerías externas.

## Diseño

El diseño debe encajar con los diseños provistos en este archivo de [figma](https://www.figma.com/file/Ia6ugagTdH8hAMzVKfDF7H/app?type=design&node-id=7%3A1167&mode=design&t=xtz4BYmfTjeKsjOm-1), tanto en colores como en medidas, espaciados, fuentes y demás detalles.

## Requisitos

### Función Reloj

Se debe poder ver la hora actual exacta en el formato hh:mm:ss 24 hs
Se debe poder apagar con un botón Apagar, en ese caso la pantalla deberá mostar --:--:--
Se debe poder encender nuevamente, utilizando el mismo botón, el cual debe indicar en su texto la acción correcta, es decir `Encender`

### Función Alarma

#### Crear

Se debe poder acceder a la misma mediante un botón Alarma
Se debe poder poner una alarma indicando la hora de la misma en formato `hh:mm`
Se podrá guardar un mensaje opcional asociado a la misma
Si no se indica un mensaje el mensaje por defecto debe ser `Alarma`
La alarma solo se creará si se presiona el botón `Guardar`
Una vez guardada debe aparecer en la lista de alarmas
Un indicador de estado `Activada \ Desactivada`, con el estado en `activada` por defecto

#### Editar

Al clickear el botón con el ícono lápiz se debe poder editar la alarma, cambiando la hora y mensaje existentes
Al clickear el indicador de estado, esta debe cambiar su estado actual y solo sonar si está activada

#### Sonar

Una vez que la hora de que una alarma existente llegue, si esta está activa, se debe mostar un dialog html con el mensaje de la misma, reproduciendo el archivo sounds/alarm-sound.wav utilizando la etiqueta [`<audio>`](https://www.w3schools.com/tags/tag_audio.asp) y controlando la misma mediante [la API del DOM](https://www.w3schools.com/tags/ref_av_dom.asp)

#### Apagar

El dialog deberá mostrar un botón apagar que haga que la alarma deje de sonar, y que su estado pase a ser desactivada

#### Borrar

Junto al botón editar, el botón con el ícono tacho de basura deberá permitir eliminar la alarma

### Función Temporizador

#### Crear

Deberá permitir crear un temporizador de cuenta regresiva indicando una hora en formato `hh:mm:ss`

#### Sonar

El temporizador deberá sonar utilizando las mismas tecnologías que la alarma, en este caso utilizando el archivo `sounds/timer-sound.wav`
El sonido deberá repetirse en loop hasta que el usuario apague la alarma
