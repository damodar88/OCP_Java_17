# Capítulo 1: Building Blocks (Fundamentos) #

- Entorno Java: Componentes principales de Java, descarga del JDK.
- Estructura de Clases: Campos, métodos, comentarios (una línea, multilínea, Javadoc).
- main() Method: Firma estándar (public static void main(String[] args)), cómo compilar y ejecutar programas Java.
- Paquetes e Imports: Declaraciones de paquetes, import (con y sin comodines *), conflictos de nombres, java.lang (importación automática), creación de paquetes, compilación y ejecución con paquetes y JARs.
- Orden de Elementos en una Clase: Orden de las declaraciones (package, import, clase).
    - Variables:Tipos Primitivos: Los ocho tipos primitivos de Java (byte, short, int, long, float, double, boolean, char), sus tamaños y rangos. Sufijos para float (f) y long (l).
    - Clases Wrapper: Clases objeto correspondientes a los primitivos (Integer, Boolean, etc.), métodos valueOf(), métodos *Value() (ej., intValue()), pérdida de precisión.
    - Strings: Inmutabilidad, concatenación (+), literales de cadena, bloques de texto (comillas triples """), caracteres de escape (\n, \t, \"), strip(), trim(), indent(), translateEscapes(), String.format() y formatted(), símbolos de formato (%s, %d, %f, %n), banderas de formato.
    - StringBuilder: Mutabilidad, métodos append(), insert(), delete(), reverse().
    - Identificadores: Reglas para nombres de variables, métodos y clases (letras, números, _, $, no pueden empezar con números, no pueden ser _ individualmente, palabras reservadas). 
    - Declaración Múltiple: Declarar múltiples variables del mismo tipo en una sola línea.
    - Inicialización de Variables:Variables Locales: Deben ser inicializadas explícitamente.
    - Variables de Instancia y Clase: Reciben valores por defecto (0 para números, false para booleans, null para referencias).
    - var (Inferencia de Tipo de Variable Local): Solo para variables locales, el tipo es inferido en tiempo de compilación, no cambia en tiempo de ejecución. No se puede usar con parámetros de método, variables de instancia o variables de clase.
    - Alcance de Variables (Scope):Variables Locales: En el ámbito del bloque donde se declaran.
    - Variables de Instancia: Disponibles durante toda la vida del objeto.
    - Variables de Clase (static): Disponibles durante toda la vida del programa.
    - Destrucción de Objetos:Garbage Collection: Proceso automático de liberación de memoria en el heap.
    - Elegibilidad para GC: Un objeto es elegible cuando no tiene referencias apuntando a él o todas sus referencias están fuera de alcance. Distinción entre objeto y referencia.


### Entorno Java: Componentes principales de Java, descarga del JDK. ###

El JDK contiene el software mínimo necesario para el desarrollo en java. Son estos comandos:

 - javac: Convierte los archivos con la extensión .java en .class (bytecode)
 ```javac hola.java```
 - java: Ejecuta el programa
```java hola.class```
 - jar: El .jar se hace con el comando jar o con una herramienta Maven/Gradle
```jar cvf programa.jar *.class```
 - javadoc: Genera la documentación los archivos .html se hace sobre un archivo .java y se suele usar la opción -d para el directorio
```javadoc -d docs Hola.java```
 - JRE: (Java Runtime Environment) Es el entorno de ejecución de Java. Ejecuta aplicaciones java ya compiladas. Incluye:
   - JVM (Java Virtual Machine)
   - Librerías estándar
   - Archivos de configuración necesarios para correr programas.

### Estructura de Clases: Campos, métodos, comentarios (una línea, multilínea, Javadoc). ###



