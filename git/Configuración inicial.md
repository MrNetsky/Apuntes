Son comandos cuyas ...
Las mismas se pueden hacer en 3 órdenes, global (para todos los repositorios del usuario), system (para todos los repositorios del equipo o pc) o local (para un repositorio en específico). Los cambios que aplican c/u funcionan de la misma manera que la especificidad de HTML (local>global>system)
**Nombre:**
```bash
git config --global user.name [NOMBRE]
```

**Mail:** (No necesariamente debe ser tu mail real, pero pon similar a esto algo@algomas)
```bash
git config --global user.mail [MAIL]
```

**CRLF:** Es básicamente indica cómo guardar el enter, ya que Linux, MacOS y sistemas derivados de UNIX, están codificados como \n, mientras que en Windows es \r\n. 
¿Pero qué carajos significa esto? Uno hace en un mismo proceso el salto de línea y se posiciona en el principio de la misma, mientras que el otro hace primero el salto de línea y luego el posiciona. 
¿Y esto como afecta a la gente del Congo? Bueno, esto nos evita problemas de compatibilidad cuando se trabaja en equipo con otras personas que pueden no tener nuestro mismo SO.
```bash
git config --global core.autocrlf [PALABRA CLAVE]
```
*Palabra clave según tu SO:*
true --> Windows
input --> Linux y MacOS

**Color:** de interfaz, puedes mantenerlo encendido, apagado o que sea inteligente a la hora de usarlo.
```bash
git config --global color.iu [COMPORTAMIENTO]
```
*Palabras clave según el comportamiento de la interfaz:*
true/auto --> Inteligente
false/never --> Nunca (para los programadores de verdad, los/las que se la bancan, por eso yo uso la anterior.)
always --> Siempre 

**Editor:** Es el programa que git abrirá automáticamente cuando necesites escribir mensajes de commit extensos o realizar ediciones complejas (como en un rebase interactivo).
```bash
git config --global core.editor "[EDITOR] --wait"
```
*Palabra clave según el programa a usar:*
code --> VSC
nano --> Nano
nvim --> NeoVim/LazyVim
Xed --> Xed (Si, el editor de texto base de Linux Mint, estoy tan sorprendido como vos.)
Hay más palabras, OBVIAMENTE, pero no te voy a hacer todo el laburo, si no está tu programa acá, pues buscalo, hace algo vos también.

El '--wait' es para que git te dé tiempo para hacer los cambios en el programa seleccionado, porque de lo contrario hará el commit antes de que siquiera pienses en usarlo. 
Pero hay que tener en cuenta que el '--wait' es solo para los programas que posean una interfaz gráfica (GUI - Graphical User Interface), como VSC o Xed, pero NO es necesaria para neovim o nano (TUI - Text-based User Interface). 
¿Usted preguntará por qué esta discriminación? Porque los TUI corren dentro de la misma terminal, mientras que los GUI no. 
Supongo que la moraleja de esto es 'git no espera a nadie'. Por favor no tome este último párrafo en serio y siga con el siguiente tema: [[Primer commit]]