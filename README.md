# 5 Consejos para Escribir un Código Limpio y Mantenible

## Introducción

Escribir un código limpio es crucial para que otros desarrolladores (y tú mismo en el futuro) lo entiendan y mantengan. Hoy te comparto 5 consejos clave para mejorar la legibilidad y mantenibilidad de tu código.

## Tabla de contenidos

- [Nombres descriptivos](#nombres-descriptivos)
- [Funciones pequeñas](#funciones-pequeñas)
- [Documenta lo necesario](#documenta-lo-necesario)
- [Evita los valores mágicos](#evita-los-valores-magicos)
- [Formatea consistentemente](#formatea-consistentemente)
- [License](#license)
- [Contact](#contact)

## Nombres descriptivos

Usar nombres claros y descriptivos para variables, funciones y clases mejora la legibilidad del código. Cuando alguien más (o tú mismo en el futuro) lea el código, no tendrá que deducir qué significa cada nombre.

### Ventajas:

- Facilita la comprensión del propósito del código.

- Reduce la necesidad de comentarios excesivos o documentación adicional.

- Minimiza errores al trabajar en equipo, ya que todos pueden entender rápidamente qué hace cada parte del código.

### No hacer

```js
let j; // Nombre del jugador
```

### Hacer

```js
let nombreDelJugador;
```

## Funciones pequeñas

Las funciones pequeñas hacen que el código sea más modular, permitiendo enfocarse en tareas específicas. Una función debería hacer solo una cosa, y hacerlo bien (principio de responsabilidad única).

### Ventajas:

- Facilita la reutilización del código, ya que las funciones son independientes.

- Hace que las pruebas unitarias sean más sencillas, ya que cada función tiene un propósito específico.

- Si una función es pequeña, es más fácil identificar y corregir errores.

### No hacer

```js
function hacerReservaCompleta() {
    // Código necesario para validar los datos de la reserva
    // Código necesario para crear la reserva
}
```

### Hacer

```js
function validarReserva() {
    // Código necesario para validar los datos de la reserva
}

function crearReserva() {
    // Código necesario para crear la reserva
}
```

## Documenta lo necesario

Escribir documentación excesiva puede ser tan malo como no documentar. Es importante que la documentación sea clara y concisa, enfocándose en lo que no es obvio en el código. Los comentarios deben explicar el "por qué" detrás de las decisiones, no el "qué", que debería ser evidente por la legibilidad del código.

### Ventajas:

- Evita la redundancia innecesaria.

- La documentación bien escrita facilita el mantenimiento, ya que explica el propósito y la lógica detrás de la implementación.

- Reduce la carga cognitiva de leer código complejo sin contexto adicional.

### No hacer

```js
let index = 0;
// Incrementar 1 el índice
index++;
```

### Hacer

```js
let index = 0;
// Incrementar la posición para situarnos en la siguiente tarifa
index++;
```

## Evita los valores mágicos

Un "valor mágico" es un número o cadena que aparece directamente en el código sin explicación. Reemplazarlos con constantes con nombres descriptivos hace que el código sea más fácil de entender y modificar.

### Ventajas:

- Hace que el código sea más legible y autodescriptivo.

- Facilita los cambios en el futuro. Si ese valor necesita cambiar, solo se modifica en un lugar.

- Reduce la posibilidad de cometer errores al reutilizar esos valores en varias partes del código.

### No hacer

```js
if (tiempo < 60) {}
```

### Hacer

```js
const SEGUNDOS_POR_MINUTO = 60;
if (tiempo < SEGUNDOS_POR_MINUTO) {}
```

## Formatea consistentemente

Mantener un estilo de formato uniforme (uso de espacios, indentación, llaves, etc.) hace que el código sea más fácil de leer y comprender para todos los miembros del equipo. Herramientas como linters y formateadores automáticos pueden ayudar en esto.

### Ventajas:

- Mejora la legibilidad general, haciendo que sea más fácil detectar errores visualmente.

- Facilita el trabajo en equipo, ya que todos siguen el mismo estándar.

- Reduce la posibilidad de errores relacionados con una estructura inconsistente.

### No hacer

```js
class Reserva() { function hacerReserva() {} }
```

### Hacer

```js
class Reserva() {
    function hacerReserva() {
// Código necesario para crear la reserva
    }
}
```

## License

This project is licensed under the MIT License. For more details, see [LICENSE](https://github.com/CompilandoYT/20240914-5-Consejos-Codigo-Limpio/blob/main/LICENSE)

## Contact