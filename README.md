# Curso de Java

Sintaxis para mostrar un hola mundo en JAVA

```java
public class HolaMundo {
    //Agregamos el metodo principal
    public static void main(String[] args) {
        System.out.println("hola mundo perros");
    }
}
```
#### Ejercicio presentarse en java

```java
public class Presentate {
    public static void main(String[] args) {
        System.out.println("Angel G");
        System.out.println("27 años");
        System.out.println("mexico");
    }
}

```
***

## Variables

#### Ejercicio de reserva de hoteles

```java
import java.sql.SQLOutput;

public class ReservaHoteles {
    public static void main(String[] args) {
        /*
        Sistema de reserva de Hoteles

        Captura el detalle de la reservacion de hoteles.

        El detalle que se debe de capturar es:
        - Nombre del cliente
        - Dias de estancia
        - Tarifa diaria
        - Indicar si la habitacion cuenta con vista al mar

        Debe asignar valores iniciales y mandar a imprimir el valor de cada variable.
        Por ultimo se les pide modificar algunos valores de la reservacion y mandar a imprimr nuevamente cada
        variable para observar los cambios
        * */

        System.out.println("*** Reserva de hoteles ***");

        //Definimos variables
        var nombreCliente="Miguel flores";
        var diasEstancia=7;
        var tarifaDiaria=1300;
        var tienesVistaMar=true;

        //Mostramos el detalle de la reserva con soutv (con esto imprimimos las variables)
        System.out.println("nombreCliente = " + nombreCliente);
        System.out.println("diasEstancia = " + diasEstancia);
        System.out.println("tarifaDiaria = " + tarifaDiaria);
        System.out.println("tienesVistaMar = " + tienesVistaMar);

        //Modificando valores
        diasEstancia=4;
        tarifaDiaria=1111;
        tienesVistaMar=false;

        //Nuevos datos de la reservacion
        System.out.println("Nuevos datos de la reservacion");
        System.out.println("nombreCliente = " + nombreCliente);
        System.out.println("diasEstancia = " + diasEstancia);
        System.out.println("tarifaDiaria = " + tarifaDiaria);
        System.out.println("tienesVistaMar = " + tienesVistaMar);
    }
}
```

***
## Cadenas

Manejo de cadenas en JAVA
```java
public class Cadenas {
    public static void main(String[] args) {
        System.out.println("*** Manejo de Cadenas en Java ***");
        var cadena1 = "Hola";
        System.out.println("cadena1 = " + cadena1);
        var cadena2 = new String("Mundo");
        System.out.println("cadena2 = " + cadena2);
        var cadena3 = cadena1 + " " + cadena2;
        System.out.println("cadena3 = " + cadena3);
        // Cadena multiples lineas (text block)       
        var cadena4 = """
                Este es un texto
                multilinea
                mas 
                lineas
                """;
        System.out.println("cadena4 = " + cadena4);
    }
}
```

#### Ejemplo de comparacion de cadenas

```java
public class ComparacionCadenas {
    public static void main(String[] args) {
        // Comparacion de Cadenas (pool de cadenas)
        var cadena1 = "Java";
        var cadena2 = "Java";
        var cadena3 = new String("Java");

        // Comparacion de cadenas (==) comparan la referencia
        System.out.print("cadena1 es igual en referencia a cadena2: ");
        System.out.println(cadena1 == cadena2);
        // Comparamos cadena1 con cadena3 (referencias)
        System.out.print("cadena1 es igual en referencia a cadena3: ");
        System.out.println(cadena1 == cadena3);

        // Comparar contenido usaremos el metodo equals
        System.out.print("cadena1 es igual en contenido a cadena3: ");
        System.out.println(cadena1.equals(cadena3));

    }
}

```

#### Ejemplo de manejo de indices en una cadena 
```java
public class IndicesCadena {
    public static void main(String[] args) {
        // Manejo de índices en una cadena
        var cadena1 = "Hola Mundo";
        // Recuperar el primer caracter
        var primerCaracter = cadena1.charAt(0); // Recuperar el caracter 'H'
        System.out.println("primerCaracter = " + primerCaracter);
        // Recuperar el último caracter (en la posicion 9)
        var ultimoCaracter = cadena1.charAt(9);
        System.out.println("ultimoCaracter = " + ultimoCaracter);
        // imprimir la leta M, indice 5
        var letraM = cadena1.charAt(5);
        System.out.println("letraM = " + letraM);
    }
}
```
#### Inmutabilidad de cadenas

