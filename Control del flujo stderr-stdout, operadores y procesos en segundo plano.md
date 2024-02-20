
whoami; ls 
	Se ejecutan los dos comandos en líneas deferentes. Si alguno de los dos comandos es erróneo te mostrara la información del correcto y te dirá que el otro no lo es

whoami && ls ----> AND
	solo ejecuta si ambos son correctos, si el primer comando no es valido, no devuelve ningún estado por consola

whoami || ls  -----> OR 
	En este caso te ejecutará ambos, si uno de los dos es erróneo te lo mostrara por pantalla y el otro que si es correcto lo ejecutara de manera correcta.

Ver código de estado:
	echo $?
		Si el código de estado es 127, 1 ó 2 indica que generalmente se produjo un error durante la ejecución del comando

¿Qué es el error estándar (stderr)?
	Los errores se identifican con el numero 2
	Ejemplo: whoam 2>/dev/null
	Por ende no lo muestra en pantalla

Para que tanto el #stderr (errores comunes) como el #stdout (salida estándar de un programa o proceso) queden ocultos pero sigan ejecutándose:
	Ejemplo: cat /etc/hosts &>/dev/null

Procesos #hijo Proceso #padre :
	Para ocultar un proceso por terminal debemos ocultarlo mandándolo al /dev/null
	Ejemplo: wireshark &>/dev/null
			En este caso se abrirá la el proceso/aplicación wireshark pero no aparecerá el proceso por consola.
	Si quieres ejecutar el proceso/aplicacion pero que se ejecute en segundo plano y poder seguir escribiendo en la terminal hay que añadir un & al final del comando
	Ejemplo: wireshark &>/dev/null &
			En este caso solo aparece por consola el PID (es un valor identificativo único de cada programa)
			IMPORTANTE: SIGUE SIENDO UN PROCESO #HIJO, ESTO QUIERE DECIR QUE SI CIERRAS LA TERMINAL SE CIERRAN LOS PROGRAMAS.
	Para convertirlo en proceso #padre debes añadir al final de la linea el comando #disown
	Ejemplo: wireshark &>/dev/null & disown


Listar archivos #ocultos: -a
	Ejemplo: ls -l -a

Crear archivos #ocultos: (poner un punto antes del nomnre del archivo)
	Ejemplo: mkdir .file.txt

Para borrar archivos ocultos no olvides poner el punto antes del nombre del archivo.
Si no funciona puedes hacerlo de manera recursiva: -r
	Ejemplo: rm -r .archivo.txt

Actualizar sistema operatico parrot:
	parrot-upgrade
	NUNCA HAGAS UN UPGRADE A SECAS SE VA PAL CARAJO EL PARROT.

Crear Directorios #temporales:
	mktemp -d

Mirar #diferencias entre archivos 
	diff passwords.old passwords.new
	< p6ggwdNHncnmCNxuAt0KtKVq185ZU7AW (Esta es la linea que se elimina)
	---
	> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg (Esta es la linea que se agrega)
	



Despues de un comando ssh al final de la linea puedes agregar una instruccion para que la realize antes de que las bash se ejecute... por ejemplo una whoami o un bash
	Ejemplo: 
	sshpass -p 'JQttfApK4SeyHwDlI9SXGR50qclOAil1' ssh bandit16@bandit.labs.overthewire.org -p 2220 bash

	Esto te dara una bash interacativa antes de iniciar por completo la bashrc original del sistema


bucle para pin de 4 dígitos fuerza bruta:

for pin in {0000..9999}; do echo "$pin"; done | nc localhost 30002 | grep -v "Wrong"
