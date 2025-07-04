Documento de Pruebas Funcionales
Proyecto: Aplicación Blazor - Consumo API Rick y Morty



ID del Caso de Prueba: TC-001
Título: Carga y visualización exitosa de personajes de la API de Rick y Morty

Objetivo/Descripción:
Verificar que la aplicación Blazor consume correctamente la API pública de Rick y Morty

Precondiciones:

Acceso a la aplicación Blazor (https://localhost:XXXXX/characters).
Conexión a internet estable para acceder a https://rickandmortyapi.com/api/character.
La API de Rick y Morty debe estar operativa y devolver una respuesta válida.

Pasos de Prueba:
1 Navegar a la página de "Personajes" en la aplicación Blazor (/characters).

2 Esperar a que el indicador de carga (spinner) desaparezca.

3 Verificar que la galería de personajes (grid) se muestra en pantalla.

4 Para al menos un personaje visible, verificar la presencia de:

Imagen del personaje.
Nombre del personaje.
Estado (Vivo, Muerto, Desconocido).
Especie.
Botones "Like" y "Dislike".


Resultado Esperado:

La página de "Personajes" carga exitosamente sin errores.
Se muestra una cuadrícula (grid) con múltiples tarjetas de personajes.
Cada tarjeta de personaje contiene la imagen, nombre, estado y especie del personaje.
Los botones "Like" y "Dislike" son visibles y clickeables para cada personaje.
El puntaje inicial de cada personaje es 0.

Prioridad: Alta
