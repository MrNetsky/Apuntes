Un **comando** es una instrucción o palabra clave que el usuario escribe en la interfaz de línea de comandos (**CLI**, _Command Line Interface_) para solicitar al sistema que realice una tarea determinada. Dependiendo de su naturaleza, un comando puede ejecutar un programa externo almacenado en el sistema o una función integrada en el propio shell. Generalmente recibe datos de entrada, los procesa y devuelve un resultado a través de la salida estándar.

El **shell** es un programa que actúa como intermediario entre el usuario y el sistema operativo. Permanece a la espera de instrucciones mediante una línea de comandos identificada por un **prompt**. Su función consiste en interpretar lo que escribe el usuario, localizar el comando solicitado, ejecutarlo y mostrar el resultado obtenido.

**Bash** (_Bourne Again Shell_) es uno de los shells más utilizados en GNU/Linux. Además de actuar como intérprete de comandos, posee su propio lenguaje de scripting, utilizado para automatizar tareas mediante scripts de shell. Existen otras alternativas, como **Z Shell (Zsh)**, que mantiene una alta compatibilidad con Bash e incorpora características avanzadas como un sistema de autocompletado más potente y mayores posibilidades de personalización.

No todos los comandos provienen del mismo lugar, por lo que resulta útil diferenciarlos:

- **Integrados (Built-ins):** Son comandos implementados directamente dentro del shell. Algunos ejemplos son `cd`, `alias`, `history` y `exit`.
- **Comandos externos o ejecutables:** Son programas almacenados en el sistema de archivos. Cuando se ejecutan desde la terminal, el shell los localiza utilizando la variable de entorno **PATH**, que contiene una lista de directorios donde buscar programas ejecutables.
- **Alias:** Son nombres alternativos asignados a comandos existentes con el objetivo de simplificar su escritura o personalizar su comportamiento.
- **Funciones:** Permiten agrupar varios comandos bajo un único nombre, facilitando la automatización de tareas repetitivas. Tanto los alias como las funciones suelen definirse en archivos de configuración como `.bashrc` para Bash o `.zshrc` para Zsh.
