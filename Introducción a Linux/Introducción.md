Existe una diferencia conceptual entre **Linux** y **GNU/Linux**. Habitualmente nos referimos a GNU/Linux simplemente como Linux, aunque técnicamente Linux es solamente el **kernel**, es decir, el núcleo del sistema operativo encargado de gestionar los recursos del hardware y coordinar el funcionamiento del sistema. Un sistema **GNU/Linux** combina el kernel Linux con las herramientas del proyecto GNU, bibliotecas, gestores de paquetes y otros componentes que conforman una **distribución** como Debian, Fedora, Arch Linux, entre muchas otras, brindando la experiencia completa de uso.

Dentro de sus capacidades, el kernel administra la memoria, asigna tiempo de CPU a los procesos, controla el acceso a los dispositivos y decide cuándo cada proceso obtiene tiempo de ejecución, implementando lo que se conoce como **multitarea preventiva** (_preemptive multitasking_).

El kernel abstrae los detalles de funcionamiento del hardware mediante una **API (Application Programming Interface)**, permitiendo que las aplicaciones interactúen con recursos del sistema sin necesidad de conocer su implementación específica. Gracias a ello, una aplicación no necesita preocuparse por si los datos se almacenan en un disco rígido mecánico (HDD), una unidad de estado sólido (SSD) o incluso un sistema de archivos remoto.

Cuando un programa se ejecuta, el kernel crea y administra uno o más **procesos** para llevar a cabo su ejecución. También se encarga de asignarles recursos, supervisar su estado y coordinar su interacción con el resto del sistema.

El proyecto **GNU** fue iniciado por Richard Stallman en 1983 con el objetivo de desarrollar un sistema operativo libre. Posteriormente, en 1991, Linus Torvalds creó el kernel **Linux**, escrito principalmente en lenguaje **C**. La combinación del kernel Linux con las herramientas desarrolladas por GNU dio origen a los sistemas GNU/Linux que conocemos actualmente.

El código fuente desarrollado por los programadores no puede ser ejecutado directamente por el procesador. Para ello debe ser traducido a **código máquina** mediante un **compilador**, que transforma los archivos fuente en programas ejecutables. De esta manera es posible construir aplicaciones, bibliotecas y también componentes fundamentales del sistema, como el propio kernel Linux.

Linux y gran parte del ecosistema GNU/Linux están estrechamente relacionados con las filosofías del **Software Libre** y el **Código Abierto**. Estas promueven el acceso al código fuente para que los usuarios puedan estudiarlo, modificarlo y redistribuirlo de acuerdo con las condiciones establecidas por sus respectivas licencias.

## Distribuciones de Linux

Una distribución GNU/Linux reúne el kernel Linux junto con herramientas, bibliotecas, aplicaciones y utilidades que permiten construir un sistema operativo completo. Además, suele incluir un instalador, herramientas de administración del sistema y un gestor de paquetes que facilita la instalación, actualización y eliminación de software.

Aunque existen numerosas distribuciones, gran parte del ecosistema GNU/Linux actual puede agruparse en dos grandes familias: **Debian** y **Red Hat**. Muchas distribuciones populares derivan de una de ellas, como Ubuntu y Linux Mint en el caso de Debian, o Fedora, Rocky Linux y AlmaLinux en el caso de Red Hat.

Una de las diferencias más visibles entre ambas familias es el sistema de gestión de paquetes. Las distribuciones basadas en Debian utilizan paquetes **.deb** y habitualmente el gestor **APT**, mientras que las distribuciones basadas en Red Hat utilizan paquetes **.rpm** y gestores como **DNF**. También existen diferencias en la organización de algunos archivos del sistema, las herramientas de administración, los ciclos de actualización y la filosofía general de cada proyecto.

**Linux Mint** es una distribución GNU/Linux basada en Ubuntu LTS y orientada a ofrecer una experiencia de escritorio sencilla, estable y amigable para el usuario. Hereda la robustez y compatibilidad de Ubuntu, incorporando además herramientas propias que simplifican tareas habituales de administración y configuración.

La edición **Cinnamon**, desarrollada por el equipo de Linux Mint, es la más popular del proyecto. Su interfaz sigue un paradigma tradicional basado en menú de aplicaciones, barra de tareas y área de notificaciones, lo que facilita la transición de usuarios provenientes de Microsoft Windows. Gracias a su equilibrio entre facilidad de uso, personalización y estabilidad, Linux Mint Cinnamon es una de las distribuciones más recomendadas para quienes se inician en GNU/Linux y también para usuarios experimentados que buscan un entorno de trabajo confiable para el día a día.

