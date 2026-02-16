[[Introducción a git]]

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
Si usas el '-a' podrás hacer un commit saltando el stage area, aunque no es una práctica. También se puede usar junto a messege de la siguiente manera'-am', por lo menos si vas a hacer algo que no se recomienda, no lo hagas de todo mal. El problema no está si es solo tu repositorio, pero por el amor de Dios no lo hagas en un proyecto.

Y... ¿Qué onda con los repositorios remotos? Puedes crear uno, clonar uno y más, pero en el siguiente tema: [[Repositorios remotos]].
