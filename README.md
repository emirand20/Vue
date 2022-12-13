# VUE 3 

# 1. Conceptos Basicos

## 1. Programacion Reactiva <br>
Es un PARADIGMA DE PROGRAMACION ASÍNCRONA orientado al FLUJO DE DATOS y PROPAGACION DEL CAMBIO. 
Se compone de tres componentes basicos, OBSERVABLE, METODO QUE AVISA LOS CAMBIOS Y OBSERVER (nosotros como clientes).


## 1.1 Sincrono y Asíncronio <br>
Un código síncrono es aquel código donde cada instrucción espera a la anterior para ejecutarse mientras que un código asíncrono no espera a las instrucciones diferidas y continúa con su ejecución. Por lo general la asincronía permite tener una mejor respuesta en las aplicaciones y reduce el tiempo de espera del cliente.


### Síncrono <br>
Cada instrucción se ejecutará en secuencia hasta terminar.
~~~
console.log('Primero'); 
console.log('Segundo');
console.log('Tercero');
~~~

### Asíncrono <br>
En el caso asícrono, algunas de las instrucciones se ejecutarán a destiempo.
~~~
console.log('Primero');
setTimeout(_ => {
  console.log('Segundo');
},10);
console.log('Tercero');
~~~

## 1.2 Flujo de datos <br>
Son todos aquellos datos cuyas llamadas haran que estos datos cambien gracias a una funcion que estara escuchando.

## 1.3 Propagacion del cambio <br>
No saber cuando van a suceder esos cambios tanto en la vista como en el codigo, cada uno de ellos ha de estar cmunicado.

# Composer API
## Sintaxis de plantilla
VUE utiliza una sintaxis de plantilla basada en HTML que permite vincular declarativamente el DOM.<br>
Todas las platillas de Vue son HTML sintacticas válidas.<br>
Vue compila las plantillas de Js altamente optimizado. <br>
Combiando con al reactividad. Vue es capaz de calcular la cantidad minima de componentes a realizar y aplicar la cantidad minima de manipulaciones en el DOM.
~~~
<template>
    <h1>Hola Vue 3!<h1>
</template>
~~~
## Interpolación de texto
Bigotes es una forma de insertar valores en una plantilla
~~~
<script setup>
const name = "Vue 3"
</script>
<template>
  <h1>{{name}}</h1>
</template>
~~~
## Enlaces de atributos
Los bigotes no se pueden insertar dentro de los atributos HTML. En su lugar utilice una una 'v-bind' para elazar un valor del atributo.
~~~

~~~