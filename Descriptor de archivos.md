
Los números que se utilizan para representar los flujos estándar en sistemas Unix y Linux se llaman "descriptores de archivo". En particular:
	0 se refiere al descriptor de archivo estándar de entrada ( #stdin )
	1 se refiere al descriptor de archivo estándar de salida ( #stdout ) 
	2 se refiere al descriptor de archivo estándar de error ( #stderr )

	Ejemplo: exec 3<> mi-archivo ---> Esto creara un archivo en la ruta en donde te encuentres. (cabe destacar que el 3 puedes ser otro numero, puede haber mas descriptores de archivo)
	Si quieres que el archivo sea de solo lectura sera asi ---> exec 3< mi-archivo
	Si quieres que el archivo sera de lectura y escritura sera asi ---> exec 3<> mi-archivo


	En este punto con ( exec 3<> mi-archivo ) has creado un archivo llamado mi-archivo, si quieres guardar el output de un comando en ese archivo utiliza >&3
	Ejemplo: whoami >&3  guardara en el archivo el output del comando whoami

Para cerrar el descriptor de archivos se utiliza el comando exec 3>&- 
Para copiar el descriptor de archivo 3 a otro con numero 6 por ejemplo seria exec 6<&3










