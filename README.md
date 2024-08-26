# 2024---TPconsola---G09

Descripción de console.log()

La función console.log() es una herramienta de depuración en JavaScript que se usa para imprimir mensajes en la consola del navegador o en la consola de un entorno de ejecución como Node.js. Es esencial para desarrollar, depurar y monitorear el estado de las aplicaciones.

Parámetros de console.log()

- Parámetro 1: El primer parámetro es el mensaje que deseas imprimir. Puede ser un texto simple (cadena de caracteres), un número, un objeto, un array, etc.
- Parámetro 2 en adelante: Puedes pasar múltiples parámetros a console.log(). Estos se imprimen en la consola en el orden en que se pasan, separados por espacios.

Ejemplos

1. Texto simple:
   console.log("Hola, mundo!");

2. Números:
   console.log(123);

3. Objetos:
   const persona = { nombre: "Juan", edad: 30 };
   console.log(persona);

4. Arrays:
   const numeros = [1, 2, 3, 4];
   console.log(numeros);

5. Múltiples parámetros:
   console.log("Nombre:", "Juan", "Edad:", 30);

Uso en Front-end vs Back-end

Front-end

En el desarrollo front-end (interfaz de usuario), console.log() se utiliza comúnmente para:

1. Depurar eventos: Verificar que los eventos del usuario, como clics o entradas de teclado, se manejan correctamente.
   document.getElementById("miBoton").addEventListener("click", function() {
     console.log("Botón clickeado!");
   });

2. Verificar estados de variables: Ayuda a verificar los valores de las variables y el flujo de ejecución del código.
   let contador = 0;
   function incrementar() {
     contador++;
     console.log("Contador:", contador);
   }

3. Depurar datos de formularios: Verificar la entrada del usuario antes de procesarla.
   function enviarFormulario() {
     const nombre = document.getElementById("nombre").value;
     console.log("Nombre ingresado:", nombre);
   }

Back-end

En el desarrollo back-end (servidor), console.log() se usa para:

1. Depurar rutas y solicitudes: Imprimir detalles de solicitudes HTTP recibidas y respuestas enviadas.
   app.get('/api/usuario', (req, res) => {
     console.log("Solicitud recibida para obtener usuario");
     res.send({ nombre: "Ana", edad: 25 });
   });

2. Monitorear el flujo de datos: Verificar que los datos se procesen correctamente en la lógica del servidor.
   app.post('/api/usuario', (req, res) => {
     console.log("Datos del usuario:", req.body);
     res.status(201).send("Usuario creado");
   });

3. Depurar errores: Identificar errores y excepciones que ocurren en el servidor.
   try {
     // Código que podría lanzar una excepción
   } catch (error) {
     console.log("Error encontrado:", error);
   }

Contenido para Publicar en la Consola

- Estado del Programa: Publica información sobre el estado actual del programa, incluyendo valores de variables y resultados de operaciones. Esto es útil para comprender cómo progresa la aplicación en diferentes puntos.

- Flujo de Información: Muestra cómo los datos se mueven a través del sistema. Por ejemplo, imprimir datos recibidos en una solicitud HTTP y la respuesta generada puede ayudar a verificar el flujo de información entre el cliente y el servidor.

Claro, vamos a investigar algunos métodos del objeto console en JavaScript distintos de console.log. Aquí te explico tres de ellos:

1. console.error()
Descripción: console.error() se utiliza para mostrar mensajes de error en la consola. Es útil para registrar errores que ocurren en el código, ya que generalmente estos mensajes se resaltan en rojo o tienen un formato diferente para destacar su importancia.

Uso:

console.error('Este es un mensaje de error.');
Ejemplo:

Supongamos que estás desarrollando una función que divide dos números y deseas registrar un error si el divisor es cero:

function dividir(dividendo, divisor) {
    if (divisor === 0) {
        console.error('Error: División por cero.');
        return;
    }
    return dividendo / divisor;
}

dividir(10, 0);  // Esto registrará "Error: División por cero."
2. console.warn()
Descripción: console.warn() se utiliza para mostrar advertencias. Estos mensajes suelen aparecer en amarillo en la consola y son útiles para señalar problemas que no son errores críticos pero que podrían necesitar atención.

Uso:

console.warn('Este es un mensaje de advertencia.');
Ejemplo:

Imaginemos que tienes una función que está en desuso:

function funcionAntigua() {
    console.warn('Advertencia: Esta función está obsoleta y será eliminada en futuras versiones.');
}

funcionAntigua();  // Esto registrará "Advertencia: Esta función está obsoleta y será eliminada en futuras versiones."
3. console.table()
Descripción: console.table() permite visualizar datos en formato de tabla. Es muy útil para mostrar arreglos y objetos en una forma tabular, lo que facilita su lectura y análisis.

Uso:

console.table([
    { nombre: 'Juan', edad: 30 },
    { nombre: 'Ana', edad: 25 },
    { nombre: 'Pedro', edad: 35 }
]);
Ejemplo:

Supongamos que tienes un array de objetos que representa una lista de usuarios y quieres visualizarlo en una tabla para facilitar su análisis:

javascript
Copiar código
const usuarios = [
    { id: 1, nombre: 'Alice', edad: 28 },
    { id: 2, nombre: 'Bob', edad: 32 },
    { id: 3, nombre: 'Charlie', edad: 25 }
];

console.table(usuarios);
Este código imprimirá una tabla en la consola con las columnas id, nombre y edad, mostrando los datos de cada usuario de forma clara y ordenada.

Resumen
console.error(): Muestra mensajes de error. Útil para registrar y destacar errores críticos.
console.warn(): Muestra advertencias. Ideal para señalar problemas que requieren atención pero no son críticos.
console.table(): Muestra datos en formato tabular. Facilita la visualización y análisis de arreglos y objetos.
Estos métodos enriquecen la manera en que puedes registrar y visualizar la información en la consola, ayudándote a depurar y entender mejor tu código.