```java
public class InmutabilidadCadenas {
    public static void main(String[] args) {
        //Inmutabilidad de Cadenas
        var cadena1="hola";
        System.out.println("cadena1 = " + cadena1);
        //Si no queremos perder la referencia del objeto anterior,
        //creamos una cadena2 que almacenara la referencia de cadena1
        var cadena2=cadena1;
        cadena1="adios";
        System.out.println("cadena1 modificado = " + cadena1);
        System.out.println("cadena2 = " + cadena2);
    }
}
```

#### Metodos de cadenas
```java
public class MetodosDeCadenas {
    public static void main(String[] args) {
        // Metodo de cadenas
        var cadena1 = "Hola Mundo";

        // Obtener el largo de una cadena
        var longitud = cadena1.length();
        System.out.println("longitud = " + longitud);

        // Reemplazar caracteres
        var nuevaCadena = cadena1.replace('o','a');
        System.out.println("nuevaCadena = " + nuevaCadena);

        // Convertir a mayusculas
        var mayusculas = cadena1.toUpperCase();
        System.out.println("mayusculas = " + mayusculas);

        // Convertir a minusculas
        System.out.println("minusculas = " + cadena1.toLowerCase());

        // Eliminar espacios al inicio y al final
        var cadena2 = " Leo Reyes    ";
        System.out.println("cadena2 con espacios = " + cadena2);
        System.out.println("cadena2 sin espacios = " + cadena2.trim());

    }
}
```

### Manejo de subcadenas en JAVA

```java
public class ManejoSubcadenas {
    public static void main(String[] args) {
        // Tema de subcadenas
        // substring(inicio, fin (sin incluirlo))
        var cadena1 = "Hola Mundo";
        System.out.println("cadena1 = " + cadena1);

        // Subcadena
        var subcadena1 = cadena1.substring(0, 4);
        System.out.println("subcadena1 = " + subcadena1);

        //var subcadena2 = cadena1.substring(5);
        var subcadena2 = cadena1.substring(5, 10);
        System.out.println("subcadena2 = " + subcadena2);

    }
}
```

### Busqueda de subcadenas

```java
public class BusquedaSubcadenas {
    public static void main(String[] args) {
        // Buscar subcadenas
        // indexOf - Devuelve el indice de la primera aparicion de la subcadena
        var cadena1 = "Hola Mundo";
        // subcadena a buscar "Hola"
        var indice1 = cadena1.indexOf("Hola");
        System.out.println("indice1 = " + indice1);
        // lastIndexOf - devuelve el indice de la ultima aparicion de la subcadena
        // subcadena de Mundo
        var indice2 = cadena1.lastIndexOf("Mundo");
        System.out.println("indice2 = " + indice2);
        // subcadena no encontrada devuelve -1
        var indice3 = cadena1.lastIndexOf("Java");
        System.out.println("indice3 = " + indice3);
    }
}
```

### Reemplazar subcadenas

```java
public class ReemplazarSubcadenas {
    public static void main(String[] args) {
        // Reemplazar subcadenas
        var cadena = "Hola Mundo";
        System.out.println("cadena original = " + cadena);

        // Reemplazar "Mundo" por "a todos"
        var nuevaCadena = cadena.replace("Mundo", "a todos");
        System.out.println("nuevaCadena = " + nuevaCadena);

        // Reemplazar "Hola" por "Adios"
        nuevaCadena = cadena.replace("Hola", "Saludos");
        System.out.println("nuevaCadena = " + nuevaCadena);
    }
}

```

### Mas formas de concatenar cadenas

```java
public class MasConcatenacionCadenas {
    public static void main(String[] args) {
        //Mas formas de concatenar cadenas en java
        var cadena1="hola";
        var cadena2="mundo";
        var cadena3= cadena1 + " " + cadena2;
        System.out.println("cadena3 = " + cadena3);

        //Metodo concat
        cadena3=cadena1.concat(" ").concat("Tonotos");
        System.out.println("cadena3 usando concat = " + cadena3);

        //StringBuilder
        var constructorCadenas= new StringBuilder();
        constructorCadenas.append(cadena1);
        constructorCadenas.append(" ");
        constructorCadenas.append(cadena2);
        var resultado=constructorCadenas.toString();
        System.out.println("resultado = " + resultado);

        //StringBuffer
        var stringBuffer= new StringBuffer();
        stringBuffer.append(cadena1).append(" ").append(cadena2);
        resultado=stringBuffer.toString();
        System.out.println("resultado stringbuffer= " + resultado);

        //join
        resultado=String.join(" ", cadena1, cadena2, "tonotos");
        System.out.println("resultado join= " + resultado);
    }
}
```

