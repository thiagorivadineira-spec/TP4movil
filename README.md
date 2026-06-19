# TP4movil
Proyecto .NET MAUI (Blazor) para consumir una API REST la cual (target .NET 9) agregar,modificar, obtener y eliminar productos mediante una api falsa(fakestoreapi.com por defecto).

requisitos
- .NET 9 SDK
- Visual Studio 2022 con ".NET MAUI" instalada


TodoProductos
  - Ruta: /todoproductos
  - Archivo: TP4movil/Components/Pages/Todoproductos.razor
  - Descripción: Muestra la lista de productos en tarjetas las cuales tienen sus            respectivos botones para eliminar,modificar y ver sus detalles.
  - Endpoint https://fakestoreapi.com/
	- GET products que recupera todos los productos de la api
	- DELETE products/{id} dependiendo en que producto se ubique se elimina

Crearproducto
  - Ruta: /crearproducto
  - Archivo: TP4movil/Components/Pages/Crearproducto.razor
  - Descripción: muestra un formulario para crear un nuevo producto
  - Endpoint https://fakestoreapi.com/
	- POST products crea un nuevo producto en formato json

EditarProducto
  - Ruta: /editarproducto/{id:int}
  - Archivo: TP4movil/Components/Pages/EditarProducto.razor
  - Descripción:sirve para editar un producto mediante id.
  - Endpoint https://fakestoreapi.com/
	- GET products/{id} el cual recupera un producto por su id
	- PUT products/{id} el cual modifica y actualiza un producto mediante id y lo devuelve en json

DetallesProducto
  - Ruta: /verproducto/{id:int}
  - Archivo: TP4movil/Components/Pages/VerProducto.razor
  - Descripción: muestra un producto por su id
  - Endpoint https://fakestoreapi.com/
	- GET products/{id} el cual recupera un producto por su id

Modelos
- Todo (TPmovil/Models/Todo.cs)
  - id: int
  - title: string (required)
  - price: float (required)
  - description: string
  - category: string
  - image: string
 
Su ejecucuion
  -copie el repositorio o instala y abra el proyecto
  -restaura sus dependencias (dotnet restore)
  -compile (dotnet build -c Debug)
  -Luego ejecute en visual studio2022 (muy probablemente tengas que usar  dotnet workload restore para restaurar el proyecto)
  -luego inicie el proyecto
