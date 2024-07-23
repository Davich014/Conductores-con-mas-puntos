# Conductores-con-mas-puntos
Muestra los resultados de los conductores de una competición, como la Fórmula 1, utilizando una tabla para visualizar los datos. A continuación, se explica cada parte del código:

Estructura General
1.- Imports: Se importan las clases necesarias de JavaFX para crear la interfaz gráfica y para manejar conexiones a bases de datos SQL.
2.- Clase Principal: DriversResultsApp extiende Application, lo que significa que es una aplicación JavaFX.

Métodos Principales
start(Stage primaryStage): Este es el método principal que se llama al iniciar la aplicación. Aquí se configura la interfaz de usuario.
BorderPane: Se utiliza un BorderPane como contenedor principal, que permite organizar los elementos en cinco áreas (norte, sur, este, oeste, centro).
Label: Se crea un Label en la parte superior que indica el título "Driver Results".
TableView: Se crea una TableView para mostrar los datos de los conductores. Se añaden varias columnas (TableColumn) que representan diferentes atributos de los resultados de los conductores:
driversStanding
raceId
points
position
positionText
wins
Botones:
Conductor con más puntos: Al hacer clic, este botón filtra la tabla para mostrar solo al conductor con más puntos.
Todos los conductores: Este botón restablece la vista para mostrar todos los conductores.
Estilo de Botones: Ambos botones tienen un estilo CSS que les da un fondo rojo y texto blanco.

Métodos Auxiliares
getDriverWithMostPoints(ObservableList<DriverStanding> driverStandings): Este método itera sobre la lista de conductores y devuelve el que tiene más puntos.
connectToDatabase(): Este método establece una conexión a una base de datos MySQL, ejecuta una consulta para obtener los datos de driverstandings, y llena la lista driverStandings con objetos DriverStanding creados a partir de los resultados.

Clase DriverStanding
Aunque no se muestra en el código, se asume que existe una clase DriverStanding que representa los datos de un conductor, con un constructor que toma los atributos necesarios y métodos para obtenerlos (getters).

Método Main
main(String[] args): Este es el punto de entrada de la aplicación, donde se llama al método launch(args) para iniciar la aplicación JavaFX.


Capturas del codigo ejecutado 
![image](https://github.com/user-attachments/assets/d937af96-a90b-49fa-954b-f43b78eb4bb6)
![image](https://github.com/user-attachments/assets/ef4732cc-b2b1-430d-a16c-0cf839483530)