### Caracteres Especiales en Java

```java
public class CaracteresEspeciales {
    public static void main(String[] args) {
        // Caracteres Especiales
        // '\n' - imprimir un salto de linea
        var cadena1 = "Hola\nMundo";
        System.out.println("cadena1 = " + cadena1);

        // '\t' - tabulador
        var cadena2 = "\tHola\tMundo";
        System.out.println("cadena2 = " + cadena2);

        // '\'' - agrega una comilla simple
        var cadena3 = "Hola \' Mundo";
        System.out.println("cadena3 = " + cadena3);

        // '\"' - agrega una comilla doble
        var cadena4 = "Hola \" Mundo";
        System.out.println("cadena4 = " + cadena4);

        // '\\' - caracter de diagonal invertida
        var cadena5 = "Hola \\ Mundo";
        System.out.println("cadena5 = " + cadena5);

    }
}
```

### Ejercicio para la creacion de emails

![imagen](generadoremail.png "ejercicios")
![imagen](generadoremail2.png "ejercicios")

#### SOLUCION AL EJERCICIO

```java
public class GeneradorEmails {
    public static void main(String[] args) {
        System.out.println("*** Generador de emails ***");
        //Nombre completo del usuario
        var nombreCompleto="Angel Granados Perez";
        System.out.println("nombreCompleto = " + nombreCompleto);

        //Procesar o normalizar el nombre del usuario
        //Limpiar los espacios en blanco al inicio y al final
        var nombreNormalizado=nombreCompleto.strip();
        //Reemplazamos los espacios en blancos por puntos
        nombreNormalizado=nombreNormalizado.replace(" ",".");
        //Convertimos a minusculas el nombre
        nombreNormalizado=nombreNormalizado.toLowerCase();

        //Datos de la empresa
        var nombreEmpresa="Global Mentoriong";
        System.out.println("\nNombre empresa: "+ nombreEmpresa);
        var extensionDominio=".com.mx";

        //Quitamos los espacios en blanco y convertimos a minisculas
        var nombreEmpresaNormalizado=nombreEmpresa.strip().replace(" ",".").toLowerCase();
        var dominioEmailNormalizado="@"+ nombreEmpresaNormalizado + extensionDominio;
        System.out.println("dominioEmailNormalizado = " + dominioEmailNormalizado);
        
        //Creamos el email final
        var emailNormalizado=nombreNormalizado+dominioEmailNormalizado;
        System.out.println("emailNormalizado = " + emailNormalizado);

    }
}
```

## Scanner

Manejo por consola

```java
import java.util.Scanner;

public class ManejoConsola {
    public static void main(String[] args) {
        //Introducir valores por consila
        var consola=new Scanner(System.in);
        System.out.println("escribe tu nombre");
        var nombre=consola.nextLine();
        System.out.print("nombre = " + nombre);
    }
}

```

Leer diferentes tipos de datos
```java
import java.util.Scanner;

public class LeerTiposDatos {
    public static void main(String[] args) {
        // Leer distintos tipos de datos

        // Leer un tipo int
        var consola = new Scanner(System.in);
        System.out.print("Ingresa tu edad: ");
        var edad = consola.nextInt();
        System.out.println("edad = " + edad);

        // Leer un tipo double
        System.out.print("Ingresa tu altura: ");
        var altura = consola.nextDouble();
        System.out.println("altura = " + altura);
        // Consumimos el caracter de salto de linea
        consola.nextLine();

        /*
        Los metodos nextDouble y nextLine no consumen el caracter de salto de linea
        tenemos que consumirlos directamente nosotros antes de consumir el metodo
        nextLine(), NO ES RECOMENDABLE USARLOS  (ARRIBA)
         */


        // Leer un tipo String
        System.out.print("Ingresa tu nombre: ");
        var nombre = consola.nextLine();   //REGESA UNA CADENA
        System.out.println("nombre = " + nombre);

        // Conversion de datos
        System.out.print("Proporciona un valor entero: ");
        /*
         var enteroString = consola.nextLine();
         var entero = Integer.parseInt(enteroString);
        */
        var entero = Integer.parseInt(consola.nextLine());
        System.out.println("entero = " + entero);
        // Tipo flotante
        System.out.print("Proporciona un valor flotante: ");
        var flotante = Float.parseFloat(consola.nextLine());
        System.out.println("flotante = " + flotante);
        //Double.parseDouble()
        //Boolean.parseBoolean()
    }
}
```


