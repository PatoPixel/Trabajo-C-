---
attachments: [Clipboard_2023-10-24-13-37-59.png, Clipboard_2024-01-01-20-37-10.png, Clipboard_2024-01-02-01-52-25.png]
favorited: true
title: '(C#)'
created: '2023-11-21T11:31:08.984Z'
modified: '2024-01-13T03:53:13.921Z'
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
  - [Estructura general](#estructura-general)
    - [1. Espacios de Nombres (namespace):](#1-espacios-de-nombres-namespace)
      - [2. Alias](#2-alias)
      - [4. Clases (class)](#4-clases-class)
        - [ 3. Métodos (method): ](#-3-métodos-method-)
          - [ Return ](#-return-)
        - [3. Campos (field):](#3-campos-field)

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

Son como un if en 1 sola línea, se escriben tal que así:

```csharp
//(condicion) ? valorVerdadero : valorFalso;

int num1 = 5;
string frase = num1 > 6 ? "5 es mayor que 6" : "5 es menor que 6";

Console.WriteLine(frase);
```

#### 10.3 Condicional switch

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
  - Se puede utilizar [return]() y [throw]() (Se explicará más tarde)
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

11.5 Throw exceptions
 
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

Aquí hablaremos de 









## Estructura general
[Indice](#c)  
En C#, laestructura básica de un programa es la siguiente:
- Espacios de nombres [(namespace)](#1-espacios-de-nombres-namespace)
  - Alias (alias)
  - Clases [(class)](#2-clases-class)
    - Campos
  - Interfaces (interface)
  - Enumeraciones (enum)
  - Delegados (delegate) 
  - Eventos (event) 
  - Estructuras (struct) 

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
  - Clases [(class)](#2-clases-class)
  - Interfaces (interface)
  - Enumeraciones (enum)
  - Delegados (delegate) 
  - Eventos (event) 
  - Estructuras (struct) 
  - Alias (alias)

- Características:
  - No es obligatorio usarlo, pero es una buena práctica ya que te evita muchos problemas futuros y es más ordenado
  - Puede haber más de 1 en un mismo archivo. 
  - Los namespace no pueden tener modificadores (public, private, etc).
  - Usando namespace no hay conficto de nombres
  - Nos permite usar el código que tenga escrito en otros archivos o proyectos.   
  - Se pueden anidar.
  - El uso de la palabra clave [using]()
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
Puedes utilizar la palabra clave **using** para crear un alias para un tipo. La sintaxis básica es:
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

>[!NOTE]
> Ya he explicado namespace, asi que para no hacer los codigos tan largos voy a dejar de escribirlos si no es necesario para el ejemplo.  


#### 4. Clases (class)
[Indice](#c)  

**¿Que es?**: Las clases son fundamentales en C#, se utilizan para definir tipos de objetos.  

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
  - Métodos (Methods)
  - Campos (Fields)
  - Constructores (Constructors)
  - Clases (class)
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
> Las clases son el inciio de la Programación Orientada a Objetos ([POO](#POO))
##### <h3> 3. Métodos (method): </h3>
[Indice](#c)
**¿Necesario?**: No siempre. Un programa debe tener al menos un método Main como punto de entrada para la ejecución.
**¿Qué es?**: código que realiza una tarea específica o una acción.
**Ubicación**: Dentro de una clase.
**¿Para qué sirve**: Para realizar una tarea en concreto en un momento determinado. Un método no ejecuta su código hasta que no es llamado.
<br>
- Estructura: 

[modificadorAcceso] [modificadorOtros] tipoRetorno NombreDelMetodo([parámetros])

  - Es obligatorio que como minimo haya un [tipoRetorno]() y el nombre del método para crear un método
La estructura básica de un método en C# incluye varias palabras clave y elementos opcionales. Aquí tienes una combinación típica de palabras clave que conforman la declaración de un método:

Aquí hay una descripción de estas palabras clave:

- Modificador de Acceso ([public](), [private](), [protected](), [internal](), etc.): Indica el nivel de acceso al método.

- Modificador Otros ([static](), [virtual](), [abstract](), [sealed](), [override](), [async](), [unsafe](), etc.): Pueden modificar el comportamiento del método de diversas maneras. No todos son aplicables a todos los métodos.

- Tipo de Retorno (void, int, string, etc.): Indica el tipo de valor que devuelve el método. Puede ser void si no devuelve nada.

- Nombre del Método: Es el identificador único del método.

- Parámetros: Los valores que se pasan al método cuando se llama.

- Cuerpo del Método: Contiene las declaraciones, expresiones y sentencias que definen la lógica del método.

- Sentencia [return](#Return) (opcional): Devuelve un valor del tipo especificado en el tipo de retorno del método.

Un ejemplo completo podría ser:

```csharp
public class MiClase
{
    // Método con modificador de acceso, modificador static, tipo de retorno int y parámetros
    public static int Sumar(int a, int b)
    {
        // Cuerpo del método
        int resultado = a + b;

        // Devolver el resultado
        return resultado;
    }
}
```
Este método se llama Sumar, es público, estático, tiene un tipo de retorno int, acepta dos parámetros a y b, y devuelve la suma de los dos parámetros. Recuerda que no todos los modificadores son aplicables a todos los métodos; su aplicabilidad depende del contexto y del tipo de método que estés definiendo.


###### <h3> Return </h3>

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
##### 3. Campos (field):
 
**¿Qué es?**: Nos almacena una variable que podrá ser usada siempre en la clase o incluso fuera de la misma si es [pública](#markdown)

```csharp
class MiClase
{
    private int miCampo;
}
```






