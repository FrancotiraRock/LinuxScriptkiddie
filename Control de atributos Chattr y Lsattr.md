

#chattr (Change Attributes)**: Este comando se utiliza para modificar los atributos extendidos de archivos y directorios. Con `chattr`, puedes configurar o eliminar atributos en archivos o directorios para cambiar su comportamiento y propiedades. Algunos atributos comunes que puedes modificar con `chattr` incluyen `+i` para establecer el atributo de solo lectura, `-i` para quitarlo, `+a` para establecer el atributo de apéndice, entre otros.
	Ejemplo: chattr +i [Archivo] le das persimos de inmutable, ni root puede borrar el archivo.
	Para quitar el persimo seria chattr -i [Archivo]


Con lsattr [archivo] ves las propiedades del archivo, es como un #ls normal pero con la cualidad  de mirar los atributos attr 

Y para agregarle esos atributos #chattr (Change Attributes)
Ejemplo: chattr +i  [archivo]


