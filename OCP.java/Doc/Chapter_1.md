# Capítulo 1: Building Blocks (Fundamentos) #

- Entorno Java: Componentes principales de Java, descarga del JDK.
- Estructura de Clases: Campos, métodos, comentarios (una línea, multilínea, Javadoc).
- main() Method: Firma estándar (public static void main(String[] args)), cómo compilar y ejecutar programas Java.
- Paquetes e Imports: Declaraciones de paquetes, import (con y sin comodines *), conflictos de nombres, java.lang 
  (importación automática), creación de paquetes, compilación y ejecución con paquetes y JARs.
- Orden de Elementos en una Clase: Orden de las declaraciones (package, import, clase).
    - Variables:Tipos Primitivos: Los ocho tipos primitivos de Java (byte, short, int, long, float, double, boolean, 
      char), sus tamaños y rangos. Sufijos para float (f) y long (l).
    - Clases Wrapper: Clases objeto correspondientes a los primitivos (Integer, Boolean, etc.), métodos valueOf(), 
      métodos *Value() (ej., intValue()), pérdida de precisión.
    - Strings: Inmutabilidad, concatenación (+), literales de cadena, bloques de texto (comillas triples """), 
      caracteres de escape (\n, \t, \"), strip(), trim(), indent(), translateEscapes(), String.format() y formatted(), 
      símbolos de formato (%s, %d, %f, %n), banderas de formato.
    - StringBuilder: Mutabilidad, métodos append(), insert(), delete(), reverse().
    - Identificadores: Reglas para nombres de variables, métodos y clases (letras, números, _, $, no pueden empezar con 
      números, no pueden ser _ individualmente, palabras reservadas). 
    - Declaración Múltiple: Declarar múltiples variables del mismo tipo en una sola línea.
    - Inicialización de Variables:Variables Locales: Deben ser inicializadas explícitamente.
    - Variables de Instancia y Clase: Reciben valores por defecto (0 para números, false para booleans, null para 
      referencias).
    - Var (Inferencia de Tipo de Variable Local): Solo para variables locales, el tipo es inferido en tiempo de 
      compilación, no cambia en tiempo de ejecución. No se puede usar con parámetros de método, variables de instancia 
      o variables de clase.
    - Alcance de Variables (Scope):Variables Locales: En el ámbito del bloque donde se declaran.
    - Variables de Instancia: Disponibles durante toda la vida del objeto.
    - Variables de Clase (static): Disponibles durante toda la vida del programa.
    - Destrucción de Objetos:Garbage Collection: Proceso automático de liberación de memoria en el heap.
    - Elegibilidad para GC: Un objeto es elegible cuando no tiene referencias apuntando a él o todas sus referencias 
      están fuera de alcance. Distinción entre objeto y referencia.


### Entorno Java: Componentes principales de Java, descarga del JDK. ###

El JDK contiene el software mínimo necesario para el desarrollo en java. Son estos comandos:

 - javac: Convierte los archivos con la extensión .java en .class (bytecode)
 ```javac hola.java```
 - java: Ejecuta el programa
```java hola.class```
 - jar: El .jar se hace con el comando jar o con una herramienta Maven/Gradle
```jar cvf programa.jar *.class```
 - javadoc: Genera la documentación los archivos .html se hace sobre un archivo .java y se suele usar la opción -d para 
el directorio
```javadoc -d docs Hola.java```
 - JRE: (Java Runtime Environment) Es el entorno de ejecución de Java. Ejecuta aplicaciones java ya compiladas. Incluye:
   - JVM (Java Virtual Machine)
   - Librerías estándar
   - Archivos de configuración necesarios para correr programas.

### Estructura de Clases: Campos, métodos, comentarios (una línea, multilínea, Javadoc), clases y archivos fuente. ###

#### Estructura de una clase ####
Las clases son la estructura básica en donde se escribe el código java. Donde se describen todas
Sus partes y características.
Para usar las clases creamos los objetos (Un objeto es una instancia de una clase en tiempo de
de ejecución en memoria) un objeto se crea a partir de una clase la clase es como la plantilla él
Marco para generar diferentes objetos. Estos Objetos se les llama instancia de una clase genere una
Representación de la clase. Una referencia es una variable que apunta un objeto.

##### Campos y métodos #####

##### Comentarios #####
#### Clases y archivos fuente ####


### main() Method ###

La firma del metodo main() es: ```public static void main(String[] args)```es la entrada para que la JVM llame a la 
clase para ejecutar el inicio del programa este es llamados desde afura del programa.
Esta es la explicacion de sus 
partes:

##### Public: #####
Public es un modificador de acceso que se refiere que puede ser llamado desde cualquier parte del programa. En este caso
es estrictamente necesario que sea public ya que la JVM hace el llmado desde fuera del programa al metodo main() de no 
ser public no podria llamar al programa.

##### Static: #####
Static es que el metodo pertenece a la clase y no a una instancia de un objeto. Esto es necesario porque cuando la JVM 
hace el llamado al metodo main() no hay ningun objeto creado ahun y por lo tanto no hay ninguna instancia de la clase.
Por lo que si no es static no podria llamar al metodo main() el llamado a un metodo static es diferente ya que no es 
necesario crear un objeto se hace asi  ```NombreDeLaClase.NombreDelMetodo()``` entonces la JVM busca un metodo public
sin hacer una instancia llamando al metodo por el nombre de la clase.

##### Void: #####
Void es el tipo de dato de retorno de un metodo el void indica que hace una accion sin esperar un retorno de datos.
En este caso igual es necesario ya que la JVM hace el llamado sin esperar un retorno de datos.

##### main(): #####
main() es el nombre del metodo que se llama cuando la JVM ejecutara el programa es necesario ya que busca ese nombre de
metodo para llamarlo. Java es keysencitive diferencia entre mayusculas y minusculas. Entonces tiene que ser en miniscula
para que la JVM pueda encontrarlo.

##### String: #####
String es el tipo de dato que se pasa como argumento al metodo main() es necesario ya que el metodo main() espera un
argumento de tipo String. Tiene que ser de tipo String ya que si es Integer u otro dato no podria pasar datos ya que
serian de otro tipo de datos.

##### []: #####
[] es el arreglo que el metodo contiene como entrada que son de tipo string y parte en 0. Es un arreglo de elementos que
espera como entrada el metodo main(). Este puede variar en String... , String args[].

##### args: #####
args es el nombre de la variable que contiene los argumentos que se pasan al programa que es de tipo String y arreglo,
pero este no es necesario ya que puede ser llamado de cualquier manera no es necesario que sea args. Ya que es solo
el nombre de entrada de los argumentos.

Las partes estrictamente necesarias son: public (es el camino de inicio como encontrar el metodo). Static es la parte de
llamado sin instancia por que la JVM no a creado ningun objeto todavia, void es la parte de retorno el flujo del programa
por lo que es necesario, el nombre de la firma main() tiene que ser ese nombre ya que es lo que busca, String el tipo de 
dato tiene que ser, [] el arreglo tiene que ir pero puede variar en como representarlo y args es el nombre que se puede 
cambiar.

