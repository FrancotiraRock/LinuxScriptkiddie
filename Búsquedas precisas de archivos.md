
Para buscar dentro de una carpeta que a su vez tenga muchas carpetas y archivos dentro, podremos buscar con los siguientes comandos:
	Ejemplo: una vez en el directorio a analizar pondremos:
	find . -type f ! -executable -size 1033c

	Nota: Recuerda con -type puedes buscar tanto carpetas (d) como archivos (f)
	El . delante de -type indica que hay que hacer la busqueda en toa la carpeta
	El simbolo ! delante de -executable indica que buscamos archivos no ejecutables
	La c detras de 1033 indica  quebuscas un archivo con 1033 bytes.
			 `b'    for 512-byte blocks (this is the default if no suffix is used)
              `c'    for bytes
              `w'    for two-byte words
              `k'    for kibibytes (KiB, units of 1024 bytes)
              `M'    for mebibytes (MiB, units of 1024 * 1024 = 1048576 bytes)
              `G'    for gibibytes (GiB, units of 1024 * 1024 * 1024 = 1073741824 bytes)


Para buscar archivos de usuarios o grupos especificos: 
	find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null | xargs cat
	Nota: El ultimo comando #xargs cat sirve para abrir directamente el contenido de todo el comando anteriormente escrito.


En este caso vamos a ordenar #alfabéticamente la data dentro de un archivo .txt  y ademas buscar la linea que solo se repita una vez:
short sirve para ordenar #alfabéticamente y #uniq -u para ver las linas que solo se repiden una sola vez.

	cat data.txt | sort | uniq -u


El comando #strings sirve para ver las cadenas #legibles dentro de un archivo #ilegible tipo data
	strings data.txt | grep "==="








