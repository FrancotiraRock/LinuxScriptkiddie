
Para clonarte un repositorio utiliza: git clone (url del repositorio)

Ver los Commit: git log

Ver los cambios de cada commit: git show (y el código de cada commit)

En caso de querer volver a un estado del proyecto pasado, podremos hacer uso del comando ‘**git checkout**‘ seguido del identificador del Commit deseado




Con el comando ‘**git log**‘ podremos siempre listar todos los Commits existentes en un proyecto. Lo que obtendremos es un listado de identificadores los cuales podremos aprovechar para, por ejemplo, mediante el uso del comando ‘**git show**‘ seguido del identificador del Commit cuyas propiedades queramos visualizar, ser capaces de ver todos los cambios que se hayan aplicado para un punto dado del proyecto.

En caso de querer volver a un estado del proyecto pasado, podremos hacer uso del comando ‘**git checkout**‘ seguido del identificador del Commit deseado, pudiendo así volver a ese punto de la historia con todos los archivos existentes para ese entonces restaurados.




El comando ‘**git branch**‘ nos permite crear, enumerar y eliminar ramas, así como cambiar sus nombres. Es importante recalcar que no nos permite cambiar entre ramas o volver a unir un historial bifurcado. Por este motivo, ‘**git branch**‘ está estrechamente integrado con los comandos ‘**git checkout**‘ y ‘**git merge**‘.


Para ver las ramas de un repositorio:
	git branch -a

Para elegir una rama en concreto: git checkout dev

	bandit29@bandit:/tmp/tmp.jOn8CntmrN/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev





En Git, una etiqueta o #tag sirve básicamente como una rama firmada que no permuta, es decir, siempre se mantiene inalterable. Sencillamente es una cadena arbitraria que apunta a un Commit específico. Puede decirse que un tag es un nombre que puedes usar para marcar un punto específico en la historia de un repositorio.

bandit30@bandit:/tmp/tmp.CJjV6Sly1s/repo$ git tag

y para ver las tag --> git show (y el nombre de la tag)


