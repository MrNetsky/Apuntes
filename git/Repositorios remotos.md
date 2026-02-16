[[Primer commit]]

¿Y qué pasa si yo quiero que mi repositorio se pueda acceder desde cualquier equipo y no sólo desde el mío? Bueno, primero debemos indicar a qué repositorio remoto subiremos los cambios. Para ello iremos a [GitHub](https://github.com/), creamos un perfil y cuando ya estemos logueados, pues le damos a crear un nuevo repositorio. Es importante que, salvo el nombre y la descripción, las demás opciones te recomiendo que las dejes como están.
![[1er-repo-remoto.png]]
Una vez creado el repositorio local, en la terminal deberemos escribir lo siguiente:
```bash
git remote add origin [URL_GITHUB]
```
Antes de subir nuestros archivos la nube, sugiero que renombres la rama 'master' a 'main'. Lo haremos de la siguiente manera:
```bash
git branch -M [NOMBRE]
```
Esto es porque GitHub usualmente trabaja con 'main'. Mientras que el '-m' renombra, mientras que '-M' fuerza dicho renombre, sin importar si hay otra rama con el mismo nombre, aunque como recién arrancamos, no hay otra rama con el mismo nombre.
Ahora sí estamos listos para subir nuestros cambios y lo haremos de la siguiente manera:
```bash
git push -u origin main
```
El '-u' lo usaremos únicamente ahora, para que cada vez que subamos un cambio lo haga en la rama main. Para los posteriores pusheos de contenido, escribiremos:
```bash
git push origin main
```

Y si el repositorio remoto ya tiene cambios, pero el mío no, tengo dos repositorios distintos... ¿Qué se hace? No hay nada para hacer, ese repositorio está muerto, solo queda barajar y dar de nuevo, a menos que hagas lo siguiente:
```bash
git pull origin main
```
Ahí se descargaran los archivos que se hayan modificado a tu repositorio local. Es una buena práctica hacer un pull previo a un push, para evitar problemas de compatibilidad.
<U>Nota:</U> Donde ves que dice 'main', puedes poner el nombre de otra rama.


Y si me piden algo como 'clonar' un repositorio... ¿Qué debo hacer? Bueno, lo primero es entrar en crisis, todo es tristeza y oscuridad hasta que lees que tenes que te das cuenta que debes escribir lo siguiente:
```bash
git clone [URL_GITHUB]
```
Si bien el proyecto se descargará en donde estés situado, por favor, sé consciente dónde vas a descargar dicho directorio.