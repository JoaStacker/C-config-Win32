# CONFIGURACION DE ENTRORNO C/C++ PARA WINDOWS.

Manual de instalacion de entrono de desarrollo en C/C++ con MINGW

## Pasos

- **1)** Descargar e instalar MSYS2 64 bits desde https://www.msys2.org/. Se instalaran 3 terminales. <br/>
Esta es una coleccion de herramientas y librerias que nos proveera de un entorno para desarrolladores facil de usar para crear, instalar y correr software nativo de windows escrito en C/C++.<br/>
![image](https://user-images.githubusercontent.com/58922125/120826347-b58dc000-c530-11eb-8bed-4c1a9988586e.png)

- **2)** Debemos sincronizar y actualizar el paquete de la base de datos de MSYS2. <br/> ![image](https://user-images.githubusercontent.com/58922125/120826478-dfdf7d80-c530-11eb-868f-b1f2df6a9561.png) <br/>
	- Para ello en la terminal de MSYS2 ejecutar: 
   
		`pacman -Syu `
   
	- Luego confirmar dos veces con "y"

- **3)** Actualizar los paquetes de base.<br/>
	- Ejecutar el comando:
	
		`pacman -Su`
	
	- Luego confirmar una vez con "y" <br/>
	- Cerrar terminal

- **4)** Abrir la terminal "MSYS2 MinGm 64-bit" para instalar gcc. <br/> ![image](https://user-images.githubusercontent.com/58922125/120826583-fe457900-c530-11eb-907e-13d382041aa0.png) <br/>
	- Primero buscamos los paquetes disponibles con el nombre gcc
  
		`pacman -Ss gcc`
	    
	- Ahora buscamos el archivo con el nombre "mingw-w64-x86_64-gcc" para windows de 64bit o "mingw-w32-x86_64-gcc" para 32bit y copiar el nombre para luego indicarlo en el comando de instalacion.
    
 	- Instalar el packete con:
  
		`pacman -S mingw-w64-x86_64-gcc`
      
	- Continuar con "y"
      
	- Comprobar la version:
  	
		`gcc --version`  (para c)
    
		`g++ --version` (para c++)

	- Buscar el debugger package (paquete de depuracion) "mingw-w64-x86_64-gdb" y copiarlo (este es el de 32 bits).<br/>

	- Instalarlo con el siguiente comando:
  
		`pacman -S mingw-w64-x86_64-gdb`
	
	- Confirmar con "y"

	- Verificar la version de nuestro compilador:

		`gdb --version`


# DEFINIR VARIABLE DE ENTORNO EN WINDOWS
  Definir la variable de entorno (sino no podremos correr el compilador)
## Pasos
- Ir a C:\msys64\mingw64\bin y copiar esta ruta .
- Buscar "Editar variables de entorno" en las configuraciones o simplemente buscarlo en la barra de busqueda.
- En la pesta??a de "Variables del sistema" o "System variables" buscar la variable de nombre "path"
y a??adir una nueva ruta en esta variable con la direccion "C:\msys64\mingw64\bin" que copiamos al comienzo.

Listo! Ya tienes tu compilador de C/C++ en Windows.

## Compilar mi primer programa
- Asegurarse de abrir el terminar y estar situado en la carpeta donde tenemos nuestro archivo .cpp con el codigo en C/C++
- Ejecutar el siguiente comando:

    `g++ -o "nombre" "miArchivo.cpp"` El nombre es el que recibe el archivo ejecutable .exe listo para correr.
    
    `gcc -o "nombre" "miArchivo.c"`
    
-  Correr el ejecutable generado solamente escribindo el nombre del mismo.

    `nombre`