***

### Ejercicio: Sistema de Empleados 

![imagen](sistemaempleados.png "ejercicios")

#### SOLUCION AL EJERCICIO

```java
package Java.ManejoConsola.src;

import java.util.Scanner;

public class SistemaEmpleados {
    public static void main(String[] args) {
        System.out.println("*** Sistema de empleados ***");

        var consola=new Scanner(System.in);

        //Nombre del empleado
        System.out.print("Nombre del empleado:  ");
        var nombreEmpleado=consola.nextLine();

        //Edad del empleado
        System.out.print("Edad del empleado: ");
        var edadEmpleado=Integer.parseInt(consola.nextLine());

        //Salario empleado
        System.out.print("Salario empleado: ");
        var salarioEmpleado=Double.parseDouble(consola.nextLine());

        //Es jefe de departamento
        System.out.print("Es jefe de departamenro (true/false)? ");
        var esJefeDepartamento= Boolean.parseBoolean(consola.nextLine());

        //Imprimir los valores del Empleado

        System.out.println("\nDatos del empleado: ");
        System.out.println("\tnombre: "+ nombreEmpleado);
        System.out.println("\tedad: "+edadEmpleado + "Años" );
        System.out.println("\tSalario: $%.2f".formatted(salarioEmpleado));
        System.out.println("\tEs jefe de departamento? "+ esJefeDepartamento);

    }
}
```
***
### Ejercicio: Reto - Proyecto Recetas de Cocina
![imagen](recetascocina.png "ejercicios")
__Resultado del ejercicio__
![imagen](recetascocina2.png "ejercicios")

#### SOLUCION AL EJERCICIO
```java
import java.util.Scanner;

public class RecetasCocina {
    public static void main(String[] args) {
        System.out.println("*** Recetas de Cocina ***");
        var consola = new Scanner(System.in);

        // Nombre de la receta
        System.out.print("Ingresa el nombre de la receta: ");
        var nombreReceta = consola.nextLine();

        // Ingredientes
        System.out.print("Ingresa los ingredientes: ");
        var ingredientes = consola.nextLine();

        // Tiempo de preparación
        System.out.print("Ingresa el tiempo de preparación (min): ");
        var tiempoPreparacion = Integer.parseInt(consola.nextLine());

        // Dificultad de la preperación
        System.out.print("Ingresa la dificultad (Fácil/Medio/Dificil): ");
        var dificultadPreperacion = consola.nextLine();

        // Imprimir los valores de la receta
        System.out.println("\n--- Receta de Cocina ---");
        System.out.println("\tNombre receta: " + nombreReceta);
        System.out.println("\tIngredientes: " + ingredientes);
        System.out.println("\tTiempo de preparación: " + tiempoPreparacion + " minutos");
        System.out.println("\tDificultad: " + dificultadPreperacion);
    }
}

```

***
## Números Aleatorios (Random)

```java
package Java.ManejoConsola.src;

import java.util.Random;

public class NumerosAleatorios {
    public static void main(String[] args) {
        System.out.println("*** Números Aleatorios ***");
        var random = new Random();

        // Generar un numero aleatorio entre 0 y 9
        var numeroAleatorio = random.nextInt(10);
        System.out.println("numeroAleatorio entre 0 y 9 = " + numeroAleatorio);

        // Generar un numero aleatorio entre 1 y 10
        numeroAleatorio = random.nextInt(10) + 1;
        System.out.println("numeroAleatorio entre 1 y 10 = " + numeroAleatorio);

        // Generar un numero flotante entre 0.0 y 1.0
        var flotanteAleatorio = random.nextFloat();
        System.out.println("flotanteAleatorio = " + flotanteAleatorio);

        // Simular el lanzamiento de un dado (1 y 6)
        var dado = random.nextInt(6) + 1;
        System.out.println("Resultado de lanzar el dado = " + dado);
    }
}

```