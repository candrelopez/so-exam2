### Examen 1
**Universidad ICESI**  
**Curso:** Sistemas Operativos  
**Docente:** Daniel Barragán C.  
**Tema:** Comandos de Linux, Virtualización  
**Nombre:** Carlos Andrés Torres López  
**Código:** A00141804
**Url Git-hub:** https://github.com/candrelopez/so-exam1/tree/A00141804


Parcial Sistemas operativos  

3.  
 1.	Sum_all_numbers  

Respuesta:  
-	Como primer paso creo un archivo sumar.txt dentro del directorio Home.  
![sumar](sumar.jpg)  
-	En el archivo ingrese los números por línea 1,2,3,4.  
-	Luego de esto descargue bc con el comando yum install bc  
-	Luego de esto ejecuto el siguiente comando paste –sd+ sumar.txt | bc  lo que da como resultado la suma de los números, presento a   continuación el pantallazo:  

![Suma_completa](suma_completa.jpg)
 

2.	replace_spaces_in_filenames  

Respuesta:  
-	Inicialmente creo el archivo readme.txt con la siguiente información:  

![Creacion](creacion_archivo.png)

 

Posteriormente utilizo el comando sed  de la siguiente manera sed –i –e  ‘s/ /g’ mas el nombre del fichero en este caso readme.txt y   esto modifica el archivo de la siguiente manera:  

![espacio](espacio.png)
 

Dando como resultado:

![puntos](puntos.png) 




3.	reverse_readme

Respuesta:
Cree el archivo readme.txt con la siguiente información:

![leer](leer_archivo.png)

 

Luego utilizo el comando tac  de la siguiente manera tac readme.txt y genera lo siguiente:

 ![leer_arch](leer_archivo1.png)

4.	remove_duplicated_lines  
Respuesta:  
Inicialmente creo un archivo que se llama líneas repetidas con la siguiente información:
![Linea_duplicada](linea_duplicada.png)
 
 Luego de esto utilizo el el siguiente comando cat líneas_repetidas.txt | sort | uniq lo que me genera el siguiente resultado:  

![linea_duplicada](linea_duplicada1.png)
 
Claramente se ve como quita las líneas repetidas.  
5.	Disp_table  
Respuesta:  

Par imprimir las líneas del archivo csv utilizo la siguiente línea de comando:  
![csv](archivo_csv.png)

Y tiene como resultado:  

![csv1](archivo_csv1.png)
 


4.  Para iniciar con la creación del script realizo lo siguiente:  
Primero creo el usuario gutnberg con el comando:  
-	Useradd –m Gutenberg  
Luego de crear el usuario dentro de la su directorio creo el directorio mybooks   
Con el siguiente comando:  
-	mkdir mybooks  
y dentro de este directorio creo el script.sh de la siguiente forma:  
-	touch script.sh && chmod +x script.sh  
-	luego utilizo el siguiente comando:  
-	echo ‘#!/bin/bash’ > script.sh && echo ‘# -*- ENCODING:  UTF-8 -*-‘ >> script.sh  
Con esto queda creado el script.  
Luego de esto descargo por medio de yum el paquete wget de la siguiente manera:  
Yum install wget  
- Después de instalar este paquete agrego la siguiente linea al script:  
wget -A epub https://www.gutenberg.org/ebooks/55688  
 , luego de esto creo el crontab siguiente :  
 */5 2 * * 1-5 /bin/ejecutar/script.sh  
 
 5. Para este punto descargue los archivos del git que se menciona en el parcial, luego de eso modifique el archivo makefile para que  
 solo utilizara el archivo rickroll, también modifique el archivo rickroll.c modifique la ruta del archivo mp3 y puse la ruta de  
 la canción  que quiero ue suene al tratar de reproducir cualquier mp3, el archivo mp3 con la cancion de mi gente de jbalvin, la puse  
 en la misma carpeta donde estan los archivos.  
 
 Luego de eso ejecute desde la el directorio donde estan los archivos el comando make, este me creo el archivo rickroll.ko  
 para incluirlo como un modulo del kernel ejecute el comando insmod rickroll.ko y esto me carga este modulo en el kernel, y este modulo  lo que realiza en el sistema es hacer que cualquier .mp3 que ejecute  reproduzca el que parametrice en el rickroll.c.  
En el siguiente video demuestro ello:  

https://www.youtube.com/watch?v=o2dxHLIwVIk&feature=youtu.be



