---
attachments: [Clipboard_2023-10-24-13-37-59.png]
favorited: true
title: '(C#)'
created: '2023-11-21T11:31:08.984Z'
modified: '2023-12-12T19:51:33.412Z'
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
  - [Sintaxis](#sintaxis)
  - [Estructura básica](#estructura-básica)
    - [1. Espacios de Nombres (namespace):](#1-espacios-de-nombres-namespace)
      - [2. Clases (class)](#2-clases-class)
        - [3. Campos (field):](#3-campos-field)
        - [3. Métodos (method):](#3-métodos-method)
    - [4. Propiedades (property):](#4-propiedades-property)
    - [Visual Studio:](#visual-studio)
    - [Seccion1](#seccion1)

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
## Sintaxis
[Indice](#c)  
- SIEMPRE hay que poner ; después de añadir una línea de código.
- No es obligatorio pero es una buena práctica poner la primera letra mayúscula en las clases.
- SIEMPRE hay que definir un Main, si no el código tendrá un error, aun así puede llegar a funcionar.
- C# SÍ distingue entre mayúsculas y minisculas.
- No se pueden modificar las variables que esten definidas dentro de un método importado


## Estructura básica
[Indice](#c)  
En C#, la estructura básica de un programa es la siguiente:
- Espacios de nombres [(namespace)](#1-espacios-de-nombres-namespace)
  - Clases [(class)](#2-clases-class)
    - Campos
  - Interfaces (interface)
  - Enumeraciones (enum)
  - Delegados (delegate) 
  - Eventos (event) 
  - Estructuras (struct) 
  - Alias (alias)

### 1. Espacios de Nombres (namespace):
[Indice](#c)
**¿Qué es?**: es un contenedor que se utiliza para organizar y agrupar tipos relacionados. El propósito principal de los espacios de nombres es evitar conflictos de nombres y proporcionar una estructura jerárquica para organizar el código.  
- Que puede contener un espacio de nombres:
  - Clases [(class)](#2-clases-class)
  - Interfaces (interface)
  - Enumeraciones (enum)
  - Delegados (delegate) 
  - Eventos (event) 
  - Estructuras (struct) 
  - Alias (alias)

- Características:
  - Es el necesario al empezar un archivo nuevo.
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
//Puedes comprobar que si intentas correr este codigo, te dará un error, podrá correrlo aun así pero no es el objetivo.
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

>[!CAUTION]
>Recuerda poner las mayusculas y minúsuclas bien
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

Al primer archvio que habiamos creado le añadimos lo siguiente:  
```csharp
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
El codigo seguirá funcionando, lo  unico que hemos cambiado es el nombre del namespace, pero las clases y los métodos siguen teniendo el mismo nombre

#### 2. Clases (class)
[Indice](#c)  

>[!NOTE]
> Ya he explicado namespace, asi que para no hacer los codigos tan largos voy a dejar de escribirlos si no es necesario para el ejemplo  

**¿Que es?**: Las clases son fundamentales en C#, se utilizan para definir tipos de objetos.  

- Que puede contener una clase:
  - Métodos (Methods)
  - Campos (Fields)
  - Constructores (Constructors)
  - Clases (class)
  - Eventos (event) 
  - Propiedades (Properties) 



- Características:
  - Es el necesario al empezar un archivo nuevo.
  - Puede haber más de 1 en un mismo archivo. 
  - Los namespace no pueden tener modificadores (public, private, etc).
  - Usando namespace no hay conficto de nombres
  - Nos permite usar el código que tenga escrito en otros archivos o proyectos.   
  - Se pueden anidar.
  - El uso de la palabra clave [using]()


```csharp
namespace MiPrograma
{
    class MiClase
    {
        // Contenido de la clase aquí
    }
}
``` 


##### 3. Campos (field):

**¿Qué es?**: Nos almacena una variable que podrá ser usada siempre en la clase o incluso fuera de la misma si es pública

```csharp
class MiClase
{
    private int miCampo;
}
```

##### 3. Métodos (method):
[Indice](#c)
**¿Necesario?**: No siempre. Un programa debe tener al menos un método Main como punto de entrada para la ejecución.
**¿Qué es?**: código que realiza una tarea específica o una acción.
**Ubicación**: Dentro de una clase.
- Estructura: 

[modificadorAcceso] [modificadorOtros] tipoRetorno NombreDelMetodo([parámetros])

  - Es obligatorio que como minimo haya un [tipoRetorno]() y el nombre del método para crear un método
La estructura básica de un método en C# incluye varias palabras clave y elementos opcionales. Aquí tienes una combinación típica de palabras clave que conforman la declaración de un método:

Aquí hay una descripción de estas palabras clave:

- Modificador de Acceso (public, private, protected, internal, etc.): Indica el nivel de acceso al método.

- Modificador Otros (static, virtual, abstract, sealed, override, async, unsafe, etc.): Pueden modificar el comportamiento del método de diversas maneras. No todos son aplicables a todos los métodos.

- Tipo de Retorno (void, int, string, etc.): Indica el tipo de valor que devuelve el método. Puede ser void si no devuelve nada.

- Nombre del Método: Es el identificador único del método.

- Parámetros: Los valores que se pasan al método cuando se llama.

- Cuerpo del Método: Contiene las declaraciones, expresiones y sentencias que definen la lógica del método.

- Sentencia return (opcional): Devuelve un valor del tipo especificado en el tipo de retorno del método.

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

### 4. Propiedades (property):
[Indice](#c)
**¿Necesario?**: No siempre. Se utilizan para acceder y modificar valores de un objeto.
**Ubicación**: Dentro de una clase.

```csharp
class MiClase
{
    public int MiPropiedad { get; set; }
}
```
Ahora, algunas consideraciones adicionales:

Un programa puede tener múltiples espacios de nombres y clases. Puedes organizar tu código en varios espacios de nombres y tener múltiples clases dentro de cada espacio de nombres.

El método Main es el punto de entrada principal para la ejecución del programa. Sin embargo, no todas las clases necesitan tener un método Main. Otros métodos y miembros de las clases pueden interactuar entre sí.

Propiedades, campos y otros miembros de una clase deben declararse dentro de la clase. No puedes declarar propiedades, campos o métodos directamente en el espacio de nombres sin estar dentro de una clase.

En resumen, un programa C# típicamente tiene una estructura jerárquica donde las clases están dentro de espacios de nombres, los métodos están dentro de clases, y otros miembros como propiedades y campos están dentro de clases también. El método Main actúa como el punto de entrada principal. La organización específica dependerá de la complejidad y requisitos de tu programa.
  1. Comentarios:

En C#, puedes agregar comentarios de una sola línea utilizando // o comentarios de varias líneas con /* ... */. Los comentarios son ignorados por el compilador y son útiles para explicar el código.

```c#
// Esto es un comentario de una sola línea

/*
   Esto es un comentario
   de varias líneas
*/
```
2. Directivas de Uso (using directives):

Las directivas using permiten importar espacios de nombres para que puedas usar tipos sin tener que escribir sus nombres completos.

```csharp
using System;
```

Esto nos permite ahorrar codigo por ejemplo:

```csharp
//sin usar "using"
System.Console.WriteLine("Primera línea");
System.Console.WriteLine("Segunda línea");

//usando "using"
using System
Console.WriteLine("Primera línea");
Console.WriteLine("Segunda línea");
```
3. Espacios de Nombres (namespace):

Los espacios de nombres son un contenedor que se usa para organizar y agrupar tipos (clases, interfaces...).

```csharp
namespace MiEspacioDeNombres
{
    // Tu código aquí
}
```
4. Clases:

Las clases son fundamentales en C#. Contienen miembros como campos, propiedades, métodos, eventos, y más.

```c#
class MiClase
{
    // Miembros de la clase aquí
}
```
5. Métodos:

Los métodos son bloques de código que realizan tareas específicas. El método Main es el punto de entrada de una aplicación de consola.

csharp
Copy code
class MiClase
{
    static void Main()
    {
        // Código del método Main
    }

    void OtroMetodo()
    {
        // Código de otro método
    }
}
6. Variables y Tipos de Datos:

Debes declarar variables antes de usarlas. C# tiene tipos de datos, como int, string, bool, etc.

csharp
Copy code
int numero = 42;
string texto = "Hola, mundo!";
bool esVerdadero = true;
7. Estructuras de Control:
C# incluye estructuras de control como if, else, for, while, switch, etc., para controlar el flujo de ejecución del programa.

csharp
Copy code
if (condicion)
{
    // Código si la condición es verdadera
}
else
{
    // Código si la condición es falsa
}

for (int i = 0; i < 5; i++)
{
    // Código ejecutado en cada iteración
}

while (condicion)
{
    // Código ejecutado mientras la condición sea verdadera
}
8. Arreglos:
Los arreglos permiten almacenar colecciones de elementos del mismo tipo.

csharp
Copy code
int[] numeros = { 1, 2, 3, 4, 5 };
9. Orientación a Objetos:
C# es un lenguaje orientado a objetos. Puedes definir clases, crear objetos y utilizar conceptos como herencia y polimorfismo.

csharp
Copy code
class MiClase
{
    // Campos, propiedades, y métodos de la clase
}

MiClase instancia = new MiClase();
10. Comentarios XML (Documentación):
C# permite agregar comentarios XML para documentar tu código, y estas documentaciones se pueden generar automáticamente como documentación de API.

csharp
Copy code
/// <summary>
/// Este es un comentario de documentación XML
/// </summary>
class MiClase
{
}
Estos son solo algunos de los elementos básicos de la sintaxis de C#. A medida que profundices en el lenguaje, encontrarás conceptos más avanzados y características específicas de .NET que te permitirán construir aplicaciones más complejas y robustas.





### Visual Studio: 
  - 
 
 

### Seccion1
[Indice](#c)

```console
#...
```
- hola
gege
  - egeg

wfwfw

  wffwf

