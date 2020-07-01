<div align="center">
  <h1>Curso profesional de Git y GitHub</h1>
</div>

<div align="center"> 
  <img src="readme_img/git-github-logo.png" width="60%">
</div>

# Introducción al documento

El contenido de este documento son apuntes del [Curso profesional de Git y GitHub](https://platzi.com/clases/git-github/) y busca ser una guía. El mismo está dictado por [Freddy Vega](https://github.com/freddier) CEO y fundador de [Platzi](https://platzi.com).
***

## Tabla de contenido

- [Introducción a Git](#Introducción-a-Git)
    - [¿Qué es Git y GitHub?](#¿Qué-es-Git-y-GitHub?)
    - [¿Porque usar un sistema de control de versiones como Git?](#¿Porque-usar-un-sistema-de-control-de-versiones-como-Git?)
      - [Comandos básicos](#Comandos-básicos)
    - [Instalando](#Instalando)
    - [Editores de código, archivos binarios y de texto plano](#Editores-de-código,-archivos-binarios-y-de-texto-plano)
    - [Introducción a la terminal y línea de comando](#Introdución-a-la-terminal-y-línea-de-comando)

- [Comandos básicos de Git](#Comandos-básicos-de-Git)
- [Flujo de trabajo básico en Git](#Flujo-de-trabajo-básico-en-Git)
- [Trabajando con repositorios remotos en GitHub](#Trabajando-con-repositorios-remotos-en-GitHub)
- [Flujos de trabajo profesionales](#Flujos-de-trabajo-profesionales)
- [Multiples entornos de trabajo](#Multiples-entornos-de-trabajo)
- [Comandos en Git para casos de emergencia](#Comandos-en-Git-para-casos-de-emergencia)
- [Bonus](#Bonus)


## Introducción a Git

### ¿Qué es Git y GitHub?
[Git](https://git-scm.com/) es un software de control de versiones diseñado por [Linus Torvalds](https://es.wikipedia.org/wiki/Linus_Torvalds), pensando en la eficiencia y la confiabilidad del mantenimiento de versiones de aplicaciones cuando estas tienen un gran número de archivos de código fuente. 

En el siguiente enlace se encuentra el [libro oficial de Git](https://git-scm.com/book/es/v2)

<div align="center"> 
  <img src="readme_img/git-logo.png" width="60%">
  <p></p>
</div>

En su lugar [GitHub](https://github.com/) es una forja para alojar proyectos utilizando el sistema de control de versiones Git. GitHub sería la red social de código para los programadores, tu propio curriculum vitae.

<div align="center"> 
  <img src="readme_img/github-logo.png" width="60%">
  <p></p>
</div>

### ¿Porque usar un sistema de control de versiones como Git?

Un sistema de control de versiones como Git nos ayuda a guardar el historial de cambios y crecimiento de los archivos de nuestro proyecto.

En realidad, los cambios y diferencias entre las versiones de nuestros proyectos pueden tener similitudes, algunas veces los cambios pueden ser solo una palabra o una parte específica de un archivo específico. Git está optimizado para guardar todos estos cambios de forma atómica e incremental, o sea, aplicando cambios sobre los últimos cambios, estos sobre los cambios anteriores y así hasta el inicio de nuestro proyecto.

#### Comandos básicos

- ```$ git init```: Comando para iniciar nuestro repositorio, o sea, indicarle a Git que queremos usar su sistema de control de versiones en nuestro proyecto.
- ```$ git add nombre_archivo.txt```: Comando para que nuestro repositorio sepa de la existencia de un archivo o sus últimos cambios. Este comando no almacena las actualizaciones de forma definitiva, solo las guarda en algo que conocemos como “Staging Area”.
- ```$ git commit -m "Mensaje del commit"```: Comando para almacenar definitivamente todos los cambios que por ahora viven en el staging area. También podemos guardar un mensaje para recordar muy bien qué cambios hicimos en este commit con el argumento -m "Mensaje del commit".
- ```$ git add .```: Se guardan todos los archivos que hayan cambiado en la carpeta donde se hizo init.
- ```$ git status```:  Conocer el estado de modificaciones.
- ```$ git log nombre_archivo.txt```: Muestra el historial de commits.
- ```$ git show```: Muestra uno o mas objetos (blobs, tree, tags y commits), es decir es mucho más completo y detallado.
- ```git push```: Comando que sirve para mandar nuestros commits a un servidor remoto, un lugar donde todos podamos conectar nuestros proyectos.

### Instalando

Windows y Linux tienen comandos diferentes, graban el enter de formas diferentes y tienen muchas otras diferencias. Cuando instales Git Bash en Windows debes elegir si prefieres trabajar con la forma de Windows o la forma de UNIX (Linux y Mac) .

Ten en cuenta que, normalmente, los entornos de desarrollo profesionales tienen personas que usan sistemas operativos diferentes. Esto significa que, si todos podemos usar los mismos comandos, el trabajo resultará más fácil para todos en el equipo.

[Pagina oficial de Git para instalar en diferentes sistemas operativos](https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Instalaci%C3%B3n-de-Git)

#### Instalación en Linux
Cada distribución de Linux tiene un comando especial para instalar herramientas y actualizar el sistema.

En las distribuciones derivadas de Debian (como Ubuntu) el comando especial es `apt-get`, en Red Hat es yum y en ArchLinux es `pacman`. Cada distribución tiene su comando especial y debes averiguar cómo funciona para poder instalar Git.

Antes de hacer la instalación, debemos hacer una actualización del sistema. En nuestro caso, los comandos para hacerlo son `sudo apt-get update` y `sudo apt-get upgrade`.

Con el sistema actualizado, ahora sí podemos instalar Git y, en este caso, el comando para hacerlo es `sudo apt-get install git`. También puedes verificar que Git fue instalado correctamente con el comando `git --version`.

### Editores de código, archivos binarios y de texto plano

Un [editor de código](https://es.wikipedia.org/wiki/Editor_de_c%C3%B3digo_fuente) es una herramienta que nos brinda muchas ayudas para escribir código, algo así como un bloc de notas muy avanzado. Los editores más populares son [VSCode](https://code.visualstudio.com/), [Sublime Text](https://www.sublimetext.com/) y [Atom](https://atom.io/).

Tipos de archivos y sus diferencias:

- **Archivos de Texto (.txt)**: Texto plano normal y sin nada especial. Lo vemos igual sin importar dónde lo abramos, ya sea con el bloc de notas o con editores de texto avanzados.
- **Archivos RTF (.rtf)**: Podemos guardar texto con diferentes tamaños, estilos y colores. Pero si lo abrimos desde un editor de código, vamos a ver que es mucho más complejo que solo el texto plano. Esto es porque debe guardar todos los estilos del texto y, para esto, usa un código especial un poco difícil de entender y muy diferente a los textos con estilos especiales al que estamos acostumbrados.
- **Archivos de Word (.docx)**: Podemos guardar imágenes y texto con diferentes tamaños, estilos o colores. Al abrirlo desde un editor de código podemos ver que es código binario, muy difícil de entender y muy diferente al texto al que estamos acostumbrados. Esto es porque Word está optimizado para entender este código especial y representarlo gráficamente.

### Introducción a la terminal y línea de comando


## Comandos básicos de Git
## Flujo de trabajo básico en Git
## Trabajando con repositorios remotos en GitHub
## Flujos de trabajo profesionales
## Multiples entornos de trabajo
## Comandos en Git para casos de emergencia
## Bonus