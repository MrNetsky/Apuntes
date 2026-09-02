## Crear una rama de trabajo
Para NO alterar el main del proyecto, lo que se recomienda es trabajar en una rama paralela, misma que hay que crear. Para ello se usa el siguiente comando:
```bash
git switch -c blog/flasheo-de-repetidores
```
- switch -> Permite cambiar de rama
- -c -> Crea la rama y cambia a ella directamente
- blog/flasheo-de-dispositivos -> Nombre de la rama. Puede ser cualquiera, aunque se sugiere buscar un nombre que refleje los cambios que la rama intenta implementar. En este caso utilicé el prefijo `blog/` porque la rama estaba destinada a incorporar un nuevo artículo.

## Trabajar en la rama
Luego de crear la rama, trabajé en el proyecto hasta terminarlo. En este caso, debía crear un blog y no necesitaba agregar archivos adicionales.

Una vez terminado, probé el proyecto en el servidor local de Docusaurus y, al comprobar que funcionaba correctamente, continué con el proceso.

> **NOTA:** No tuve que realizar ninguna configuración adicional para que Git reconociera los cambios realizados dentro de la rama en la que estaba trabajando. Git ya sabe en qué rama estoy y registra allí los nuevos commits.

## Agregar los cambios al Staging Area
Se adicionan los archivos, en este caso uno solo, por lo que puedo hacer:
```bash
git add .
#ó
git add blog/flasheo-de-repetidores.md
```
Una vez en el stage area, hago el commit para que se guarde en mi repositorio local.

## Crear el commit
Una vez que los cambios están en el **Staging Area**, puedo crear un commit:
```bash
git commit -m 'Agregar el blog sobre flasheo de repetidores'
```
- `git commit` → Crea un nuevo commit con los cambios que están actualmente en el Staging Area.
- `-m` → Permite escribir el mensaje del commit directamente desde la terminal.
- `"Agregar el blog sobre flasheo de repetidores"` → Mensaje que describe qué cambios contiene el commit.

El commit queda almacenado en mi **repositorio local**.

## Configurar los repositorios remotos
En mi caso trabajo con un **fork** del repositorio original.

Por lo tanto, necesito tener configurados dos repositorios remotos:

- `origin` → Mi fork.
- `upstream` → El repositorio original.

Primero configuré `origin` para que apunte a mi fork:

```bash
git remote set-url origin https://github.com/MrNetsky/Documentacion.git
```

Con este comando cambio la URL asociada al remoto llamado `origin`.

Luego agregué el repositorio original como `upstream`:

```bash
git remote add upstream https://github.com/Wildfire-Mesh/Documentacion.git
```

De esta manera puedo obtener posteriormente los cambios realizados en el repositorio original.

Para comprobar que ambos remotos están configurados correctamente:

```bash
git remote -v
```

## Subir la rama a mi fork
Una vez creado el commit, puedo subir la rama a mi fork:

```bash
git push -u origin blog/flasheo-de-repetidores
```

El `-u` tiene una función importante: establece una relación de seguimiento entre mi rama local y la rama remota.

Es decir, después de ejecutar ese comando, Git sabe que:

```
rama local:
blog/flasheo-de-repetidores

        ↓ sigue a

rama remota:
origin/blog/flasheo-de-repetidores
```

Por eso, si posteriormente realizo nuevos cambios en esa misma rama, puedo hacer simplemente:

```
git push
```

sin tener que volver a escribir:

```
git push origin blog/flasheo-de-repetidores
```

## Crear el Pull Request
Una vez con los cambios subidos a mi fork, me parece una opción que dice **compare & pull request**. El Pull Request sirve para **proponer que los cambios realizados en mi rama sean incorporados al `main` del proyecto original**.

## Sincronizar el repositorio local
Una vez finalizado el trabajo y realizado el merge, toca sincronizar mi repositorio local con el repositorio original.

Primero obtengo información actualizada del repositorio original:

```bash
git fetch upstream
```

`git fetch` descarga la información nueva de `upstream`, pero **no modifica directamente mi rama `main`**.

Después incorporo esos cambios a mi `main` local:

```bash
git merge upstream/main
```

Esto hace que mi `main` local incorpore los cambios que están en `upstream/main`.

En mi caso, Git realizó un **Fast-forward**, porque no había cambios diferentes en mi `main` local que impidieran avanzar directamente hasta el nuevo estado.

## Sincronizar mi fork
Después del `merge`, Git me informó que mi `main` local estaba adelantado respecto de `origin/main`.

Sí: **`origin` se refiere a mi fork**, porque anteriormente configuré:

```
origin → MrNetsky/Documentacion
upstream → Wildfire-Mesh/Documentacion
```

Por lo tanto, si mi `main` local tiene commits que todavía no están en mi fork, necesito subirlos:

```bash
git push
```

## Eliminar la rama de trabajo
Por último se elimina la rama porque ya no será utilizada y ha cumplido su propósito, por ello, escribimos lo siguiente:
```bash
git branch -d blog/flasheo-de-repetidores
```