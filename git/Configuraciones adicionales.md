[[Configuración inicial]]

Con el siguiente comando podemos cambiar en qué rama hace el commit inicial. Porque git, lo hace normalmente en master y usualmente se trabaja con main. Aunque también puedes elegir cualquier otra rama.
```bash
git config --global init.defaultBranch [NOMBRE]
```

Con el siguiente comando podrás ver la cantidad de cifras que elijas cuando veas el historial logs de los commits
```bash
git config --global core.abrev [NÚMERO]
```