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
        System.out.println("cadena1 = " + cadena1);
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
