README 
Aplicación Blazor - Consumo API Rick y Morty

!Hello work¡

Descripción General del Proyecto
Esta aplicación web fue desarrollada con Blazor WebAssembly. 
Su propósito principal es conectarse a una API pública (la de Rick y Morty) para obtener información de personajes y mostrarlos en pantalla.
Además, permite a los usuarios interactuar con los personajes dándoles "Likes" o "Dislikes"

Instrucciones para Ejecutar la Aplicación

Clonar el Repositorio

Abre la solución (.sln) en visual studio.

Restaurar Paquetes NuGet

Ejecutar la Aplicación
Presiona F5 en Visual Studio

Se abrirá una ventana del navegador con la aplicación.
En el menú lateral (barra de navegación), busca y haz clic en el enlace "Personajes" para ir a la página principal de la aplicación.
Las otras opciones de navegacion son de la plantilla que use y no estan implementadas

Cómo se Consumió la API
Para obtener los datos de los personajes de Rick y Morty, la aplicación se conecta a una API pública.
Con el endpoint Usado: https://rickandmortyapi.com/api/character

Herramienta: Usé HttpClient en el código C# de Blazor. HttpClient es una forma estándar en .NET para hacer solicitudes web.
Proceso: La aplicación hace una solicitud GET a la API. La respuesta que viene de la API está en formato JSON, y Blazor la convierte automáticamente a objetos de C# que la aplicación puede usar.

Estructura del Código
El proyecto está organizado de la siguiente manera:
Program.cs: Este es el archivo principal donde la aplicación Blazor se inicia y se configuran cosas importantes

Pages/Characters.razor: Este es el corazón de la aplicación. Es un componente de Blazor que contiene:
La lógica (código C#) para llamar a la API, manejar los personajes y sus puntajes, y aplicar los filtros.

Shared/NavMenu.razor: Este componente maneja la barra de navegación lateral de la aplicación. Aquí se añadió el enlace para ir a la página de "Personajes".

wwwroot/css/app.css: Este archivo contiene todos los estilos CSS de la aplicación. Aquí se agregaron los estilos para que los personajes se vean en un formato de cuadrícula (grid).

Funcionalidades Adicionales
Además de mostrar los personajes, la aplicación tiene estas funciones:

Votos "Like" y "Dislike": Cada personaje tiene dos botones para dar "Like" o "Dislike". Al hacer clic, se actualiza un contador de "Puntaje" que se muestra debajo de cada personaje.

Puntaje Total de Likes: En la parte superior de la página, se muestra un "Total de Likes en General" que suma solo los puntajes positivos de todos los personajes.


Decisiones Técnicas
Algunas de las decisiones que tomé al construir este proyecto incluyen:

Tipo de Proyecto Blazor: Elegí "Blazor WebAssembly Standalone App" porque permite que la aplicación se ejecute directamente en el navegador del usuario, usando C# para toda la lógica, sin depender de un servidor ASP.NET Core después de la carga inicial.
Consumo de API con HttpClient
Estilos CSS en app.css
Votos No Persistentes: Los "Likes" y "Dislikes" se guardan solo mientras la aplicación está abierta en el navegador. Si cierras la pestaña o reinicias la aplicación, los puntajes vuelven a cero. Esto se hizo para mantener la simplicidad del proyecto, ya que guardar estos datos requeriría una base de datos o almacenamiento local (como localStorage), que no se implementó para este alcance.

Propuesta de mejora:
si tuviera mas tiempo o mas concimiento del consumo y manipulacion de apis me hubiera gustado añadir el filtrado, y que los likes persistan en un tipo de base de datos.
ademas de agregar un estilo mas personalizado si contara con un concimiento mas pleno de css.
tambien me gustaria añadir una paguinacion para poder desplazarme por los personajes de la api, ya que actualmente solo se muestran los primeros 20 personajes.

Muchas gracias por la oportunidad y la atencion prestada!