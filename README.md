README 
Aplicaci�n Blazor - Consumo API Rick y Morty

!Hello work�

Descripci�n General del Proyecto
Esta aplicaci�n web fue desarrollada con Blazor WebAssembly. 
Su prop�sito principal es conectarse a una API p�blica (la de Rick y Morty) para obtener informaci�n de personajes y mostrarlos en pantalla.
Adem�s, permite a los usuarios interactuar con los personajes d�ndoles "Likes" o "Dislikes"

Instrucciones para Ejecutar la Aplicaci�n

Clonar el Repositorio

Abre la soluci�n (.sln) en visual studio.

Restaurar Paquetes NuGet

Ejecutar la Aplicaci�n
Presiona F5 en Visual Studio

Se abrir� una ventana del navegador con la aplicaci�n.
En el men� lateral (barra de navegaci�n), busca y haz clic en el enlace "Personajes" para ir a la p�gina principal de la aplicaci�n.
Las otras opciones de navegacion son de la plantilla que use y no estan implementadas

C�mo se Consumi� la API
Para obtener los datos de los personajes de Rick y Morty, la aplicaci�n se conecta a una API p�blica.
Con el endpoint Usado: https://rickandmortyapi.com/api/character

Herramienta: Us� HttpClient en el c�digo C# de Blazor. HttpClient es una forma est�ndar en .NET para hacer solicitudes web.
Proceso: La aplicaci�n hace una solicitud GET a la API. La respuesta que viene de la API est� en formato JSON, y Blazor la convierte autom�ticamente a objetos de C# que la aplicaci�n puede usar.

Estructura del C�digo
El proyecto est� organizado de la siguiente manera:
Program.cs: Este es el archivo principal donde la aplicaci�n Blazor se inicia y se configuran cosas importantes

Pages/Characters.razor: Este es el coraz�n de la aplicaci�n. Es un componente de Blazor que contiene:
La l�gica (c�digo C#) para llamar a la API, manejar los personajes y sus puntajes, y aplicar los filtros.

Shared/NavMenu.razor: Este componente maneja la barra de navegaci�n lateral de la aplicaci�n. Aqu� se a�adi� el enlace para ir a la p�gina de "Personajes".

wwwroot/css/app.css: Este archivo contiene todos los estilos CSS de la aplicaci�n. Aqu� se agregaron los estilos para que los personajes se vean en un formato de cuadr�cula (grid).

Funcionalidades Adicionales
Adem�s de mostrar los personajes, la aplicaci�n tiene estas funciones:

Votos "Like" y "Dislike": Cada personaje tiene dos botones para dar "Like" o "Dislike". Al hacer clic, se actualiza un contador de "Puntaje" que se muestra debajo de cada personaje.

Puntaje Total de Likes: En la parte superior de la p�gina, se muestra un "Total de Likes en General" que suma solo los puntajes positivos de todos los personajes.


Decisiones T�cnicas
Algunas de las decisiones que tom� al construir este proyecto incluyen:

Tipo de Proyecto Blazor: Eleg� "Blazor WebAssembly Standalone App" porque permite que la aplicaci�n se ejecute directamente en el navegador del usuario, usando C# para toda la l�gica, sin depender de un servidor ASP.NET Core despu�s de la carga inicial.
Consumo de API con HttpClient
Estilos CSS en app.css
Votos No Persistentes: Los "Likes" y "Dislikes" se guardan solo mientras la aplicaci�n est� abierta en el navegador. Si cierras la pesta�a o reinicias la aplicaci�n, los puntajes vuelven a cero. Esto se hizo para mantener la simplicidad del proyecto, ya que guardar estos datos requerir�a una base de datos o almacenamiento local (como localStorage), que no se implement� para este alcance.

Propuesta de mejora:
si tuviera mas tiempo o mas concimiento del consumo y manipulacion de apis me hubiera gustado a�adir el filtrado, y que los likes persistan en un tipo de base de datos.
ademas de agregar un estilo mas personalizado si contara con un concimiento mas pleno de css.
tambien me gustaria a�adir una paguinacion para poder desplazarme por los personajes de la api, ya que actualmente solo se muestran los primeros 20 personajes.

Muchas gracias por la oportunidad y la atencion prestada!