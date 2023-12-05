---
attachments: [Clipboard_2023-10-24-13-37-59.png]
favorited: true
title: '(C#)'
created: '2023-11-21T11:31:08.984Z'
modified: '2023-12-05T21:12:13.869Z'
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
    - [Windows:](#windows-1)
      - [Correr el código](#correr-el-código)
    - [Linux:](#linux-1)
      - [Correr el código](#correr-el-código-1)
  - [Capitulo 3](#capitulo-3)
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

### Windows: 
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


### Linux:

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
[Indice](#c)
## Capitulo 3
[Indice](#c)

- Recursos: 
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

