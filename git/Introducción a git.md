Es un sistema de control de versiones distribuido, diseñado por Linus Torvalds. Está optimizado para guardar cambios de forma incremental, lo que permite contar con un historial, pudiendo regresar a una versión anterior y agregar funcionalidades.
El flujo de trabajo es el siguiente.

![[Gemini_Generated_Image_u27otiu27otiu27o.png]]

Los archivos se pueden encontrar en 3 estados dependiendo de dónde se encuentren actualmente.
1. Modified: Son archivos los cuales generan cambios que NO existían en el repositorio anteriormente. Ejemplo de ello son archivos o carpetas que son nuevos, que han sido movidos de lugar, se han eliminados o como su nombre lo indica, son archivos existentes que han sido modificados. Se encuentran en el working directory o directorio de trabajo.
2. Staged: Son los archivos cuyos cambios no se encontraban en el repositorio con anterioridad, pero que están listos para subirse al mismo, pudiendo ser todos los archivos modificados o una selección de los mismos. Se encuentran en el stage area o área de preparación.
3. Commited: Son todos los archivos que se encuentran almacenados en tu repositorio. Mismos, que posteriormente puedes subir a un repositorio remoto. Se encuentran en el local repository o repositorio local

Antes de iniciar, verificar si tenemos instalado git, para ello escribimos en la terminal:
```bash
git --version
```

Si no te devuelve la versión, dependiendo el sistema operativo hay diferentes formas de instalarlo, por lo que hay que entrar en la parte de install de la página de [git](https://git-scm.com/) para ver la manera de hacerlo.

Tema siguiente: [[Configuración inicial]]