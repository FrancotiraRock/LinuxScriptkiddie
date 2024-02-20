

Los permisos en si tu quieres borrar un archivo que por ejemplo tiene estos permisos:
	Ejemplo: .rw-r--r-- pepe   pepe
	Este archivo lo creo pepe y otros pueden leerlo pero no escribir.
	Pero siendo otro usuario si te va a dejar borrarlo, porque prevalece los permisos de la carpeta contenedora del archivo drwxrwxrwx.
	Para que esto no ocurra entre en juego el #StickyBit se trata de ponerle permisos especiales a la carpeta contenedora.
		Ejemplo: chmod +t [Carpeta contenedora] con esto solo los usuarios que hayan creado los archivos dentro de esa carpeta podrán modificar sus archivos según sus privilegios


En otras palabras, el bit sticky protege a los usuarios normales de eliminar o renombrar los archivos de otros usuarios en ese directorio, pero no impide que el superusuario (root) realice esas operaciones. Root tiene privilegios completos en el sistema y puede anular la mayoría de las restricciones de permisos. Esto se hace por razones de seguridad y para garantizar que el sistema siempre tenga acceso total y control.