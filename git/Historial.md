[[Primer commit]]
Antes de ver lo que veremos aquí, necesitaremos saber la identidad de nuestros commits, porque cada uno tiene un hash de identificación único, sería como el DNI de cada uno de los commits. Para ello escribimos lo siguiente:
```bash
git log --oneline
```
Esta es la manera corta, donde te mostrará la cantidad de cifras que hayas elegido en las [[Configuraciones adicionales]], junto al mensaje del commit, pero si quieres más información de dicho commit, tienes que sacar el '--oneline'.

Ahora si 
```bash
git show [COMMIT]:[ARCHIVO]
```
Al commit nos podemos referir con el numero de cifras que incluya el hash indentificatorio o bien escribiendo head e indicándole cuantos commits debe ir hacia atrás. También podemos ver el estado de un archivo en particular en un commit especificado. Este comando puede verse de las siguientes maneras:
```bash
git show 
git show [HASH]
git show HEAD[~[NÚMERO]]
git show [COMMIT_ID]:[ARCHIVO]
git show [RAMA]
```
Si el nombre del archivo contiene espacios deberemos ponerlo entre comillas.