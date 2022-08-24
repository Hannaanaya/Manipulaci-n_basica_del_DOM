## Variables y operaciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve? 
Espacio disponible en memoria donde se puede guardar un valor.
- ¿Cuál es la diferencia entre declarar e inicializar una variable? 
Cuando se declara una variable, se le da un nombre a la hora de crearla y, al inicializarla, se refiere a que se le asigna un valor.
- ¿Cuál es la diferencia entre sumar números y concatenar strings? 
La suma de números se refiere a la operación matemática de incrementar una cantidad; concatenar strings es enganchar dos o más cadenas de texto para formar una sola.
- ¿Cuál operador me permite sumar o concatenar? +

### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre - string
- Apellido - string
- Nombre de usuario en Platzi - string
- Edad - number
- Correo electrónico - string
- Mayor de edad - booleano
- Dinero ahorrado - number
- Deudas - number

### 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

let name = 'Hanna';
let lastname = 'Anaya';
let username = 'HannaAnaya';
let age = 20
let email = 'hannaanaya0511@gmail.com';
let mayor_edad = true;
let ahorro = 2300;
let deudas = 7;

### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)
- Dinero real (dinero ahorrado menos deudas)

let fullname = name + '' + lastname;
let dineroReal = ahorro - deudas;


## Funciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una función? 
Es la encapsulación de un bloque de código para hacerlas reutilizables en el futuro.
- ¿Cuándo me sirve usar una función en mi código? 
Cuando se quiere llevar a cabo una tarea específica dentro del programa.
- ¿Cuál es la diferencia entre parámetros y argumentos de una función? 
Los parámetros son valores llamados de otras funciones cuando se crean y enviamos argumentos cuando las ejecutamos.

### 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```

´´´
function nombreCompleto(name, lastName) {
    return name + ' ' + lastName
}

function saludo(name, lastname, username) {
    const completeName = nombreCompleto(name, lastname);

    console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + username + ".");  
}
´´´´
## Condicionales

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un condicional? 
Es la forma en que se ejecuta un bloque de código dependiendo de una condición o validación.
- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias? 
if (else, else if), switch
- ¿Puedo combinar funciones y condicionales? 
Sí. Las funciones pueden almacenar cualquier bloque de código, incluyendo condicionales y ciclos.

### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;
}
```


```
if (tipoDeSuscripcion == 'Free') {
       console.log("Solo puedes tomar los cursos gratis");
   } else if (tipoDeSuscripcion == 'Basic') {
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
   } else if (tipoDeSuscripcion == 'Expert') {
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
   } else if (tipoDeSuscripcion == 'ExpertDuo') {
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays y un solo condicional. 😏

```
function conseguirSuscripcion(suscripcion) {
    if (tipoDeSuscripcion == 'Free') {
       console.log("Solo puedes tomar los cursos gratis");
       return;
   } if (tipoDeSuscripcion == 'Basic') {
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       return;
   } if (tipoDeSuscripcion == 'Expert') {
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       return;
   } if (tipoDeSuscripcion == 'ExpertDuo') {
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       return;
   }
   console.log('Este tipo de suscripcion no existe');
}

```

## Ciclos

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un ciclo? 
Es un bucle que se repite hasta cumplir la petición.
- ¿Qué tipos de ciclos existen en JavaScript? 
For, while, do while.
- ¿Qué es un ciclo infinito y por qué es un problema? 
Un ciclo infinito no detiene nunca la ejecución del programa.
- ¿Puedo mezclar ciclos y condicionales? 
Sí

### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}
```

let i = 0;
while (i < 5) {
    console.log("El valor de i es: " + i);
    i++;
}

let i = 10;
while (i >= 2) {
    console.log("El valor de i es: " + i);
    i--;
}
```

### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> 💡 Pista: puedes usar la función prompt de JavaScript.

for (2+2=4) {
    if (r == 4) {
        prompt 'Felicidades';
    } else if {}
    
}

## Listas

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?
Es una lista de elementos
- ¿Qué es un objeto? 
Es un conjunto de elementos con diferentes nombres y valores
- ¿Cuándo es mejor usar objetos o arrays?
Arrays cuando lo que haremos en un elemento, aplicará para otros y objetos para utilizarlos a lo largo del algoritmo.
- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?
Sí. Los arrays pueden guardar objetos y los objetos pueden guardar arrays entre sus elementos.

### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

const array = [1,2,3,4,5,6];

const mifuncion(arr) {
    console.log(arr[1]);
}

### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

const mifuncion(arr) {
    for (let i=0; i < arr.lenght; i++) {
        console.log(array[i]);
    }
}

### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

const mifuncion(obj) {
    const arr = Object.values(obj);
    for (let i=0; i < arr.lenght; i++) {
        console.log(array[i]);
    }
}