# git remote add origin https://github.com/breyolic/apuntes-git.git
Con este comando vinculamos nuestro repositorio local con Github.

## Pasos para aportar a otro repositorio
1. Hacer un fork en Github.
2. Clonar el repositorio desde mi cuenta de Github..
3. Crear una rama local.
4. Realizar mis cambios en mi nueva rama local.
5. Confirmar los cambios realizados en local.
6. Hacer push de mis cambios (enviar los commits locales a Github) `git push origin nombre_rama_local`
7. Crear un pull request con la nueva rama de mi repositorio en Github.
8. Esperar que el administrador del repositorio original acepte mis cambios.

## Varios repositorios remotos
Podemos configurar un mismo proyecto para sincronizar cambios con varios repositorios remotos.

## Conexión con SSH
1. generar la llave pub y priv con el comando `ssh-keygen -t rsa -C "breyolic@gmail.com"`
2. Nos pedirá una ubicación para guardarlo. Ejemplo ` /c/llaves-ssh/github_rsa`
3. Abrir la llave pública con el comando `cat /c/llaves-ssh/github_rsa.pub` para luego copiarlo en nuestro repositorio.
4. Una vez configurada la llave, hacer la conexión vía SSH en nuestro cliente. Ejemplo `git remote add githubssh git@github.com:breyolic/apuntes-git.git`
5. Iniciamos ssh-agent en background ejecutando el comando `eval "$(ssh-agent -s)"`(resultado `Agent pid xxxxx`) y a continuación agregamos la llave ssh generada a ssh-agent ejecutando el comando `ssh-add /c/llaves-ssh/github_rsa` (resultado `Identity added: /c/llaves-ssh/github_rsa (/c/llaves-ssh/github_rsa)`).
6. Ahora ya podemos hacer `git push` sin problemas.
