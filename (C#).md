---
favorited: true
title: '(C#)'
created: '2023-11-21T11:31:08.984Z'
modified: '2024-01-28T04:49:34.267Z'
---

 

# (C#)
--------------

[//]: # (version: 1.0)
[//]: # (author: Izan Abramovici Cabrera)
[//]: # (date: 2023-11-21)

 
   
# Indice
- [(C#)](#c)
- [Indice](#indice)
  - [Introducción](#introducción)
  - [Instalación del IDE](#instalación-del-ide)
    - [Windows:](#windows)
    - [Linux:](#linux)
  - [Creacion del primer proyecto](#creacion-del-primer-proyecto)
    - [Windows](#windows-1)
      - [Correr el código](#correr-el-código)
    - [Linux](#linux-1)
      - [Correr el código](#correr-el-código-1)
  - [Sintaxis básica](#sintaxis-básica)
    - [Buenas Prácticas](#buenas-prácticas)
    - [1. Comentarios](#1-comentarios)
    - [2. Identificadores](#2-identificadores)
    - [3. Tipos de datos](#3-tipos-de-datos)
    - [4. Variables](#4-variables)
    - [5. Constantes](#5-constantes)
    - [6. Booleanos](#6-booleanos)
    - [7. Arrays](#7-arrays)
    - [8. Operadores](#8-operadores)
      - [8.1 Operadores aritméticos](#81-operadores-aritméticos)
      - [8.2 Operadores de comparación](#82-operadores-de-comparación)
      - [8.3 Operadores lógicos](#83-operadores-lógicos)
      - [8.4 Operadores lógicos a nivel de bit](#84-operadores-lógicos-a-nivel-de-bit)
    - [9. Transformar variables](#9-transformar-variables)
    - [10 Estructuras de contol de flujo](#10-estructuras-de-contol-de-flujo)
      - [10.1 Condicional **if**](#101-condicional-if)
      - [10.2 Ternarios](#102-ternarios)
      - [10.3 Condicional switch](#103-condicional-switch)
      - [10.4 Blucles](#104-blucles)
        - [ 10.4.1 While ](#-1041-while-)
        - [ 10.4.2 Do-While ](#-1042-do-while-)
        - [ 10.4.3 For ](#-1043-for-)
      - [Ejercicio](#ejercicio)
    - [11. Excepciones](#11-excepciones)
  - [Estructura básica](#estructura-básica)
    - [1. Espacios de Nombres (namespace):](#1-espacios-de-nombres-namespace)
      - [2. Alias](#2-alias)
      - [3. Clases (class)](#3-clases-class)
        - [1. Campos (field):](#1-campos-field)
        - [ 2. Métodos (method): ](#-2-métodos-method-)
          - [ Return ](#-return-)
  - [Programación orientada a objetos (POO) ](#programación-orientada-a-objetos-poo-)
    - [Modificadores de acceso](#modificadores-de-acceso)
    - [1. Creación de Objetos](#1-creación-de-objetos)
    - [2. Constructores](#2-constructores)
      - [2.1 Setters y Getters](#21-setters-y-getters)
      - [2.2 Sobrecarga](#22-sobrecarga)
      - [2.3 this.](#23-this)
    - [3. Math](#3-math)
    - [Ejemplo usando todo](#ejemplo-usando-todo)
    - [Herencia](#herencia)
  - [BBDD (Bases de datos)](#bbdd-bases-de-datos)
    - [1. Instalación](#1-instalación)
    - [2. Base de datos](#2-base-de-datos)
      - [2.1 Creacion base de datos](#21-creacion-base-de-datos)
      - [2.2 Insercion de datos](#22-insercion-de-datos)
    - [3. Creacion del proyecto](#3-creacion-del-proyecto)
    - [4. Crear la conexion](#4-crear-la-conexion)
    - [5. Crear las propiedas](#5-crear-las-propiedas)
    - [6. Diseño dl Formulario](#6-diseño-dl-formulario)
    - [7. Select de MySql](#7-select-de-mysql)
    - [8. Mostrar datos select](#8-mostrar-datos-select)
    - [9. Añadir registro](#9-añadir-registro)
        
<div style="page-break-after: always;"></div>
         
     
## Introducción
[Indice](#c)

1. ¿Qué es C#?
 - C# Es un lenguaje de programación desarrollado por Microsoft, es una evolución de C y C++, su objetivo es permitir a los desarroladores crear aplicaciones ejecutadas en .NET Framework
    - Caracterisiticas: 

         1. Es un lenguaje orientado a objetos (clases, herencia, polimorfismo y encapsulamiento)
         2. Su sintaxis es sencilla y facil de aprender, siendo parecidas a las de C y C++
         3.  Integración con otros lenguajes, por ejemplo:
              - F#
              - C++/CLI
              - IronPython
              - IronRuby
              - JavaScript (a través de TypeScript)
              - Powershell (No es un lenguaje pero puede interactuar con y consumir bibliotecas escritas en C# y otros lenguajes de .NET.)
              - SQL Server
         4. C# puedes divir el código en múltiples hilos de ejecución y trabajar en paralelo (mejorar el rendimiento y la capacidad de respuesta de una aplicación)

## Instalación del IDE
[Índice](#c)  

1. deberemos de usar un IDE (Integrated Development Environment o, lo que es lo mismo, Entorno de Desarrollo Integrado), usaremos Visual Studio para windows y visual studio code para linux, deberemos seguir los siguientes pasos:
### Windows:
 1. Enlace de descarga para el visual studio community: https://visualstudio.microsoft.com/es/thank-you-downloading-visual-studio/?sku=Community&channel=Release&version=VS2022&source=VSLandingPage&cid=2030&passive=false

 2. Instalamos haciendo doble click 
 
 3. Nos apareceran varios recuadros, tendremos que elegir .NET desktop developement (un monitor con un cuadrado morado que pone .NET arriba a la izquierda)
          
 4. Clickamos instalar

 5. Iniciamos sesisón con Microsoft

 6. Inciar proyecto
  
-------------
 
### Linux:
  1. Debemos instalar visual studio code, haremos lo siguiente:

  - Recursos:

    - https://ubunlog.com/visual-studio-code-editor-codigo-abierto-ubuntu-20-04/

  - Instalación por consola:

```console
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt install code
```

  2. Instalaremos dotnet-sdk:

   Recursos:
  
   -  https://learn.microsoft.com/en-us/dotnet/core/install/linux
  ```console
  Si no hiciste el paso anterior, haz el "sudo apt update"

  sudo apt-get install -y dotnet-sdk-7.0

  dotnet --version (para comprobar que version se ha instalado)
  ```
  3. Inciaremos Visual Studio Code y buscaremos en la parte izquierda las pestaña de extensiones (4 cuadrados y el de arriba a la derecha esta separado del resto)

  4. Cuando estemos en las extensiones buscaremos "C# Dev Kit" y clicakremos [Instalar]
 
## Creacion del primer proyecto
[Indice](#c)

### Windows 
  1. Abrimos Visual Studio

  2. Seleccionamos la opcion [Crear un proyecto]

  3. Nos aparecerá una lista de todas las plantillas que podemos usar, elegimos "aplicación de consola"

  4. Ahora deberemos de poner el nombre de nuestro proyecto y elegir donde queremos que se guarde

  5. En mi caso lo llamaré Prueba01 y lo guardaré en "C:\Users\Izan\Documents\C#"

  6. Ahora deberemos de elegir el farmework, yo selecciono el ".NET 8.0"

  7. Ya se nos ha abierto el proyecto, deberia de salirnos algo así:
  ```C#
  // See https://aka.ms/new-console-template for more information
Console.WriteLine("Hello, World!");
  ```
  #### Correr el código

  1. Arriba se pueden ver 2 botones de una flecha verde, uno con el nombre del proyecto y otro sin nada
      - El que tiene nombre depura nuestro código antes de mostrarnos el resultado
      - El que no tiene nobre nos muestra el resusltado sin depurar 
      (Más tarde explicaré la diferencia)
    
  2. Pulsamos cualquiera de los 2, se nos abrirá una ventana de cmd con el siguiente contenido:
  ```console
  Hello, World!

C:\Users\Izan\Documents\C#\Prueba01\Prueba01\bin\Debug\net8.0\Prueba01.exe (proceso 19688) se cerró con el código 0.
Presione cualquier tecla para cerrar esta ventana. . .
  ``` 
  Ha hecho exactamente lo que el código pedia, imprimir en una consola la frase "Hello, World!"

-------------

### Linux

  1. Crearemos una carpeta donde vayamos a guardar nuestros proyectos, por ejemplo:
  ```console
  mkdir Documentos/proyectos-C-sharp
  ```
  2. Abriremos visual studio code

  3. En las opciones de arriba seleccionaremos [Terminal] y clickaremos [Nuevo Terminal]

  4. En la parte baja nos saldra un terminal, haremos lo siguiente:
  ```console
  cd (para asegurarnos que estamos en la raiz)

  cd Documentos/proyectos-C-sharp (abrimos la carpeta donde estaran nuestros proyectos)
  
  mkdir Proyecto01 (Creamos una carpeta para nuestro primer proyecto)
  
  dotnet new console 
  
  (Con este comando crearemos nuestro primer proyecto, en caso de terner mas de una version de dotnet 
  especifiaremos la versió del mismo poniendo al final --framework net(version que se queire usar pj: net7.0))

  code . (abriremos el directorio donde se encuentra el proyecto para que podamos trabajar)
  
  ```
  Si cerraste visual studio code y no está el proyecto, clicka en [Archivo] > [Agregar carpeta al área de trabajo...] > selecciona la carpeta donde tengas tus proyectos.

  Se te debieron crear 1 carpeta y 2 archivos, una carpeta de nombre "OBJ" y 2 archivos con nombre "(nombre de la carpeta del proyecto).csproj" y "Program.cs"

  5. Listo, ya tienes tu primer proyecto creado, ahora hace falta hacerlo funcionar
 
#### Correr el código
  [Indice](#c)
   
1. Abriremos una nueva terminal como hicimos previamente

2. Nos aseguramos que estamos en la carpeta del proyecto

3. Escribimos lo siguiente:
    ```console 
    dotnet run 
    ```
    Nos deberia dar el siguiente resusltado
   ```console
    dotnet run
    Hello, World!
   ```
-------------  
## Sintaxis básica
Lo minimo que debemos de tener en nuestro proyecto de c# y lo que vamos a usar en los siguientes ejemplos es:
```csharp
namespace NombreQueQueramos
{
    class NombreQueQueramos
    {
        static void Main()
        {
          //Código
        }
    }
}
```
 
[Indice](#c)  
- SIEMPRE hay que poner ; después de añadir una línea de código. 
- SIEMPRE hay que definir un Main estático.
- Es caseSensitive : distingue entre mayúsculas y minisculas.
- C# subraya en verde para las advertencias y rojo para los errores en sintaxis
- Lee el código de arriba a abajo siempre y cuando no tenga POO (programación orientada a objetos)
### Buenas Prácticas
- Usar camelCase/Snake/PascalCase
```csharp
//camelCase
namespace pruebaDocumento {}
//snake
namespace prueba_documento {}
//PascalCase
namespace PruebaDocumento {}
```
- Seguir convenciones de nomenglatura para mejorar la legibilidad, por ejemplo, usar PascalCase para nombres de clase y camelCase para nombres de variables y métodos.
- Dejar una linea en blanco para cada "{}"
- Tabular cada vez que haya otro nivel inferior (indentación)
```csharp
namespace prueba_nombre
{
    class PruebaMenor
    { 
        void pruebaMetodo()
        {
          //Codigo
        }
    }
}
```
- Usar comentarios
  
-------------
 
### 1. Comentarios
[Indice](#c) 
<br>
```csharp
// Esto es un comentario de una linea

/*
 Esto es un comentario
 Multilinea
*/
```
Los comentarios en C# son anotaciones en el código que se utilizan para proporcionar información adicional. No afectan la ejecución del programa y son útiles para la documentación, explicación y comprensión del código fuente.

>[!Note]
>Una práctica entre lo programadores es poner comentarios tal que así
>```csharp
>// TODO: --Continuar o no terminado
>```
>Sirve para recoradarte a ti u a otra persona donde seguir el código o si algo está terminado o no.
>Estos comentarios Visual Studio los guarda en "Lista de tareas" para poder ir rápido al archivo y linea donde se encuentra.


### 2. Identificadores
[Indice](#c) 
<br>
  Un identificador en programación es un nombre que se utiliza para identificar una función, clase u otro elemento en el código fuente. Los identificadores son etiquetas que asignamos a elementos (Namespaces, clases, métodos...) del programa para referirnos a ellos y manipularlos en el código.
    - Solo se pueden usar letras, numeros y guiones bajos
    - Debe de comenzar por una letra o un guión bajo
    - No usar palabras reservadas por el sistema (Son las que aparecen en azul, como class, void, namespace, etc.)

### 3. Tipos de datos
[Indice](#c) 
<br>
Tipos: 
  - Por referencia
  - Por valor
    - Primitivos
      - Enteros
      - Reales
      - Booleanos
    - [Enumerados](#enum)
    - [Estructurados](#struct)

>[!NOTE]
>Se va a hacer una pequeña explicacion de cada tipo lo minimo para entenderlo pero por ahora no entraremos en detalles más especificos

 1. Por referencia
    A la hora de almacenar estos datos, almacenamos una dirección en la memoria de ese tipo por la referencia   

 2. Por valor
    Son aquellos que maneja el procesador y se almacenan en una variable

  - 3. Primitivos
      Son los más importantes y a su vez los más básicos los cuales se dividen en enteros, reales y boolenaos.
        - Enteros: Valores sin decimales
        - Reales: Valores con decimales
        - Booleanos: Condiciones lógicas (True/False)
      Dentro de los Enteros encontrados dos tipos:
        - Sin signo: Puede ser tanto positivo como negativo
          - byte: 0 a 255 
          - ushort: 0 a 65.535
          - uint: 0 a 4.294,967.295
          - ulong: 0 a 18,446,744,073,709,551,615
        - Con signo: Pueden ser tanto positivos como negativos
          - sbyte: -128 a 127
          - short: -32,768 a 32,767
          - int: -2,147,483,648 a 2,147,483,647
          - long: -9,223,372,036,854,775,808 a 9,223,372,036,854,775,807
       Dentro de los Reales encontramos:
        - Float: 6-9 digitos de precisión total
        - Double: 15-17 dígitos de precisión total
        - Decimal: 28-29 dígitos de precisión total   
>[!Caution]
>Para flotar y decimal es aconsejable poner f y m respectivamente al finalizar la declaracion de la variable:
>```csharp
>float NumeroFloat = 23.543f;
>decimal NumeroDecimal = 2415.1325234m;
>```
>Esto es porque de manera predeterminada c# pone los decimales como double, no es estrictamente necesario ponerlos pero si queremos almacenar un número que aun no tenga decimales, es mejor especificarlo.   
  - Tipos de datos más usados
    - int: 32 bits
    - long: 64 bits
    - float: 32 bits
    - double: 64 bits
    - decimal: 128 bits
    - char: Para carácteres sueltos (Seria un 4 grupo de los primitivos llamado "utf16") 16 bits
    - String: Es una cadena de chars (es de tipo por referencia): 16bits por carácter
    - bool (booleano): 8 bits
>[!Note]
>La cantidad en bits hace referencia al espacio que ocupa en la RAM  
 
 ### 4. Variables
[Indice](#c) 
<br>
¿Que és?: Una variable es un espacio en la memoria RAM donde se almacenará un valor que podrá cambiar durante la ejecución del programa

Buenas prácticas al definir una variable:
- No comenzar el nombre de la variable con un guion bajo
- No crear mas de una variable que se diferencien solo por una letra
- Comenzar el nombre de la variable con letra minúscula
- Si el nombre de la variable está compuesto por más de una palabra,
comenzar la segunda con mayúscula (camelCase).
- No usar la notación húngara (nombrar variables y funciones que incluye información sobre el tipo ej: int = iEdad)

<h3>4.1 Declarar una variable </h3>  

```csharp
// [Tipo de dato] [Nombre De la Variable]
int edadDelAlumno;
//Con esto nuestro programa ha reservado un espacio de 32 bits en la ram y ahora podremos usar edadDelAlumno en nuestro porgrama
//se pueden declarar varias variables a la vez
int edadDelAlumno1, edadDelAlumno2, edadDelAlumno3, edadDelAlumno4;
```   

  <h3>4.2 Inciar una variable </h3>   

```csharp
//[Nombre De la Variable] = [Valor]
edadDelAlumno = 10;
//Con esto nuestro programa ha especificado que edadDelAlumno tiene un valor de 10
//No se pueden iniciar varias variables a la vez
edadDelAlumno1, edadDelAlumno2, edadDelAlumno3, edadDelAlumno4 = 27;
//esto lo unico que hará es inciar la ultima variable
```   

  Existe la posibilidad de hacer los dos pasos anteriores a la vez
```csharp
int edadDelAlumno = 10;
string nombreAlumno = "Juan";
//Si hacemos lo siguiente
int edadDelAlumno1, edadDelAlumno2, edadDelAlumno3, edadDelAlumno4 = 27;
//Se crearan las 3 primeras variables y la ulitma se creará e iniciará
```
>[!Caution]
>En C# no puedes usar una variable que no se haya iniciado.   

<h3>4.3 Ejemplo de uso</h3>   

```csharp
namespace prueba_variable
{
    class PruebaVariable
    {
        static void main()
        {
          int edadDelAlumno;
          edadDelAlumno = 11;
          int edadDelAlumno2 = 10;
          System.Console.WriteLine(edadDelAlumno);
          System.Console.WriteLine(edadDelAlumno2);
        }
    }
}
```
 
>[!Note]
>Existe una palbra clave llamada "var" se utiliza para declarar variables con inferencia de tipo. Cuando usas var para declarar una variable, >el compilador determina automáticamente el tipo de la variable basándose en el tipo de la expresión de inicialización. El tipo de la variable se determina en tiempo de compilación y no cambia durante la ejecución del programa. (Yo no recomendaría usarlo).
```csharp
var numero = 10; // El compilador infiere que 'numero' es de tipo int.
var nombre = "Juan"; // El compilador infiere que 'nombre' es de tipo string.
var pi = 3.14; // El compilador infiere que 'pi' es de tipo double.
```

### 5. Constantes
[Indice](#c) 
<br>
Una constante es simplemente un variable que no vamos a poder cambiar durante todo el código.   

Una buena práctica es poner las constantes en mayúsculas
```csharp
const int PI = 3.1416;
const int ESPACIO_CLASES = 30;
//Las constantes funcionan exactamente igual que una variable
```
### 6. Booleanos
[Indice](#c) 
Un booleano es una constante que puede tener 2 valores, **"true"**(verdadero) y **"false"**(falaso)

```csharp
bool haceCalor;
haceCalor = false;

//Podemos usar el simbolo ! para darle el valor contrario
Console.WriteLine(!haceCalor)
//Esto hará que nos salga "True" por consola
```

### 7. Arrays
[Indice](#c)
- ¿Qué es? Estructura de datos que contiene una colección de valores del mismo tipo.
- ¿Para qué? Para almacenar valores que normalmente tienen alguna relación entre sí.

>[!Note]
>La primera posición de un array es siempre 0
- Sintaxis:
    Hay 3 formas de escribir un array   

- Forma restrictiva:

El array solo admite un número especifico de valores que vamos a especificar

```csharp
//Declaración:
"variable"[] nombre_de_la_matriz;
int[] mi_matriz;
//Iniciación:
mi_matriz=new int[4]; //El 4 hace referencia a la cantidad de valores que vas a insertar.
mi_matriz[0] = 3
mi_matriz[1] = 9
mi_matriz[2] = 1
mi_matriz[3] = 3 

//En este caso usamos valores numéricos puesto que he usado int

//Declaración e iniciación en la misma línea: 
int[] mi_matriz=new int[4];
//tambien podemos hacer
int[] mi_matriz=new int[4]{1,5,3,9};
```
- Forma fexlible:
Al iniciar la matriz insertaremos la cantidad que queramos.
Esto se entiende mejor de la siguiente manera. Ej:
Imaginemos que tenemos un programa que deja al usuario elegir todos los numeros que quiera, el ususario puede elegir tanto 2 numeros como 100, como no sabemos la cantidad, no le decimos a la matriz cuantos valores va a tener.

```csharp 
int[] mi_matriz;

//Iniciación:
mi_matriz=new int[]{valores}; //El 4 hace referencia a la cantidad de valores que vas a insertar.

//Declaración e iniciación en la misma línea: 
int[] mi_matriz = {65,3,7,12,5,6};  //Puedes poner todos los que quieras y añadir más después
```

- Array implícito:

En este array, la variable elegirá su propio tipo dependiendo de los valores del array
Hay que tener en cuenta que no podemos poner valores que no tengan relacion entre si, por ejemplo una "string" y un "int"

```csharp
//Tipo entero
var arrayImplicito = new[] {1,6,2,67};

//Tipo string
var implictoString = new[] {"Juana","ADios","Hola"};

//Tipo Double
var implicitoDecimal = new[] {10,6,1.3,3,6}; 
//En la posicion 2 he puesto un decimal, asi que el array se pone como double

```

Esta ha sido una iniciación a los arrays, pero los arrays son más extensos que esto, para más información ir a:
  - [Uso de for con arrays](#forArrays)
  - [Uso de for/foreach para arrays en POO]()

### 8. Operadores
[Indice](#c)
#### 8.1 Operadores aritméticos
<br>
- Suma                | +
- Resta               | -  
- Multiplicación      | *
- División            | /
- Residuo / Módulo    | % (Devuelve el resto de una division)

Hay 2 utilidades aparte de las que ya tienes:
  - Si ponemos ++ o -- nos sirve para hacer un incremendo o un decremento
  - Podemos usar +=, -=, *=, etc para evitarnos tener que escribir: "variable" = "variable" * 4 
  - El símbolo de + nos sirve para concatenar texto, es decir, podemos juntar distintos textos
```csharp
//usamos siempre la misma estructura que puse al principio, no la pongo para ahorrar espacio
//Ejemplos de operadores
System.Console.WriteLine("Suma: " + (2 + 3));
System.Console.WriteLine("Resta: " + (5 - 2));
System.Console.WriteLine("Multiplicación: " + (4 * 6));
System.Console.WriteLine("División: " + (8 / 2));
System.Console.WriteLine("Residuo/Módulo: " + (7 % 3));

//Ejemplo con variables y operadores

int valor1 = 10;
//incrementamos 1
valor1++;

string textoParaUsar = "Juan";
//concatenamos texto evitando poner
//textoParaUsar = textoParaUsar + " y Maria";
textoParaUsar += " y Maria";

System.Console.WriteLine("La edad de " + textoParaUsar + " es " + valor1);

//Si queremos incrementar directamente en el output debemos de poner el ++ como prefijo
//Nos va a dar como resultado 12 ya que ya lo incrementamos antes
System.Console.WriteLine("La edad de " + textoParaUsar + " es " + ++valor1);

```
>[!Tip]
>Hay una manera mucho más eficaz de crear una oración así que es mediante la interpolación de strings
```csharp
//usamos $ para empezar la interpolación y las variables que queramos añadir las insertamos mediante {}

System.Console.WriteLine($"La edad de {textoParaUsar} es {valor1}");
```
 El en siguiente ejemplo vamos a ver como C# trata a los numeros decimales
```csharp
System.Console.WriteLine(7 / 3);
//Nos va a salir un resultado erroneo, esto ocurre porque aunque C# sepa que da un decimal,
//al ser dos numeros enteros seguirá respondiendo con otro número entero
//Tenemos 3 maneras de solucionarlo

//1. Creando variables que sean de tipo decimal flotar, double, decimal
double num = 7;
double num2 = 3;
System.Console.WriteLine(num / num2);

//2. Escribiendo a mano un número decimal
System.Console.WriteLine(7.0 / 3.0); //usa boolean como predeterminado

//3. Especificando que es un decimal
System.Console.WriteLine(7f / 3f);

```
#### 8.2 Operadores de comparación
[Indice](#c)


- Igual que | ==
- Diferente que | !=
- Menor que | <
- Menor o igual que | <=
- Mayor que | >
- Mayor o igual que | >=

Estos valores nos dan un resultado booleano
```csharp
int tempSevilla = 10;
int tempCadiz = 12;
//solo podemos almacenar el valor en una variable booleana
bool valor = tempSevilla == tempCadiz;

Console.WriteLine(valor);
// Esto nos dará un valor false puesto que 10 no es igual a 12
```
>[!note]
>En C# no es como otros lenguajes, el "==" se puede usar siempre y cuando sean de tipos parecidos, es decir, no puedes comparar una string con valor 12 y un int con valor 10, pero si puedes comparar un int con un float.

#### 8.3 Operadores lógicos
[Indice](#c)


- AND : && (Solo devuelve **true** si todas las expresiones son verdaderas, si no devolverá false)
- OR : || (Devuelve **true** si almenos 1 expresione es verdaderas, si no devolverá false)
- XOR : ^ (a expresión XOR devuelve true cuando hay un número impar de operandos true y false cuando hay un número par de operandos true o todos false.)

```csharp
 bool prueba1 = true;
 bool prueba2 = true; 
 bool prueba3 = false;

 Console.WriteLine(prueba1 && prueba2); //Verdadero
 Console.WriteLine(prueba1 && prueba2 && prueba3); //Falso
 Console.WriteLine(prueba3 || prueba2); //Verdadero

 bool condicion1 = false;
 bool condicion2 = false;
 bool condicion3 = true;
 bool condicion4 = false;

 bool resultadoXORfalse = condicion1 ^ condicion2; 
 bool resultadoXORtrue = condicion1 ^ condicion2 ^ condicion3 ^ condicion4;

 Console.WriteLine($"El resultado de la operación XOR es: {resultadoXORfalse}");
 Console.WriteLine($"El resultado de la operación XOR es: {resultadoXORtrue}");

```

#### 8.4 Operadores lógicos a nivel de bit
[Indice](#c)


Para entender esto debemos de saber como es el lenguaje binario.
<br>
El decimal va de los numero 0 - 9. Son 10 numero distintos.
El binario va del 0 - 1.
<br>
>[!Note]
>Normalmente al escribir en binario pones 4 digitos o 8, siendo los que no estes usando a la izquierda 0, esto se debe a que 1Byte son 8 bits   

Una tabla ver que valores usan:
Decimal - Binario
 - 00 - 0000
   01 - 0001
  02 - 0010
  03 - 0011
  04 - 0100
  05 - 0101
  06 - 0110
  07 - 0111
  08 - 1000
  09 - 1001
  10 - 1010
<br>
Los operadores lógicos daban como resultado "verdadero" o "falso" en este caso verdadero será 1 y falso 0.
```csharp
int num1 = 5;   //101
int num2 = 6;   //110
int num3 = num1 & num2;
/*
    101                 
 && 110             
-----------
    100   = 4                
*/
Console.WriteLine("AND a nivel de bit para 5 y 6 da: " + num3);

num3 = num1 | num2;
/*
    101                 
 || 110             
-----------
    111   = 7              
*/
Console.WriteLine("OR a nivel de bit para 5 y 6 da: " + num3);

num3 = num1 ^ num2;
/*
    101                 
 ^  110             
-----------
    011   = 3                
*/
Console.WriteLine("XOR a nivel de bit para 5 y 6 da: " + num3);
```

### 9. Transformar variables
[Indice](#c) 
<h4>9.1 Casting </h4>   

- Implícito: Se realiza automáticamente por el compilador cuando hay una conversión segura y sin pérdida de datos.   
```csharp
int entero = 5;
double real = entero; //ahora real es igual a 5 siendo decimal
```   
- Explícito: Se realiza manualmente por el programador y puede involucrar la posibilidad de pérdida de datos.
```csharp
double real = 5.67;
int entero = (int)real;
// En este caso como en in no puede haber decimales tenemos que obligar a que cambie su tipo
// Esto produce que se omitan todos los decimales (No se hace un redondeo)
```
>[!NOte]
>En este enlace están todas las [conversiones implicitas](https://learn.microsoft.com/es-es/dotnet/csharp/language-reference/builtin-types/numeric-conversions)
<h4>9.2 Transformación de tipo </h4>
Esta conversion nos permitirá cambiar strings a otro tipo de variable.   
<br><br>
Usaremos el siguiente comando <strong>[Tipo_Al_Que_Quieres_Convertir].Parse(string)</strong>
<br><br>

```csharp
// Queremos que el usuario nos escriba un número, para eso usaremos el comando ReadLine

System.Console.WriteLine("Escribe un número");

int num1 = System.Console.ReadLine();

// Ocurre un error y es que "ReadLine" almacena los datos como una string y nosotros queremos un valor númerico
// asi que tenemos que transformar la string


System.Console.WriteLine("Escribe un número");

int num1 = int.Parse(System.Console.ReadLine();

System.Console.WriteLine("Escribe otro número");

int num2 = int.Parse(System.Console.ReadLine();

System.Console.WriteLine($"La suna es {num1 + num2}");
```
### 10 Estructuras de contol de flujo
[Indice](#c) 
Se les da este nombre a "if" y "while" ya que pueden modificar el flujo de ejecución de un programa.
Como se explicó anteriormente, C# lee el código de arriba a abajo, pero con estas nuevas opciones podemos decirle al codigo que salte lineas,
vaya a otras lineas, vuelva a una linea que ya se ejecutó, etc.

#### 10.1 Condicional **if**

- If del ingles "si pasa algo" nos permitirá realizar ejecutar código si la condicion es correcta, seguirá la siguiente estructura:
<br>
```csharp
if(condifición){
 
  Código

}
```
- Si usamos If también existe Else, este nos permite ejecutar código si la condicion es contraria al if, pero los else siempre deben de ir acompañados de un if.
<br>
```csharp
if(condifición){ 
  
  Código

}else{
  
  Código

}
```
- Otra opción es el Else if, que nos permite añadir otra nueva condición a verificar que debe de ser verdadera para que se ejecute:
<br>
```csharp
if(condifición){ //Se lee primero  
  
  Código

}else if(condición){ //Se lee en caso de que el primero sea falso y este sea verdadero
  
  Código

}
```

>[!note]
>Se puede hacer un if sin añadir "{}" PERO este if solo ejecutará la primera linea de código, el resto del código será considerado como si > estuviese fuera del if.
>```csharp
>if(condición) Código;
>```

- Ejemplo de if:

```csharp
Console.WriteLine("¿Que nota has sacado en el examen 1?");

int NotaEx1 = int.Parse(Console.ReadLine());

Console.WriteLine("¿Que nota has sacado en el examen 2?");

int NotaEx2 = int.Parse(Console.ReadLine());

Console.WriteLine("¿Que nota has sacado en el examen 2?");

int NotaEx3 = int.Parse(Console.ReadLine());

//Aqui vas a poder observar como al usar variables de tipo int, 
//la media de las notas seguirá saliendo como un numero entero aunque de decimales,
// para arreglar eso lo que puedes hacer es declarar las variables con tipo float o double por ejemplo.
if (NotaEx1 >= 5 && NotaEx2 >= 5 && NotaEx3 >= 5) Console.WriteLine($"Has Aprobado, tu nota media es {(NotaEx1 + NotaEx2 + NotaEx3) / 3}");


else Console.WriteLine("Has suspendido al menos 1 examen, tiene que volver en septiembre");
```
- Se pueden hacer if's anidados:

```csharp
Console.WriteLine("¿Que nota has sacado en el examen 1?");

int NotaEx1 = int.Parse(Console.ReadLine());

Console.WriteLine("¿Que nota has sacado en el examen 2?");

int NotaEx2 = int.Parse(Console.ReadLine());

Console.WriteLine("¿Que nota has sacado en el examen 3?");

int NotaEx3 = int.Parse(Console.ReadLine());

if (NotaEx1 >= 5 && NotaEx2 >= 5 && NotaEx3 >= 5)
{
    int NotaMedia = (NotaEx1 + NotaEx2 + NotaEx3) / 3;
    Console.WriteLine($"Has Aprobado, tu nota media es {NotaMedia}");
    if (NotaMedia >= 9)
    {
        Console.WriteLine("Has sacado un sobresaliente");
    }
        else if (NotaMedia >= 7)
        {
            Console.WriteLine("Has sacado un notable");
        }
            else if (NotaMedia >= 6)
            {
                Console.WriteLine("Has sacado un bien");
            } else if (NotaMedia >= 5)
                {
                    Console.WriteLine("Has sacado un suficiente");
                }
}else
{     
   Console.WriteLine("Has suspendido almenos 1 examen, tienes que volver en septiembre");
}
```
>[!Caution]
>Cuidado al generar una variable dentro de un if, al estar dentro el código no lo tomará como existente, asi que todo lo que este fuera de ese if que use esa variable no podrá funcionar, para arreglar eso lo mejor es definir la varible fuera del if e iniciarlizarla, porque como vimos antes, C# no puede usar una variable sin inicializar.

#### 10.2 Ternarios
[Indice](#c)


Son como un if en 1 sola línea, se escriben tal que así:

```csharp
//(condicion) ? valorVerdadero : valorFalso;

int num1 = 5;
string frase = num1 > 6 ? "5 es mayor que 6" : "5 es menor que 6";

Console.WriteLine(frase);
```

#### 10.3 Condicional switch
[Indice](#c)


El switch nos va a permitir escribir menos lineas de código que un "if" siempre y cuando la condición a tener en cuenta sea una igualdad


- A tener en cuenta
  - Cada expresión constante ha de ser única.
  - Solo se puede usar el switch para evaluar:
• int
• char
• String
(float y double han de utilizar if)
  - Los case solo pueden contener expresiones constantes
  - Todos los case deben llevar su break
  - Se puede utilizar [return](#return) y [throw](#throw) (Se explicará más tarde)
```csharp

Switch (expresión de control) 
{
    case expresión constante:
        código a realizar
        break;

    case expresión constante:
        código a realizar
        break;

    default:
        código a realizar
        break;
}
```
Switch funciona de la siguiente manera: La expresion de control es una variable, la cual se va a comparar con los cases, siempre empezando por el primero y yendo 1 a 1, cuando uno de los cases sea true, realizará el código de dentro, en caso de que no haya ningún true, se realizará el "default", el default no es obligatorio ponerlo.

```csharp
Console.WriteLine("De que quieres saber información: Fútbol, coches, aviones");

string interes = Console.ReadLine();

switch (interes)
{
    case "Fútbol":
        Console.WriteLine("Es un deporte muy conocido");
        break;

    case "aviones":
        Console.WriteLine("Vuelan por el cielo");
        break;

    case "coches":
        Console.WriteLine("Van a 4 ruedas");
        break;
        
    default:
        Console.WriteLine("No está en la base de datos");
        break;
}
```
#### 10.4 Blucles
[Indice](#c)


Nos permiten repetir la ejecución de líneas de código un número determinado o indeterminado de veces.
Ventajas:
 - Permite repetir código de forma rápida y sencilla
 - Ahorro de tiempo a la hora de programar
 - Permite trabajar con grandes volúmenes de datos
 - Permite trabajar con Arrays
 <br>
 Tipos:
  - Indeterminados (Hay que ejecutarlo para saber cuantas veces se ejecuta)
      - While
      - Do-While
  - Determinados (Solo con leer el código fuente podemos saber cuantas veces se va a repetir)
      - For 
 

  ##### <h3> 10.4.1 While </h3>
[Indice](#c)


  >[!NOTE]
  > While viene del ingles "Mientras", esto nos ayudará a comprender el funcionamiento.

  Se utiliza el bucle while cuando no sabemos el nº de veces que se repetirá el código de su interior
  Sintaxis:
  ```csharp
  while(condición a evaluar)
  {
    //Código a repetir
  }
  ```
  While funciona de la siguietne manera, **mientras** la condición a evaluar sea verdadera, se seguirá repitiendo el código, cuando sea falsa, parará.
  Ej:
  ```csharp
Console.WriteLine("¿En que mes nació Messi?");

string mesMessi = Console.ReadLine();

while (mesMessi != "junio")
{
    Console.WriteLine("Incorrecto, vuelve a intentarlo");

    mesMessi = Console.ReadLine();
}

Console.WriteLine("Muy bien, Messi nació en junio");
  ```
  ##### <h3> 10.4.2 Do-While </h3>   

```csharp
do
{
  //codigo
}while (Condición);
```
Funciona practicamente igual que el while, la unica diferenciea es que va a ejecutar el codigo almenos 1 vez aunque sea falso.
```csharp
int num = 10;

do
{
  Console.WriteLine("El numero es el " + num);
  num++;
}while(num<10);
```
Creamos una variable y le decimos que si es menor que 10 nos diga que numero és, pero al tener el "do", nos dirá que número es aunque no sea menor que 10.

##### <h3> 10.4.3 For </h3>
[Indice](#c)


El bucle for es cuando sabemos de un vistazo al código el nº de veces que se va a repetir su interior.
La sintaxis básica del bucle for en C# es la siguiente:

```csharp

for (inicialización; condición; expresión de iteración)
{
    // Código a ejecutar en cada iteración
}
```
Donde:

1. Inicialización: Se ejecuta una vez al principio del bucle y generalmente se utiliza para inicializar una variable de control.
2. Condición: Se evalúa antes de cada vuelta. Si la condición es true, el cuerpo del bucle se ejecuta; de lo contrario, el bucle se sale.
3. Expresión de iteración: Se ejecuta al final de cada vuelta y generalmente se utiliza para modificar la variable de control (por ejemplo, incrementarla o decrementarla).
Aquí hay un ejemplo simple de un bucle for que imprime los números del 1 al 5:

```csharp

for (int i = 1; i <= 5; i++)
{
    Console.WriteLine(i);
}
```
Este bucle inicializa i en 1, se ejecuta mientras i sea menor o igual a 5, e incrementa i en 1 en cada vuelta.

- <span id="forArrays">For para arrays</span>:

Un for se puede usar de la siguiente manera para recorrer un array:
```csharp
var implicitoString = new[] { "Juana", "Andrea", "Juan" };

for (int i = 0; i < 3; i++)
{
    Console.WriteLine(implicitoString[i]);
}
```
Como sabemos que el array tiene 3 valores podemos hacerlo de esta manera, pero en el caso de no saberlo o si añadimos/eliminamos otro en la ejecucución no funcionará.
<br>
Para eso hay una manera mucho mejor para hacerlo, y es con la opcion de "Length".
```csharp
for (int i = 0; i < implicitoString.Length; i++)
{
    Console.WriteLine(implictoString[i]);
}
```
De esta forma estaremos diciendo al for que ejecute el código de dentro hasta que llegue a la longitud del array, es decir, el número de variables que contiene.

>[!Note]
>Existe el bucle [foreach](), pero este se dará más adelante
#### Ejercicio

 En este ejemplo se van a poner en práctica varías cosas que se han dado previamente.
 El objetivo es crear un programa que nos genere un numero aleatorio entre el 0-100 (no lo hemos visto asi que ahora proporcionaré la manera de hacerlo) y que el usuario deba averiguar cual es, cuando el usuario se equivoque habrá un texto que le dirá si es mayor o menor y al finalizar habrá un recuento de los intentos realizados.
 ```csharp
 //Para el numero random usaremos lo siguiente

 Random numRandom = new Random();

 int numAleatorio = numRandom.Next(0, 101); //Si ponemos 0,100 el numero será de 0-99.
 ```

 <h3>Resultado:</h3>   

 ```csharp
  Random numRandom = new Random();

 int numAleatorio = numRandom.Next(0, 101);

 int numIntentos = 0;

 int numElegido;
 Console.WriteLine(numAleatorio);
 Console.WriteLine("Adivina que número estoy pensando");

 do
 {
     numIntentos++;  
     numElegido = int.Parse(Console.ReadLine());
     if (numAleatorio > numElegido)
     {
         Console.WriteLine("Incorrecto, el número que he pensado es mayor");
         Console.WriteLine("Vuelve a intentarlo:");
     }
     if (numAleatorio < numElegido)
     {
         Console.WriteLine("Incorrecto, el número que he pensado es menor");
         Console.WriteLine("Vuelve a intentarlo:");
     }
     
 }while (numAleatorio != numElegido);

 Console.WriteLine($"Muy Bien, el número que habia pensado era el {numAleatorio} y lo has averiguado en tan solo {numIntentos} intentos");
``` 

### 11. Excepciones 

11.1 Introducción a Excepciones
[Indice](#c)


Las excepciones son errores en tiempo de ejecución del programa que escapan al control del programador.
Algunos tipos de errores pueden ocurrir por: 
 - Memoria corrupta
 - Desbordamiento de pila
 - Sectores de disco duro defectuosos
 - Acceso a ficheros inexistentes
 - Conexiones a BBDD interrumpidas
 - Etc   
 <br>

Cojamos el ejercicio de arriba donde debemos de acertar el número, más especificamente esta linea:
```chsarp
numElegido = int.Parse(Console.ReadLine());
```
Si en está linea el usuario inserta letras, ya sea intencionalmente o no, nos va a salir un error y el código dejará de ejecutarse.
```csharp
System.FormatException
HResult=0x80131537
Mensaje = The input string 'f' was not in a correct format.
Origen = System.Private.CoreLib
Seguimiento de la pila:
  en System.Number.ThrowFormatException[TChar](ReadOnlySpan`1 value)
  en System.Int32.Parse(String s)
  en prueba_variable.PruebaVariable.Main() en C:\Users\Izan\Documents\C#\ConsoleApp2\ConsoleApp2\Program.cs: línea 21
```
- Si leemos el código podemos encontrar información útil, en la primera línea, nos dice el tipo de error (System.FormatException), un error de formato.   
- Luego en la tercera nos viene un mensaje que dice traducido "La cadena de entrada 'f' no tenía un formato correcto."   
- Y para terminar en la última línea nos sale que archvio es el que ha fallado y en que línea.   
 
>[!Note]   
>En este ejemplo es sencillo ver donde está el fallo, pero al tener un proyecto muy grande es importante saber leer los mensajes de error para poder identificar la falla.   


11.2 Bloques try-catch
[Indice](#c)


La sintaxis es la siguiente:
```chsarp
try 
{
    //código que entra en error
}
catch (Nombre_excepción Nombre_variable_mensaje )
{
    //Código a ejecutar si "try" entra en error
}
```
Como funciona try-catch   
1. Siempre debe de haber un try y un catch
2. El fragmento de código que da el error la metemos dentro de un try (intenta), esto hará que el código intente ejecutar esa línea
3. si acaba en error pasará al catch, comprobará que es la excepción correspondiente y ejecutará el código
4. El nombre de la variable del mensaje lo que nos permite es guardar el mensaje de error en una variable, es decir, si yo cambio eso por mensaje, ahora podría usar la variable mensaje.Message, para usar el mesanje de error como yo quiera.
4. El código seguirá su flujo normal sin pararse.

Un ejemplo sencillo para ver como solventar errores seria el siguiente:
```chasrp
try
{
    numElegido = int.Parse(Console.ReadLine());
}
catch (Format.Exception mensajito)
{
    Console.WriteLine("Has introducido letras. Se pondrá el valor -1 por defecto, intentalo de nuevo");
    Console.WriteLine(mensajito.Message);
    numElegido = -1;
}
```
Lo que hacemos aquí es lo siguiente.
  1. Try intentará ejecutar la línea donde el usuario debe de poner el número, cuando el usuario ponga letras pasaremos a catch.
  2. Catch comprobará que es el error de formato, en caso correcto ejecutará su código, si no, dejará paso a otro error.
  3. Con la variable mensajito ponemos en consola cual es el problema "The input string 'h' was not in a correct format.".
  3. Ya solucionado el problema de las letras ahora hay un problema de inicialización.
  3. Si vemos el código la variable numElegido no se ha inicializado puesto que para inicializarla el usuario debe de escribir un número, al insertar la línea de código en un try el código ahora no está seguro de que esa línea se ejecute asi que entra en otro error, para solucionar eso debemos de inicializar la variable con un número que no interfiera en nuestro juego (puede ser el 101 por ejemplo o el 432).
  4. La solución es poco adecuada pero para el ejemplo nos sirve.

- Pero que pasa si el usuario proporciona un número demasiado largo?   
```csharp
{
    numElegido = int.Parse(Console.ReadLine());
}
catch (FormatException mensajito)
{
    Console.WriteLine("Has introducido letras. Se pondrá el valor -1 por defecto, intentalo de nuevo");
    Console.WriteLine(mensajito.Message);
    numElegido = -1;
}
catch (OverflowException mensajito)
{
    Console.WriteLine("Has introducido demasiados números. Se pondrá el valor -1 por defecto, intentalo de nuevo");
    Console.WriteLine(mensajito.Message);
    numElegido = -1;
}
```
>[!Note]
> Puedes poner "catch" sin necesidad de especificar la excepcion, esto hará que te recoja todas las excepciones en una sola línea, pero no podras almacenar el mensaje en una variable, para eso podemos poner catch (Exception "variable"), esto seguirá recogiendo todas las excepciones pero ahora podremos almacenar el mensaje. Tambien hay que tener en cuenta que puedes hacer un catch especifico y luego uno general pero no viceversa.

11.3 Excluir excepciones
[Indice](#c)


Tambien podemos excluir una excepcion en un catch, quedaría de la siguiente manera
```csharp
try {}
catch (Exception "variable") when ("variable".GetType()!=typeof("exepcion a excluir"))
```
1. Añadimos "when" (cuando...) despues de capturar todas las variables.
2. miramos que tipo de excepcion es la "variable"
3. Usamos comparadores para especificar cual queremos excluir
4. Usamos "typeof" para especificar la excepción a excluir.

```csharp
try
{
    numElegido = int.Parse(Console.ReadLine());
}
catch (Exception mensajito) when (mensajito.GetType()!=typeof(OverflowException))
{
    Console.WriteLine("Has introducido letras. Se pondrá el valor -1 por defecto, intentalo de nuevo");
    Console.WriteLine(mensajito.Message);
    numElegido = -1;
}
```
Realizando esto ahora podriamos añadir otro catch debajo en el que especifiquemos que hacer con "OverflowException".

  11.4 Checked
[Indice](#c)


Para entender este bloque de código hay que entender como C# trata al código.
Dado este caso:
```csharp
int numero = int.MaxValue; //Da el valor máximo de int

int numeroExtra = numero + 20;

Console.WriteLine(numeroExtra);
```
Esto deberia de darnos una excepción de desbordamiento (overflow) pero eso no ocurre. El código nos devuelve un valor erroneo (-2147483629).
¿Porqué ocurre esto?
C# trabaja para mantener un buen rendimiento, en un proyecto de C# es muy normal que haya muchos ecuaciones aritméticas, así que el programa prefiere dar un valor erróneo y seguir con el código a pararlo por completo.
Esto puede ser un problema si necesitamos que ese valor sea correcto para el funcionamiento de nuestro programa, ahí es donde entra el bloque de código "checked".
>[!Important]
>Checked y unchecked solo se pueden usar con "int" y con "long".
```csharp
int numero = int.MaxValue;

checked 
  { 
  int numeroExtra = numero + 20; 
  Console.WriteLine(numeroExtra);
  }
```
Lo que hacemos es meter dentro de checked lo que queremos que de error, ahora al ejecutar el código C# vereficará esa parte para mostrar si hay excepciones o no.   
Tambien se puede hacer de una forma más abreviada
```csharp
int numero = int.MaxValue;

int numeroExtra = checked(numero + 20); 

Console.WriteLine(numeroExtra);
```
Ponemos checked justo donde puede estar el fallo.
>[!Note]
> Hay una forma de ponerlo en todo el proyecto de manera predeterminada. A la derecha en el "Explorador de soluciones" aremos click derecho en nuestro proyecto, en mi caso se llama "ConsoleApp3", buscaremos la opción de "propiedades", luego nos iremos a "Compilación" e iremos a "Opciones avanzadas" y ahí buscamos "Comprobar el desbordamiento aritmético", activamos el recuadro.   
>Ahora no tendremos que poner checked y siempre nos está comprobando todos los desbordamientos aritméticos, ahora podriamos usar el bloque de código "unchecked" para que no comprueba si hay desbordamiento.

11.5 <span id="throw">Throw exceptions</span>
 
En este apartado vamos a ver como lanzar excepciones cuando nosotros queremos.
```csharp
throw new "nombreExcepcion"("información del error");
```
Ejemplo:
```csharp
throw new OverflowException("Error de overflow prueba"); //Si no ponemos nada entre parentesis nos aparecerá el texto predeterminado
```
Pero para que queremos esto?
Esto nos sirve para "obligar" a usar un try-catch y así poder especificar que hacer acontinuación.

Para que el ejemplo sea más realista voy a usar un [método](#método).
Para entrar en contexto un método es un conjunto de líneas de código con un nombre único que podemos llamar desde cualquier parte del programa. Nos permite organizar y reutilizar bloques de código de manera modular.
Usaremos el siguiente método:
```csharp
static string ObtenerNombreMes()
{   
    int numeroMes = int.Parse(Console.ReadLine());
    string nombreMes;

    switch (numeroMes)
    {
        case 1:
            nombreMes = "Enero";
            break;
        case 2:
            nombreMes = "Febrero";
            break;
        case 3:
            nombreMes = "Marzo";
            break;
        case 4:
            nombreMes = "Abril";
            break;
        case 5:
            nombreMes = "Mayo";
            break;
        case 6:
            nombreMes = "Junio";
            break;
        case 7:
            nombreMes = "Julio";
            break;
        case 8:
            nombreMes = "Agosto";
            break;
        case 9:
            nombreMes = "Septiembre";
            break;
        case 10:
            nombreMes = "Octubre";
            break;
        case 11:
            nombreMes = "Noviembre";
            break;
        case 12:
            nombreMes = "Diciembre";
            break;
        default:
            throw new ArgumentException("Número de mes no válido. Debe estar en el rango del 1 al 12.");
    }

    return nombreMes;
}
```
Este código nos devolverá el valor correspondiente a "nombreMes" cuando llamemos a este método. 
¿Cómo podemos usar esto?

```csharp
static void Main()
{
    Console.WriteLine("Hola, en este código te voy a pedir que me des meses para distintas preguntas");
    try
    {
    Console.WriteLine("Dame el mes en el que naciste tú");
    string nombreMes = ObtenerNombreMes();
    Console.WriteLine($"tu mes corresponde al {nombreMes}.");
    }catch ( Exception e )
    {
        Console.WriteLine("Tu més no entra en los rangos del 1-12");
    }


    try
    {
        Console.WriteLine("Dame el mes en el que nació tu hermana");
        string nombreMes = ObtenerNombreMes();
        Console.WriteLine($"El mes en el que nació tu hermana corresponde al {nombreMes}.");
    }
    catch (Exception e)
    {
        Console.WriteLine("El mes de tu hermana no entra en los rangos del 1-12");
    }

}
```
Aquí podemos ver como podemos llamar al mismo método pero darle 2 mensajes de fallo distinto solo por usar el bloque try...catch. 
Si hubieramos puesto un valor defaul como por ejemplo un texto, los siguiente programadores o tu mismo tendrian luego muy limitado el uso de este método, al lanzar (throw) un error, permitimos total libertad para que puedas dar el valor erroneo que quieras.


## Estructura básica
[Indice](#c)  
En C#, laestructura básica de un programa es la siguiente:
- Espacios de nombres [(namespace)](#1-espacios-de-nombres-namespace)
  - Alias [(alias)](#Alias)
  - Clases [(class)](#2-clases-class)
    - Campos [(fields)](#campos)
    - Métodos [(method)](#Métodos)
>[!IMPORTANT]
> Los siguientes ejemplos sirven para comprender el uso de cada elemento, explicaré que función tiene el código pero no es necesario comprender cada línea de código, solamente lo que se esté explicando en esa parte en especifico, voy a explciar de forma jerárquica, es decir, más tarde explicaré cada sub-elemento que se ha usado.  


### 1. Espacios de Nombres (namespace):
[Indice](#c)
**¿Qué es?**: es un contenedor que se utiliza para organizar y agrupar tipos relacionados. El propósito principal de los espacios de nombres es evitar conflictos de nombres y proporcionar una estructura jerárquica para organizar el código.  

```csharp
//namespace [Nombre del espacio]
namespace EspacioDeNombre
{
  //Conteniodo del namepace
}
```
- Que puede contener un espacio de nombres:
  - Alias [(alias)](#2-alias)
  - Clases [(class)](#4-clases-class)
  - Interfaces (interface)
  - Enumeraciones (enum)
  - Delegados (delegate) 
  - Eventos (event) 
  - Estructuras (struct) 
  

- Características:
  - No es obligatorio usarlo, pero es una buena práctica ya que te evita muchos problemas futuros y es más ordenado
  - Puede haber más de 1 en un mismo archivo. 
  - Los namespace no pueden tener modificadores (public, private, etc).
  - Usando namespace no hay conficto de nombres
  - Nos permite usar el código que tenga escrito en otros archivos o proyectos.   
  - Se pueden anidar.
  - El uso de la palabra clave [using](#using)
>[!WARNING]
>Pudes anidar un namespace con otro namespace con exactamente el mismo nombre, pero si usas la palabra clave "using" para acortar la ruta te dará error y el código no podrá saber a que namespace te estás refiriendo.  

- Ejemplo para usar namespace en otros archivos:  

Imaginemos un archivo que contiene lo siguiente:
```csharp
//Puedes comprobar que si intentas correr este codigo, te dará un error, podrá correrlo aun así pero no es un buena práctica.
namespace MiPrograma
{
    public class Prueba
    {
        public static void Valor1()
        {
            int NumeroPrueba = 1;
            System.Console.WriteLine("El valor es " + NumeroPrueba);
        }
    }
}
```
Este archivo nos genera una variable con valor 1 y luego por consola nos muestra un mensaje.  

Ahora vamos a usar este código en otro archivo
>[!IMPORTANT]
>Para usarlo en otro archivo o proyecto asegúrate de que los archivos que contienen tu espacio de nombres y los archivos que lo utilizan estén en el mismo proyecto o que el proyecto que contiene el espacio de nombres esté referenciado por el proyecto que lo utiliza.  

```csharp
namespace ArchvioPrincipal
{ 
    public class ClasePrincipal
    {
        static void Main()
        {
            ProbarCodigo();
        }
        public static void ProbarCodigo()
        {
            //Tenemos que poner toda la ruta NameSpace>Clase>Método.
            MiPrograma.Prueba.Valor1();   
        }
    }
}
```
Esto llamará al método "Valor1" del otro archivo y será ejecutado por el método "ProbarCodigo" cuando el método Main en este caso "Main" lo llame
>[!NOTE]
> Podríamos haber metido "MiPrograma.Prueba.Valor1();" directamente en "Main". Pero para esta explicación he alargado el código.

- Ejemplo para conflicto de nombres:  

Esto quiere decir que no habrá problema en usar el mismo nombre en las clases siempre y cuando esten dentro de otro namespace

Al primer archvio que habiamos creado le añadimos lo siguiente:  
```csharp
namespace MiPrograma
{
 // Código anterior
}
namespace MiPrograma2
{
    public class Prueba
    {
        public static void Valor1() { 
            int NumeroPrueba2 = 2;
            System.Console.WriteLine("El valor es " + NumeroPrueba2);
        }
    }
}
```
y al siguiente archivo en la parte "Main" ponemos
```csharp
namespace ArchivoPrincipal
{ 
    public class ClasePrincipal
    {
        static void Main()
        {
            MiPrograma.Prueba.Valor1();
            MiPrograma2.Prueba.Valor1();
        }
    }
}
```
El codigo seguirá funcionando, lo  unico que hemos cambiado es el nombre del namespace, pero las clases y los métodos siguen teniendo el mismo nombre.
#### 2. Alias
Los alias son un mecanismo que te permite darle a un tipo existente un nombre alternativo. Esto puede ser útil para simplificar nombres largos o para evitar conflictos de nombres entre tipos.

1. Definición:
Puedes utilizar la palabra clave <span id="using">**using**</span> para crear un alias para un tipo. La sintaxis básica es:
```csharp
//using NombreAlias = RutaReal;
using Numero = MiPrograma.Prueba;
namespace MiPrograma
{
    public class Prueba
    {
        public static void Valor1()
        {
            int NumeroPrueba = 1;
            System.Console.WriteLine("El valor es " + NumeroPrueba);
        }
    }
    public class ClasePrincipal
    {
        static void Main()
        {
            Numero.Valor1();
        }
    }
}
```
 Cambiamos la ruta "MiPrograma.Pueba" por "Numero", ahora podemos usar ese alias para evitar escribir toda la ruta siempre

- Tambien podemos usar using para namespaces, pero esto es un poco diferente:

```csharp
using MiPrograma;
namespace MiPrograma
{
    public class Prueba
    {
        public static void Valor1()
        {
            int NumeroPrueba = 1;
            System.Console.WriteLine("El valor es " + NumeroPrueba);
        }
    }
    public class ClasePrincipal
    {
        static void Main()
        {
            Prueba.Valor1();
        }
    }
}
```
Con esto lo que hacemos es saltarnos la parte del espacio de nombre.
 


#### 3. Clases (class)
[Indice](#c)  

**¿Que es?**: Las clases son fundamentales en C#, se utilizan como modelo donde se redactan las características comunes de un
grupo de objetos.  

```csharp
namespace MiPrograma
{
  //[Modificador de Acceso (Opcional)] [Otros Modificadores(Opcional)] partial(opcional) class "Nombre de la clase"
    class MiClase
    {
        // Contenido de la clase aquí
    }
}
``` 
- Que puede contener una clase:
  - Clases (class)
  - Campos [(Fields)](#Campos)
  - Métodos [(Methods)](#Métodos)  
  - Constructores (Constructors)
  - Eventos (event) 
  - Propiedades (Properties) 

- Modificador **Partial**
Este modificador nos permite seguir añadiendo codigo dentro de una clase en distintos archivos, siempre y cuando el namespace sea el mismo

```csharp
partial class archivo1
{
  //Contenido de la clase
}
```
En otro archivo
```csharp
partial class archivo1
{
  //Más contenido en la misma clase
}
```
Esto nos permitirá añadir codigo a una clase desde distintios archvios.

>[!NOTE]
> Las clases son el inicio de la Programación Orientada a Objetos ([POO](#POO))

##### <h3 id="Campos">1. Campos (field):</h3>
[Indice](#c)


**¿Qué es?**: Son variables declaradas en una clase que podrá ser usada siempre en la misma o incluso fuera de la misma si es pública

```csharp
class MiClase
{
    private static int miCampo;
 // En este caso solo en esta misma clase y debe de ser static si queremos usarla sin instanciarla
    static void Main()
    {
      miCampo = 10;
      Console.WriteLine(micampo);
    }
}
```
Los campos son utiles para variables que queramos usar en toda la clase.
##### <h3 id="Métodos"> 2. Métodos (method): </h3>
[Indice](#c)


**¿Necesario?**: No siempre. Un programa debe tener al menos un método Main como punto de entrada para la ejecución.
**¿Qué es?**: código que realiza una tarea específica o una acción.
**Ubicación**: Dentro de una clase.
**¿Para qué sirve**: Para realizar una tarea en concreto en un momento determinado. Un método no ejecuta su código hasta que no es llamado.
<br>
- Estructura: 

[modificadorAcceso] [modificadorOtros] tipoRetorno NombreDelMetodo([parámetros]);

- Es obligatorio que como minimo haya un tipoRetorno y el nombre del método para crear un método
La estructura básica de un método en C# incluye varias palabras clave y elementos opcionales.

Aquí hay una descripción de estas palabras clave:

- [Modificador de Acceso](#Modificadores-de-acceso) (public, private, protected, internal, etc.)(Opcional): Indica el nivel de acceso al método, de manera predeterminada está en private.

- Modificador Otros ([static](), [virtual](), [abstract](), [sealed](), [override](), [async](), [unsafe](), etc.)(opcional): Pueden modificar el comportamiento del método de diversas maneras. No todos son aplicables a todos los métodos.

- Tipo de Retorno (void, int, string, etc.)(obligatorio): Indica el tipo de valor que devuelve el método. Puede ser void si no devuelve nada.

- Nombre del Método: Es el identificador único del método.

- Parámetros: Los valores que se pasan al método cuando se llama.

- Sentencia [return](#return)(Obligatorio): Devuelve un valor del tipo especificado en el tipo de retorno del método, es obligatorio a menos que el método sea de tipo void.

Antes de continuar visita la sentencia return para entender los ejemplos.

<h4> El ejemplo más sencillo sería:</h4> 

```csharp
public class MiClase
{
    static void Main()
    {
        Sumar(); 
    }
    static int Sumar()
    {
      // Cuerpo del método
      int a = 1; 
      int b = 2;
      int resultado = a + b;

      // Devolver el resultado
      return resultado;
    }    
}
```
El método sumar está completo pero hay que llamarlo para que se ejecute, para ello tenemos que hacerlo dentro del Main.

Las variables declaradas dentro de un método son propias de ese método y no se podrán acceder a ellas, a su vez sus nombres no se reservan, es decir, puede volver a usar ese nombre de variable en otro contexto.

>[!Note]
>Más tarde veremos que podemos usar para acceder a variables de dentro de un método.

<h4>Ejemplo con parámetros </h4>

Los parámetros en un método son variables que se definen en la declaración del método y que permiten pasar valores a la función cuando esta es llamada.

```csharp
static void Main()
{ 
    string mensajeMétodo = Sumar(1, 2, "balones");
    Console.WriteLine(mensajeMétodo);
}
static string Sumar(int a, int b, string objeto)
{
    // Cuerpo del método
    int resultado = (a + b);
    string mensaje = "tienes " + resultado + " " + objeto; 

    // Devolver el resultado
    return mensaje;
```

<h4>Ejemplo con void </h4>

Un método con tipo de retorno void no nos devolverá nada, el código que tengra dentro se ejecutará y se acabará.

```csharp
static void Main()
{ 
    Sumar(1, 2, "balones");
    
}
static void Sumar(int a, int b, string objeto)
{
    // Cuerpo del método
    int resultado = (a + b);
    string mensaje = "tienes " + resultado + " " + objeto;

    // Devolver el resultado
    Console.WriteLine(mensaje);
}
```
<h4>Ejemplo con una sola linea de código </h4>

Imaginemos que tenmos este código:

```csharp
static void Main()
{
    Console.WriteLine(Sumar(24, 6));
    
}
static int Sumar(int a, int b)
{   
    return a + b;
}
```

El métdo solo está usando 1 línea de código, en estos casos podemos simplificar el código para quitarnos esas llaves:

```csharp
static void Main()
{
    Console.WriteLine(Sumar(24, 6));
    
}
static int Sumar(int a, int b) => a + b;
```

De esta manera podemos limpiar nuestro código de linias innecesarias.

<h4>Ejemplo con parámetro "opcional"</h4>

Cuando ponemos los parámetros podemos iniciarlizarlos desde un principio.

```csharp
static void Main()
{
    Console.WriteLine(Sumar(24, 6));
    Console.WriteLine(Sumar(24, 6, 5.4));
}
static double Sumar(int a, int b, double c = 0) => a + b + c;

```

En este caso hemos inicializado el double c, esto nos permite decidir si quieremos que use el tercer valor o no. Hay que tener en cuenta que deben de ir siempre al final.
###### <h3 id="return"> Return </h3>
[Indice](#c)


La instrucción return en C# tiene varias utilidades clave:

**Devolver Resultados**: Un método puede realizar cálculos o procesos y luego devolver un resultado al código que lo llamó utilizando return. Esto permite utilizar el valor calculado en otros lugares del programa.

```csharp
static void Main()
{
    Console.WriteLine("Escriba el primer numero");
    int a = int.Parse(Console.ReadLine());
    int b = Sumar();
    Console.WriteLine("total: " + (a + b)); 
}
static int Sumar()
{
    Console.WriteLine("Escriba el segundo numero");
    int a = int.Parse(Console.ReadLine());
    Console.WriteLine("Escriba el tercer numero");
    int b = int.Parse(Console.ReadLine());
    int resultado = a + b;
    return resultado;
}
```
**Salir Temprano**: Puede utilizarse para salir temprano de un método si ciertas condiciones no se cumplen, evitando así la ejecución de código innecesario.

```csharp
static void Main()
{
    Sumar(); 
}
static void Sumar()
{
    Console.WriteLine("Escriba el primer numero");
    int a = int.Parse(Console.ReadLine());
    if ( a <= 0)
    {
        Console.WriteLine("El número no es positivo.");
        // Salir temprano del método
        return;
    }
//De normal este código se ejecutaría pero en el caso de que el "if" sea verdadero,
//todo el código que continua no se ejecutará.
    Console.WriteLine($"El número {a} es positivo.");

    Console.WriteLine("Escribe el segudno numero");

    int b = int.Parse(Console.ReadLine());

    Console.WriteLine($"La suma es {a + b}");


```
**Finalizar Métodos**: En un método que no devuelve un valor (void), return se utiliza simplemente para finalizar la ejecución del método.

```csharp
public void Saludar()
{
    Console.WriteLine("¡Hola desde el método Saludar!");
    // Finalizar el método
    return;
}
```


## <h2 id="POO">Programación orientada a objetos (POO) </h2>
[Indice](#c)


- **¿En qué consiste?**
Trasladar la naturaleza de los objetos de la vida real al código de programación.


- **¿Cuál es la naturaleza de un objeto de la vida real?**
 Los objetos tienen un estado, un comportamiento, y unas propiedades


**Pongamos un ejemplo: El objeto coche**
  - ¿Cuál es el <span style = color:aqua;> **estado**</span> de un coche? Un coche puede estar parado, circulando, aparcado etc
Estado lo entendemos por "como se encuentra/ como está"


  - ¿Qué <span style = color:aqua;> **propiedades**</span> tiene un coche? Un coche tiene un color, un peso, un tamaño etc.
Propiedades lo entedemos como "las características del objeto"


  - ¿Qué <span style = color:aqua;> **comportamiento**</span> tiene un coche? Un coche puede arrancar, frenar, acelerar girar etc.
Comportamiento lo entendemos como "que es capaza de hacer"


- Ventajas:
  - Programas divididos en "trozos", "partes", "módulos" o <span style = color:aqua;>"clases"</span>.
  <span style = color:lightgoldenrodyellow;>Modularización</span>.
  Imaginemos una pc de torre, si se te estrope un componente con solo arreglar ese componente el problema se soluciona, no hay que cambiar el ordenador al completo ya que está dividido


  - Muy reutilizable. <span style = color:lightgoldenrodyellow;>Herencia</span>.
  Imaginemos que compramos nuevos componentes, los antiguos podemos usarlos para otras torres sin ningun problema.


  - Si existe fallo en alguna línea del código, el programa continuará
con su funcionamiento. <span style = color:lightgoldenrodyellow;>Tratamiento de Excepciones</span>.
  Imaginemos que falla algo no muy importante, como un ventilador, el ordenador seguirá funcionando a pesar del fallo.


  - El <span style = color:lightgoldenrodyellow;>encapsulamiento</span> implica ocultar detalles internos y exponer solo la interfaz necesaria.
  El PC tiene un botón para "Encender" y "Apagar", este se conecta a la placa pero SOLO "conoce" "puede usar" lo que le interesa, no puede acceder a nada que no sea para ender y apagar.

    
### Modificadores de acceso
[Indice](#c)


Esto sirve para el encapsulamiento.

1. PUBLIC
Accesible desde cualquier parte

2. PRIVATE
Accesible desde la propia clase

3. PROTECTED
Accesible desde clase derivada

4. INTERNAL
Accesible desde el mismo ensamblado

5. PROTECTED INTERNAL
Accesible desde el mismo ensamblado o clase derivada de otro ensamblado 

6. PRIVATE PROTECTED
Accesible desde la misma clase o clase derivada del mismo ensamblado

7. POR DEFECTO
Accesible desde el mismo paquete


### 1. Creación de Objetos
[Indice](#c)


Las clases son fundamentales en POO, nos permiten modularizar nuestro código y crear objetos.


Primero debemos de entender que los tipos para las variables que hemos estado usando son consideradas de tipo "primitivo" tales como int, double, string, etc.
En la creación de objetos lo que estamos haciendo es darle a la variable un tipo que nosotros hemos creado usando las clases.


Ejemplo:

```csharp
class MiClase
{
    static void Main()
    {
        //Variable con un tipo creado por nosotros, esto lo transforma en un objeto.
        Circulo primerCirculo; 
        
        //Iniciación  de varible/objeto de tipo Circulo. Conocido como "instaciar una clase"
        primerCirculo = new Circulo(); 

        //Al ser un tipo, podemos hacer los objetos que queramos y serán todos diferentes
        Circulo segundoCirculo = new Circulo();
        Circulo tercerCirculo = new Circulo();

        //Podemos almacenar el resultado de un objeto siempre y cuando sean compatibles
        double areaPrimerCirculo = primerCirculo.calcularArea(5); 

        Console.WriteLine(areaPrimerCirculo);

        Console.WriteLine(segundoCirculo.calcularArea(6));
    }
}
class Circulo
{
    //Existe otras maneras más exactas para obtener este valor
    private const double PI = 3.1416; 
    
    //Método para calcular el Area, es necesario ponerlo en Public si queremos que sea accesible fuera de esta clase
    public double calcularArea(int radio) 
    {
        return PI * radio * radio; //Valor del Resultado
    }
}
```

- Una buena práctica a la hora de hacer clases es encapsular(poner en privado) a las variables que usemos, para que así no se puedan cambiar/acceder fuera de la clase. Pero en el caso que debamos de cambiar el valor deberiamos de hacerlo con un método, para especificar parámetros de cambios.


Ejemplo:

Nosotros tendriamos lo siguiente
```csharp
class MiClase
{
    static void Main()
    {
        ConversorEurosDolar primerCambio = new ConversorEurosDolar();

        Console.WriteLine(primerCambio.pasarADolar(10));
    }
}
class ConversorEurosDolar
{
    private double EuroADolar = 1.09;
    
    public double pasarADolar (double dinero)
    {
        return EuroADolar * dinero;
    }
    public double pasarAEuro(double dinero)
    {
        return (1 / EuroADolar) * dinero;
    }
}
```
Esto funciona pero el valor de las monedas fluctua asi que tenemos que se capaces de cambiar el valor de "EuroADolar".


Para ello añadimo lo siguiente en la clases "ConversorEurosDolar":
```csharp
public void cambiarValorEuro (double valorNuevo) //No necesitamos que nos devuelva nada, solo que cambie el valor.
{
    if (valorNuevo > 0)EuroADolar = valorNuevo;
}
```
Ponemos el if puesto que el valor de una moneda no puede ser negativo, en el caso de que hubieramos dejado la variable publica se podría cambiar a cualquier número, al encapsularla y hacer un método para cambiar el valor nos permite tener más control sobre como se usa el código.


Ya podriamos cambiar el valor y seguir convirtiendo la moneda
```csharp
static void Main()
{
    ConversorEurosDolar primerCambio = new ConversorEurosDolar();

    primerCambio.cambiarValorEuro(1.4);

    Console.WriteLine(primerCambio.pasarADolar(10));
}
```

>[!Important]
>Hay que recordar que cada objeto es una instancia, es decir, si yo cambio el valor de la moneda, solo servirá para ese objeto, al crear otro seguirá el valor por defecto. Para que se cambie para siempre, la variable a cambiar deberia de ser static, para que se asocie a la clase y no a la instancia. Quedaría así:
>```chsarp
>private static double EuroADolar = 1.09;
>```   

### 2. Constructores
[Indice](#c)


Los contructores se usan para dar un estado inicial a los objetos.
Se crean usando la misma variable que se ha usado en la clase y deben de ser publics.
```csharp
class Coche
{
  private int ruedas;
  private double largo;
  private double ancho;
  private bool climatizador;
  private String tapiceria;

//Constructor poniendo paramaetros por defecto
  public Coche(){
    ruedas = 4;
    largo = 5.10;
    ancho = 4.50
  }
}
```
Creamos el objeto como hicimos anteriormente.
Ahora nos encontramos con un problema, no podemos acceder a los datos que tiene el objeto Coche. Para solucionar esto usaremos lo siguiente

#### 2.1 Setters y Getters
[Indice](#c)


>[!Note]
>Por conveniencia al nombre le pondremos set o get delante, para identificarlos


Para el set un ejemplo podria ser el siguiente
```csharp
public void setExtras(bool paramClimatizador,String paramTapiceria)
{
climatizador = paramClimatizador;
tapiceria = paramTapiceria;
}
```

Y un get ya lo hemos usado antes, quedaría algo así:

```csharp
public string getInfoCoche()
{
  return $"Información del coche: Ruedas: {ruedas}, Largo: {largo}m, Ancho:{ancho}m";
}
```

#### 2.2 Sobrecarga
[Indice](#c)


Una sobrecarga hace referencia a cuando un método o contructor se usan varias veces con distintas funciones dentro, esto no entra en error siempre y cuando pidan valores distintos unos de otros.
Un ejemplo completo quedaria asi:

```csharp
    static void Main()
    {
        Coche coche1 = new Coche();
        Console.WriteLine(coche1.getInfoCoche());

        Coche coche2 = new Coche(3.4,2.3);
        coche2.setExtras(true, "cuero");
        Console.WriteLine(coche2.getInfoCoche());
        Console.WriteLine(coche2.getExtrasCoche());

    }
}
class Coche
{
    private int ruedas;
    private double largo;
    private double ancho;
    private bool climatizador;
    private String tapiceria;

    //Constructor poniendo paramaetros por defecto
    public Coche()
    {
        ruedas = 4;
        largo = 5.10;
        ancho = 4.50;
    }

    //Sobrecargamos el constructor
    public Coche(double cochelargo, double cocheAncho)
    {
        ruedas = 4;
        largo = cochelargo;
        ancho = cocheAncho;
    }

    public string getInfoCoche()
    {
        return $"Información del coche: Ruedas: {ruedas}, Largo: {largo}m, Ancho:{ancho}m";
    }
    public void setExtras(bool climatizador, String tapiceria)
    {
        this.climatizador = climatizador;
        this.tapiceria = tapiceria;
    }
    public string getExtrasCoche() {
        return $"Tapicería: {tapiceria}, Aire acondicionado: {climatizador}";
    }
```

Podemos ver como hay 2 constructores coche, pero como uno pide parámetros y el otro no, son considerados distintos, se usará el que se adapte mejor a las condiciones.

#### 2.3 this.

El this se usa para especificar que estamos hablando de la variable de esa instancia
```csharp
public void setExtras(bool climatizador, String tapiceria)
    {
        this.climatizador = climatizador;
        this.tapiceria = tapiceria;
    }
```
En este caso las variables que le damos a los parámetros que hemos pasado son las mismas que hemos definido para almacenarla, esto se puede solucionar cambiando el nombre de alguna variable pero en programacion se acostumbra a que todo quede claro a que hace referencia, para eso usamos el "this".
Con él le decimos que es la variable climatizador de la instancia de Coche.

### 3. Math
[Indice](#c)


Hay un clase que ya existe en C# que nos ayuda a realizar operaciones matemática, aqui voy a dar el ejemplo de algunas pero podeis mirar todas las que hay en este enlace: [Math en C#](https://learn.microsoft.com/es-es/dotnet/api/system.math?view=net-8.0)

```csharp
//Redondeo 
double numero = 3.75;
Console.WriteLine(Math.Round(numero)); // Resultado: 4

//Valor absoluto
int valorNegativo = -5;
Console.WriteLine(Math.Abs(valorNegativo)); // Resultado: 5

//Potencia
double baseNumero = 2;
double exponente = 3;
Console.WriteLine(Math.Pow(baseNumero, exponente)); // Resultado: 8

//Raíz cuadrada
double numeroParaRaiz = 9;
Console.WriteLine(Math.Sqrt(numeroParaRaiz)); // Resultado: 3

//Seno y coseno (en radianes)
double anguloEnRadianes = Math.PI / 4; // 45 grados
Console.WriteLine(Math.Sin(anguloEnRadianes)); // Resultado: 0.7071
Console.WriteLine(Math.Cos(anguloEnRadianes)); // Resultado: 0.7071

//Número máximo y mínimo
int numero1 = 10, numero2 = 5;
Console.WriteLine(Math.Max(numero1, numero2)); // Resultado: 10
Console.WriteLine(Math.Min(numero1, numero2)); // Resultado: 5

//Número aleatorio
Random random = new Random();
int numeroAleatorio = random.Next(1, 101); // Genera un número aleatorio entre 1 y 100
Console.WriteLine(numeroAleatorio);
```

### Ejemplo usando todo
[Indice](#c)


Vamos a crear un programa que nos calcule la distancia que hay entre 2 puntos

```csharp
    static void Main()
    {
        //Creo el primer punto
       Punto punto1 = new Punto();   

        //Creo el segundo
       Punto punto2 = new Punto(10,10);

        Punto punto3 = new Punto(24, 62);
        
        //Llamo al método desde un punto
       Console.WriteLine(punto1.DistanciaEntre2Puntos(punto2));

        //Otra prueba
        Console.WriteLine(punto3.DistanciaEntre2Puntos(punto2));
    }
}
class Punto
{
    //Defino los campos privados
    private int x, y;


    //Defino un constructor
    public Punto()
    {
        x = 0;
        y = 0;
    }

    //Sobrecargo el constructor
    public Punto(int x, int y)
    {
        this.x = x;
        this.y = y;
    }

    //Uso un parámetro para recibir un tipo "Punto" es decir, uno de esta clase.
    public double DistanciaEntre2Puntos (Punto Punto2)
    {
        //Guardo variables para la distancia entre cada coordenada
        int distanciaEnX = this.x - Punto2.x;

        int distanciaEnY = this.y - Punto2.y;

        /*Realizo el teorema de pitágoras
         c^2 = a^2 + b^2     ==>    c = Raiz Cuadrada(a^2 + b^2)
                    que es lo mismo que:
        */
        double distanciaEntrePuntos = Math.Sqrt(Math.Pow(distanciaEnX, 2) + Math.Pow(distanciaEnY, 2));

        return distanciaEntrePuntos;
    }
} 
```

### Herencia
[Indice](#c)


Este concepto es muy importante a la hora de programar ya que nos ahorra muchas lineas de código.
La herencia nos permite darle las caracteristicas de la clase a otra sin necesidad de volver a escribir de nuevo el código, la sintaxis es la siguiente:

```csharp
class Empleado
{
  // Codigo/variables a heredar
}

class Jefe : Empleado
{
  //Más código propio
}
```
Un ejemplo usandolo seria el siguiente:

```csharp
    static void Main() 
    {
        Coche coche1 = new Coche(5);
        Console.WriteLine(coche1.Acelerar());

        Camion camion1 = new Camion(1000);
        Console.WriteLine(camion1.Frenar());

    }
}
internal class Vehiculo
{
    protected int ruedas;
    protected int puertas;

    public string Acelerar()
    {
        return "Está acelerando";
    }
    public string Frenar()
    {
        return "Está frenando";
    }
}
class Coche : Vehiculo
{
    int numeroAsientos;
    public Coche(int numeroAsientos)
    {
        ruedas = 4;
        puertas = 5;
        this.numeroAsientos = numeroAsientos;
    }
}
class Camion : Vehiculo
{
    public int cargaMax;
    public Camion(int cargaMax)
    {
        ruedas = 4;
        puertas = 5;
        this.cargaMax = cargaMax;
    }
}
```
En este caso usamos "internal" para la clase, este nos permite usar esa clase para la herencia y haciendo sus datos inaccesibles para clases que no sean hijas.  
Usaremos "protected" y no "private" ya que protected nos permite usar el código en otras clases siempre y cuando sean hijas, private te lo restringe a solo ella misma.
Podemos ver como Coche y camnion pueden usar las variables de Vehiculo, a su vez vemos como al crear los objetos podemos acceder a los metodos Acelerar y Frenar sin haber escrito nada en las nuevas clases.

## BBDD (Bases de datos)

Usaremos MYSQL como base de datos, para poder utilizar MYSQL con Visual Studio necesitaremos "Connector/NET"

### 1. Instalación
[Indice](#c)

- Descargamos el conector desde este [enlace](https://dev.mysql.com/downloads/connector/net/)
- Hacemos doble click en el archivo .msi
- Le damos a continuar y estaría listo

### 2. Base de datos
[Indice](#c)

#### 2.1 Creacion base de datos
Dentro de workbench de mysql crearemos unos nueva conexion y crearemos una nueva base de datos
```mysql
DROP DATABASE IF EXISTS db_csharp;
CREATE DATABASE IF NOT EXISTS db_csharp
CHARACTER SET utf8mb4
COLLATE utf8mb4_spanish_ci;

USE db_csharp;

-- ---------------------------------
-- Tabla unidades de medida
-- ---------------------------------
CREATE TABLE IF NOT EXISTS Unidad_Medida (
  Codigo_um INT NOT NULL AUTO_INCREMENT,
  Descripcion_um VARCHAR(45) NULL,
  PRIMARY KEY (Codigo_um)
  )
ENGINE = InnoDB;
-- ---------------------------------
-- Tabla Marcas
-- ---------------------------------
CREATE TABLE IF NOT EXISTS Categoria (
  Codigo_ca INT NOT NULL AUTO_INCREMENT,
  Descripcion_ca VARCHAR(45) NULL,
  PRIMARY KEY (Codigo_ca)
  )
ENGINE = InnoDB;
-- ---------------------------------
-- Tabla Articulos
-- ---------------------------------
CREATE TABLE IF NOT EXISTS Articulos (
  Codigo_ar INT NOT NULL AUTO_INCREMENT,
  Descripcion_ar VARCHAR(45) NULL,
  Marca VARCHAR(45) NULL,
  Stock SMALLINT NOT NULL DEFAULT 0,
  Fecha_crea DATETIME NULL,
  Fecha_modifica DATETIME NULL,
  Codigo_um INT NOT NULL,
  Codigo_ca INT NOT NULL,
  PRIMARY KEY (Codigo_ar),
  FOREIGN KEY (Codigo_um ) REFERENCES Unidad_Medida (Codigo_um) ON UPDATE CASCADE,
  FOREIGN KEY (Codigo_ca ) REFERENCES Categoria (Codigo_ca) ON UPDATE CASCADE
  )
ENGINE = InnoDB;
```

Las relaciones serian así:  

+--------+‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎‎ ‎+----------+‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ +-----------+  
|‎ Unidad‎‎ ‎|‎----->|‎ Articulos‎ |<-----|‎ Categoria‎ |  
|‎ Medida‎ ‎|‎ ‎ ‎ ‎ ‎ ‎ ‎‎ ‎ +----------+‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ +-----------+  
+--------+      

#### 2.2 Insercion de datos
```mysql
-- Agregar registros a la tabla Unidad_Medida
INSERT INTO Unidad_Medida (Descripcion_um) VALUES
('Metro'),
('Litro'),
('Pulgadas');


-- Agregar registros a la tabla Categoria
INSERT INTO Categoria (Descripcion_ca) VALUES
('Electrónica'),
('Ropa'),
('Hogar');

-- Agregar registros a la tabla Articulos
INSERT INTO Articulos (Descripcion_ar, Marca, Stock, Fecha_crea, Codigo_um, Codigo_ca) VALUES
('Smartphone', 'Samsung', 50, NOW(), 3, 1),
('Camiseta', 'Nike', 100,'2023-06-27', 1, 2),
('Olla a presión', 'CocinaPro', 20, '2022-09-02', 2, 3);
```
### 3. Creacion del proyecto
[Indice](#c)


Para juntar la base de datos con nuestro programa en C# necesitaremos hacer uso de una plantilla en especifico.

- En el selector de plantillas, hay 3 selects, en el primero pondremos "C#" en el esegundo "windows" y en el tercero "Escritorio".
Tendremos que seleccionar la que se llama "Aplicacion de Windows Forms (.NET Framework). Creamos el proyecto

- Dentro del proyecto, a la derecha en el explorador de soluciones, deberemos eliminar "Form1.cs"

- Ahora hacemos click derecho en nuestro proyecto, vamos a "agregar" y clickamos en "Formulario (Windows Form)".

- Ahora deberemos de entrar en el archivo de proytecto "Program.cs" ahi veremos que hay una linea que hace referencia al formulario que hemos borrado, debemos de cambiar el contenido por el formulario que hemos creado nosotros, en mi caso:
```csharp
Application.Run(new Form_articulos());
```
- Haremos click derecho en "Referencias" ahi agregamos una nueva referencia, deberemos de buscar "Mysql.data" la version 8.3.0

>[!Note]
>En caso de que no les aparezca en el buscador clicken en examinar y vayan donde hayan instalado el connector, en mi caso estaba dentro de la carpeta de MYSQL, alli verán un archivo .dll, ese es el que deben importar.

### 4. Crear la conexion
[Indice](#c)


- Primero haremos click derecho en nuestro proyecto y en "agregar" clicaremos "clase", le ponemos el nombre que queremos. En mi caso la llamaré "Conexion"

- Deberemos de modificar un poco la plantilla para que nos quede así
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

//Añadimos dos bibliotecas necesarias
using MySql.Data;
using MySql.Data.MySqlClient;

namespace WindowsFormsApp1
{
    //Cambiamos de internal a public ya que necesitamos que el formulario pueda acceder
    public class Conexion
    {
        //Las variables necesarias a almacenar para poder realizar la conexion
        private string BaseDatos;
        private string Servidor;
        private string Puerto;
        private string Usuario;
        private string Clave;

        private static Conexion con = null;

    }
}
```

- Ahora vamos a darle los valores a estas variables (Cada persona puede tener valores distintos)
Vamos a añadir este método justo debajo de la ultima linea

```csharp
private Conexion() 
{
    this.BaseDatos = "db_csharp";
    this.Servidor = "Localhost";
    this.Puerto = "3306";
    this.Usuario = "root";
    this.Clave = "root";
}
```

- Ahora vamos a definir la forma de conexión

```csharp
public MySqlConnection CrearConexion()
{
    MySqlConnection Cadena = new MySqlConnection();
    try
    {
        Cadena.ConnectionString = $"datasource={this.Servidor.};" +
                                  $"port={this.Puerto};" +
                                  $"username={this.Usuario};" +
                                  $"password={this.Clave};" +
                                  $"Database={this.BaseDatos}";
    }
    catch (Exception ex) 
    {
        throw ex;
    }
    return Cadena;
}
```

- Método para devolver la conexion

```csharp
public static Conexion getInstancia()
{
    if (con == null)
    {
        con = new Conexion();
    }
    return con;
}
```

### 5. Crear las propiedas
[Indice](#c)


- Creamos una nueva clase para las propiedades. Yo le llamaré "P_Articulos".

- Dentro crearemos porpiedades automaticas para todos los campos de la tabla "articulos".
```csharp
 public class P_Articulos
{
    public int Codigo_ar {  get; set; }
    public string Descripcion_ar { get; set; }
    public int Marca { get; set; }
    public int Stock { get; set; }
    public string Fecha_crea { get; set; }
    public string Fecha_modifica { get; set; }
    public int Codigo_um { get; set; }
    public int Codigo_ca { get; set; }

}
```

### 6. Diseño dl Formulario
[Indice](#c)

 
Para este punto lo mejor es que vayas a buscar algun tutorial que te explique como funciona y puedes ver como se ve.
Aun así yo voy a intentar explicarte como puedes hacer un formulario sencillo con sus campos.


- Entraremos en el archvio cs de form, allí deberemos de usar el cuadro de herramientas, en caso de que no aparezca ve a ver>cuadro de herramientas.

1. DataGridView

Es lo que nos permite ver el contenido que vayamos añadiendo a la base de datos.
Yo lo voy a poner en la parte de abajo ocupando un poco menos que la mitad

Ahora, debajo de nuestro explorador de soluciones tendremos que ver que aparece una ventana de propiedades cuando tenemos seleccionado el DataGrid, aqui es donde deberemos de cambiarle el nombre por algo que lo identifique, esto lo haremos con TODOS los elementos que vamos a poner, esta opcion se llama (name), yo la llamaré DGV_principal.

>[!tip]
>En las porpiedades hay una opcion llamada "AllowUsersToAddRows", recomiendo poner esa opcion en false para no alterar el uso de la aplicación.   

2. Elementos

Vamos a hacer uso de "label", "textbox" y "button".
El label lo usaremos para identificar que debemos de escribir en el textbox.
Y el button lo vamos a usar para abrir una ventana emergente cuando debamos elegir los codigos de las claves foraneas.

Esto ya queda a tu gusto el como personalizas tu formulario, recuerda ponerle un valor al (name) para poder identificarlo.

Yo voy a usar 7 botones más, 2 irán juntos, serán los de guardar y cancelar.
Los otros 5 serán: Nuevo, Actualizar, Eliminar,Reporte y Salir.

3. Buscar

Hay que añadir un botón para buscar los articulos en la base de datos.

### 7. Select de MySql
[Indice](#c)

- Nueva clase con nombre D_Articulos

- Añade estás 3 librerias 
```csharp
using System.Data;
using MySql.Data;
using MySql.Data.MySqlClient;
```

- Con este método podremos seleccionar un elmente de la tabla articulos ingresando el nombre en la variable Texto.
```csharp
public DataTable Listado_articulos(string Texto)
{
    MySqlDataReader resultado;
    DataTable Tabla = new DataTable();
    MySqlConnection SqlCon = new MySqlConnection();
    try
    {
        SqlCon = Conexion.getInstancia().CrearConexion();
        string sql_select = "select a.codigo_ar," +
                                    "a.descripcion_ar," +
                                    "a.marca," +
                                    "b.descripcion_um," +
                                    "c.descripcion_ca," +
                                    "a.stock," +
                                    "a.Fecha_crea," +
                                    "a.Fecha_modifica," +
                                    "a.codigo_um," +
                                    "a.codigo_ca " +
                                    "from articulos a " +
                                    "inner join Unidad_medida b on a.codigo_um = b.codigo_um " +
                                    "inner join Categoria c on a.codigo_ca = c.codigo_ca " +
                                    "where Descripcion_ar like '" + Texto + "' ";
        //Esta variable nos guardará la consulta que realizaremos en MYSQL, nos junta las 3 tablas para poder recibir datos de las otras.
        
        MySqlCommand Comando = new MySqlCommand(sql_select, SqlCon);
        Comando.CommandTimeout = 60;
        SqlCon.Open();
        resultado = Comando.ExecuteReader();
        Tabla.Load(resultado);
        return Tabla;
    }
    catch (Exception ex)
    {
        throw ex;
    }
    finally
    {
        if(SqlCon.State == ConnectionState.Open) SqlCon.Close();
    }

```

>[!NOTE]
>La diferencia entre "like" y "=" es que "=" busca exactamente lo que se escribe, en cambio "like" nos permite usar el comodin %, este comodin sería el equivalente a *, que sirve para todos, en el caso de que ponga "%" me buscará todos los registros de la tabla, pero si pongo "s%" buscará todos los registros que empiecen por s.   



### 8. Mostrar datos select
[Indice](#c)

1. En el formulario que hicimos haremos click derecho en el DataGrid y haremos click en "ver codigo"

2. Añadimos el siguiente método
```csharp
private void Listado_articulos(string Texto)
{
    D_Articulos Datos = new D_Articulos();

    //(name) que se le haya puesto al DataGridView
    DGV_principal.DataSource = Datos.Listado_articulos(Texto);

}
```
3. Volvemos al formulario, hacemos click derecho y buscamos la opcion de "propiedades".
En propiedades buscaremos el simbolo del rayo que hace referencia a "Eventos"

4. Buscamos el evento "load" y le damos doble click, añadimos lo siguiente
```csharp
private void Form_articulos_Load(object sender, EventArgs e)
{
    this.Listado_articulos("%");
}
```

Este método hará que al iniciar el formulario cargue este metodo llamdo "Listado_articulos" le pasará el valor % que sirve para decirle al Where que no queremos realizar ningun filtrado. Así nos mostrará toda la tabla al iniciar el formulario

5. Cambiar formato de la tabla

- Si queremos por ejemplo cambiar el nombre mostrado de los campos, cambiar el ancho o no mostrar campos haremos lo siguiente:
```csharp
private void Formato_articulos()
{
    DGV_principal.Columns[0].Width = 80;
    DGV_principal.Columns[0].HeaderText = "Código";
    DGV_principal.Columns[1].Width = 250;
    DGV_principal.Columns[1].HeaderText = "Artículo";
    DGV_principal.Columns[2].Width = 150;
    DGV_principal.Columns[2].HeaderText = "Marca";
    DGV_principal.Columns[3].Width = 80;
    DGV_principal.Columns[3].HeaderText = "Medida";
    DGV_principal.Columns[4].Width = 150;
    DGV_principal.Columns[4].HeaderText = "Categoría";
    DGV_principal.Columns[5].Width = 150;
    GV_principal.Columns[5].HeaderText = "Stock actual";
    DGV_principal.Columns[6].Width = 70;
    DGV_principal.Columns[6].HeaderText = "Fecha Creación";
    DGV_principal.Columns[7].Width = 70;
    DGV_principal.Columns[7].HeaderText = "Ultima Modificación";
    DGV_principal.Columns[8].Visible= false;
    DGV_principal.Columns[9].Visible = false;
}
```

- Deberemos de llamar al método, añadiremos la siguiente linea al método que creamos antes
```chsarp
private void Listado_articulos(string Texto)
{
    D_Articulos Datos = new D_Articulos();
    DGV_principal.DataSource = Datos.Listado_articulos(Texto);
    
    //Agregamos esta linea
    this.Formato_articulos();
}
```
6. Botón buscar

- Para el bloque de texto buscar crearemos un botón, luego de ello haremos doble click en él para que se nos habrá el código
Pondremos lo siguiente:

```csharp
   //Pondremos el (name) del cuadro de texto que usamos para buscar y le añadimo ".Text.Trim"
    this.Listado_articulos("%"+txt_buscar.Text.Trim()+"%");
    //Lo concatenamos con % para hacer que la busqueda se complete con todos los resultados que tengan relacion con lo que escribimos.
```

7. Ahora simplemente clickamos en Iniciar y ya deberiamos de ver el DataGridView con los datos de la tabla


### 9. Añadir registro
[Indice](#c)


- En mi caso yo he añadido un botón llamado "Nuevo" el cual voy a usar para que cuando lo clicke los campos de texto se me activen

1. Para ello hay que ir a los campos de texto y poner la opcion ReadOnly como true. Mi tabla quedaría así:
  - txt_Articulo: ReadOnly = true
  - txt_Marca: ReadOnly = true
  - txt_Medida: ReadOnly = true
  - btn_Medida: Enable = false
  - txt_Categoria: ReadOnly = true
  - btn_Categoria: Enable = false
  - txt_Stock: ReadOnly = true
  - btn_Guardar: Visible = false
  - btn_Cancelar: Visible = false

2. Ahora entramos en el codigo del formulario, como hicimos previamente, click derecho en el formulario y le damos a ver codigo.
Creamos un nuevo método:
```csharp
private void txt_ReadOnly(bool Estado)
private void VistaCampos(bool Estado)
{
    // Bloques de texto
    txt_desc_articulo.ReadOnly = !Estado;
    txt_marca.ReadOnly = !Estado;
    txt_stock.ReadOnly = !Estado;

    txt_
    //Botones

    btn_medida.Enabled = Estado;
    btn_categoria.Enabled = Estado;

    btn_guardar.Visible = Estado;
    btn_cancelar.Visible = Estado;

    btn_nuevo.Enabled = !Estado;
    btn_actualizar.Enabled = !Estado;
    btn_eliminar.Enabled = !Estado;
    btn_reporte.Enabled = !Estado;
    btn_salir.Enabled = !Estado;
}
```
3. Vamos a crear una variable para que el codigo sepa si estamos usando el boton nuevo o no (se debe de almacenar en el codigo del formulario)
```csharp
bool Nuevo = false;
```

4. Ahora haremos doble click en el boton Nuevo, para agregarle una funcionalidad


```csharp
private void btn_nuevo_Click(object sender, EventArgs e)
{
  //Modificamos la variable para que sea true
    Nuevo = true;
    VistaCampos(true);
    txt_desc_articulo.Focus(); //Nos pondrá el curso directamente en el bloque de texto para empezar a escribir
}
```
 - En mi caso tengo un boton "cancelar" al cual le voy a dar la funcionalidad contraria
 ```csharp
  private void btn_cancelar_Click(object sender, EventArgs e)
  {
    //actulizo la variable
    Nuevo = false;
    VistaCampos(false);
    txt_buscar.Focus();
  }
```

4. Crear Sql de insercion

  - 1. Tenemos que irnos al archivo D_Articulos en mi caso

  - 2. Crearemos un nuevo método que se verá así

  ```csharp
  public string Insertar_articulos(bool Nuevo, P_Articulos ObjetoArticulo)
{
    string Mensaje = "";
    string Sql_insert = "";
    MySqlConnection SqlCon = new MySqlConnection();
    try
    {
        if (Nuevo = true)
        {
            SqlCon = Conexion.getInstancia().CrearConexion();
            Sql_insert = "Insert into Articulos (Sescripcion_ar," +
                                                "Sarca," +
                                                "Stock," +
                                                "Fecha_crea," +
                                                "Fecha_modifica," +
                                                "Codigo_um," +
                                                "Codigo_ca)" +
                                                "values('" + ObjetoArticulo.Descripcion_ar + "', " +
                                                "'" + ObjetoArticulo.Marca + "', " +
                                                "'" + ObjetoArticulo.Stock + "', " +
                                                "'" + ObjetoArticulo.Fecha_crea + "', " +
                                                "'" + ObjetoArticulo.Fecha_modifica + "', " +
                                                "'" + ObjetoArticulo.Codigo_um + "', " +
                                                "'" + ObjetoArticulo.Codigo_ca + "')";
        }else
        {
            //Codigo para la actualizacion de registros, lo veremos más tarde
        }    

        MySqlCommand Comando = new MySqlCommand(Sql_insert, SqlCon);
        SqlCon.Open();
        Mensaje = Comando.ExecuteNonQuery() >= 1 ? "Se ingresó correctametne" : "No se puedo ingresar el registro";
    }
    catch (Exception ex)
    {
        Mensaje = ex.Message;
    }
    finally
    {
        if (SqlCon.State == ConnectionState.Open) SqlCon.Close();
    }
    return Mensaje;
}
  ```

  Este método recibe 2 parámetros, un boleano el cual le dirá al "if" si este registro es nuevo o si es una actualización y el otro parámetro nos devuelve un objeto de la clase P_articulos, el cual no va a dar los datos ingresados en los campos.
  
