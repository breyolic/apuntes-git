# git log
Muestra el historial de commits

`git log --pretty=format:"%h - %an, %ar : %s"`
Muestra el historial con el formato que indicamos.

## Limitar la salida del historial
`git log -n`: Cambiamos la n por cualquer número entero, por ejemplo: `git log -2` nos mostrará los 2 commits más recientes.

`git log --after="2016-04-07 00:00:00"`: Muestra los commits realizados después de la fecha especificada.

`git log --before="2016-04-07 00:00:00"`: Muestra los commits realizados antes de la fecha especificada.

Las vanderas del comando `git log` se pueden usar jutnas según se convenga, por ejemplo:
`git log --after="2016-04-07 12:00:00"--before="2016-04-07 12:30:00"`

`git log --oneline`
Este comando nos muestra el historial de una sola linea por commit
