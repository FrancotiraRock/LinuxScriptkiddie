

Búsqueda de archivos con permisos específicos:
	Ejemplo: find / -perm -4000 2>/dev/null
	-4000 para archivos #suid
	-2000 para archivos #sgid
	-1000 para archivos #StickyBit 

Búsqueda de archivos con nombre especifico
	find / -name [nombre de archivo] 2>/dev/null

Búsqueda con #xargs 
	Sirve para de forma paralela a un primer comando añadirle otra función
	Ejemplo: find / -name passwd 2>/dev/null | xargs ls -l

Búsqueda de directorios o archivos
	Directorios : find / -group parrot -type d 2>/dev/null
	Archivos: find / -group parrot -type f 2>/dev/null

Búsqueda por usuarios:
	find / -user root -type f 2>/dev/null

Búsqueda con permisos de escritura:
	find / -user root -writable -type f 2>/dev/null

Búsqueda con permisos de ejecucion:
	find / -user root -executable -type f 2>/dev/null
	Si quieres que busque archivos agregar al comando -type f 
	De lo contrario encontrara carpetas ejecutables o lo que es lo mismo carpetas a las que puedes entrar 

Búsqueda de archivos que no sabes como se llaman completamente o solo sabes una parte del nombre del archivo
	Ejemplo: para el principio del nombre del archivo
			find / -name dex\*  2>/dev/null
	Ejemplo: para cuando solo sabes una parte del nombre del archivo
			find / -name \*dexlib\* 2>/dev/null
	Si aparte sabes cual es su extension puedes agregar .[extensión]
		Ejemplo:
			find / -name dex\*.rc 2>/dev/null



