# CONFIGURACION DE ENTRORNO C/C++ PARA WINDOWS.

Manual de instalacion de entrono de desarrollo en C/C++ con MINGW

## Pasos

1) Instalar MSYS2 64 bits desde msys.org. Se instalaran 3 terminales. <br/>
Esta es una coleccion de herramientas y librerias que nos proveera de un entorno para desarrolladores facil de usar para crear, instalar y correr software nativo de windows escrito en C/C++.

2) Debemos sincronizar y actualizar el paquete de la base de datos de MSYS2. <br/>
   -Para ello en la terminal de MSYS2 ejecutar: 
   
   `pacman -Syu `
   
   -Luego confirmar dos veces con "y"

3) Actualizar los paquetes de base.<br/>
	-Ejecutar el comando:
	
	`pacman -Su`
	
	-Luego confirmar una vez con "y" <br/>
	-Cerrar terminal

4)Abrir la terminal "MSYS2 MinGm 64-bit" para instalar gcc. <br/>

 a) -Primero buscamos los paquetes disponibles con el nombre gcc  
 
	    `pacman -Ss gcc`
	    
    -Ahora buscamos el archivo con el nombre "mingw-w64-x86_64-gcc" para windows de 64bit o "mingw-w32-x86_64-gcc" para 32bit y copiar el nombre para luego indicarlo en el comando de instalacion.
    
  b) -Instalar el packete con:
  
      `pacman -S mingw-w64-x86_64-gcc`
      
      -Continuar con "y"
      
  c)-Comprobar la version:
  
    `gcc --version`  (para c)
    
    o bien:
    
    `g++ --version` (para c++)

d)Buscar el debugger package (paquete de depuracion) "mingw-w64-x86_64-gdb" y copiarlo (este es el de 32 bits).<br/>

  -Instalarlo con el siguiente comando:
  
	`pacman -S mingw-w64-x86_64-gdb`
	
  -Confirmar con "y"

e) Checkear la version de nuestro compilador:

	`gdb --version`


# DEFINIR VARIABLE DE ENTORNO EN WINDOWS
  Setear la variable de entorno (sino no podremos correr el compilador)
## Pasos
1) Ir a C:\msys64\mingw64\bin y copiar esta ruta 
2) Buscar "Enviroment variables settings"
3) En la pestaña de 2system variables" buscar la que dice "path"
y añadir una nueva en esta variable con la ruta "C:\msys64\mingw64\bin"

Listo! Ya tienes tu compilador de C/C++ en Windows.

## Compilar mi primer programa
1) Asegurarse de abrir el terminar y estar situado en la carpeta donde tenemos nuestro archivo .cpp con el codigo en C/C++
2) Ejecutar el siguiente comando:
    `g++ -o "nombre" "miArchivo.cpp"` El nombre es el que recibe el archivo ejecutable .exe listo para correr.
3) Correr el ejecutable generado solamente escribindo el nombre del mismo.
    `nombre`
