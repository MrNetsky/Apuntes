Python es un lenguaje de programación creado por **Guido van Rossum** a principios de los años 90. Los archivos creados en Python poseen una extensión '.py' y sus principales características son:

- **Interpretado:** Python utiliza un intérprete para ejecutar el código fuente. En la implementación más utilizada, **CPython**, el código fuente pasa por una etapa intermedia en la que se genera _bytecode_, que posteriormente es ejecutado por la máquina virtual de Python. Por lo tanto, no es completamente correcto pensar simplemente que "Python no se compila"; existe una etapa de traducción intermedia antes de la ejecución.

- **Tipado dinámico:** No es necesario declarar previamente el tipo de una variable. El tipo está determinado por el objeto o valor al que la variable hace referencia en tiempo de ejecución. Además, una misma variable puede pasar a referenciar un objeto de otro tipo:
```python
x = 5
x = "Hola"
```
   Primero `x` hace referencia a un objeto de tipo `int` y posteriormente a uno de tipo `str`.

- **Fuertemente tipado:** Python no realiza conversiones implícitas arbitrarias entre tipos incompatibles. Por ejemplo, no podemos sumar directamente una cadena y un entero:
```python
x = "9" #str
y = 8   #int
   
x + y  # Error
```

   Si queremos realizar una conversión, debemos hacerla explícitamente:

```python
x = int("9")
y = 8

x + y  # 17
```

   Es importante aclarar que `str(x)` no cambia el tipo de `x`; devuelve una representación de `x` como cadena.
   
- **Multiplataforma:** Python dispone de implementaciones para diferentes sistemas operativos, por lo que un programa puede ejecutarse en distintos sistemas sin grandes modificaciones, siempre que no dependa de características específicas de una plataforma.

- **Orientado a objetos:** La programación orientada a objetos (POO) es un paradigma de programación en el que se utilizan **clases y objetos** para representar conceptos relevantes del problema que queremos resolver. Python también permite utilizar otros paradigmas, como la programación imperativa y funcional.   

## Implementaciones de Python

Existen distintas **implementaciones** del lenguaje Python. Una implementación es un programa que proporciona la capacidad de ejecutar el lenguaje.

Entre las implementaciones existentes se encuentran:

- **CPython:** es la que utilizamos habitualmente. Está desarrollada principalmente en C.
- **Jython:** implementación de Python para la plataforma Java/JVM.
- **IronPython:** implementación orientada al ecosistema .NET.
- **PyPy:** implementación alternativa de Python con características diferentes a CPython.

Cuando normalmente hablamos de "Python", en la práctica solemos referirnos a **CPython**, debido a que es la implementación de referencia y la más utilizada.

## Instalación de Python

En Windows, Python puede instalarse mediante el instalador oficial, descargado desde su [página oficial](https://www.python.org/downloads/) o mediante herramientas de gestión de paquetes (winget). Es importantísimo ver si la versión a instalar está disponible para tu Windows, por ejemplo para Windows 7, la última versión de Python compatible es la 3.8.10 del 2021, pero Windows 10 aún puede usar la última disponible.

En muchas distribuciones Linux, Python está disponible o puede instalarse fácilmente mediante el gestor de paquetes. Yo uso Linux Mint con Cinnamon (con una Lenovo T470s) y MATE (con una HP 520) y ya se encontraba instalado.

Para comprobar qué versión tenemos instalada podemos utilizar:

```bash
python --version
```

o, dependiendo del sistema:

```bash
python3 --version
```

