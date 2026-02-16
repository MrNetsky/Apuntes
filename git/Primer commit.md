Ahora bien... ¿cómo empezamos a usar la herramienta? Fácil, nos dirigimos a la carpeta de nuestro proyecto y escribimos:
```bash
git init
```
Te lo pido por el amor de Dios no hagas lo mismo que yo y fijate dónde estas iniciando el repositorio, porque la primera vez que lo hice lo inicié en la carpeta raíz de Windows. No seas como yo, hacelo mejor ya que te lo estoy explicando.

Ahora bien, luego de trabajar un rato en nuestro proyecto... ¿Cómo sabemos en qué estado se encuentra nuestro repositorio? Pues preguntándole ¿Y cómo hago? Así:
```bash
git status -s
```
El '-s' es la forma corta, viene de 'short', pero si no se lo pones, el comando te dará más información. Sugiero que ejecutes ambas y veas qué onda. 
Si el comando no te devuelve nada, es porque usaste el '-s' y tu repositorio no posee diferencias con el último commit. Si no lo usas te va a decir que no hay cambios. Te lo explico porque cuando me pasó pensé que el comando no funcionaba.

Pero si hay cambios... ¿Qué hago? ¿Cómo los agrego? Con el siguiente comando:
```bash
git add [ARCHIVO]
```
Puedes escribir todos los archivos que quieras, separándolos con un espacio. También puedes poner un punto '.', y esto agregará todos las modificaciones. El comando se vería así:
```bash
git add .
```

Bueno... ¿Ya esta todo listo? ¡No, pará emoción! Recién estamos comenzando. 
Los archivos ahora se encuentran en stage area o área de preparación. Se encuentran listos para ser subidos al repositorio local, pero... ¿Cómo lo hago? Así:
```bash
git commit -m '[MENSAJE]'
```
Se puede hacer sin el '-m [mensaje]', pero no seas así, explicale a tu yo del futuro o tus compañeros qué hiciste. Por favor SIEMPRE que hagas un commit, especifica qué cambios has guardado. Si has predeterminado un editor como se vió en [[Configuración inicial]], se abrirá dicho editor para que escribas el mensaje.

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

[[Introducción a git]]

