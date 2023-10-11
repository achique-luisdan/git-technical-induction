### INDUCCIÓN TÉCNICA: GIT
#### Introducción a los fundamentos de Git

Versión: 0.0.2

### Prefacio

Este material didáctico, pretende explicar cómo funciona el sistema de control de versiones git, y utilizarlo en nuestro día a día como desarrolladores e incluso como administradores de sistemas. Veremos cómo instalar git, y utilizarlo para mejorar nuestro desarrollo llevándolo a la integración continua.

### Alcance

Este documento busca ofrecer a los nuevos usuarios de Git y a los no tan nuevos una introducción a los fundamentos del mismo, abarcando aspectos como su instalación, configuración, manejo de repositorios, ramas, enfocándose en la parte práctica y no profundizando mucho en detalles conceptuales.

### Historial del Documento

| Fecha |Versión | Comentarios | Autor |
|-------|--------|-------------|-----|
| 19 de Diciembre de 2018 10:00|  0.0.1 | versión inicial |  Achique Luis |
| 24 de agosto de 2020 17:36 | 0.0.2 | Se reescribio el documento mediante la notación Mardown. | Achique Luis |

### Tabla de Contenidos

### 1 Introducción a Git
#### 1.1 Bienvenida

En el desarrollo de software una herramienta de control de versiones como Git y otras como un gestor de peticiones, una herramienta de integración continua o despliegue continuó o una wiki para documentación son necesarias. Hay productos específicos para cada uno de ellos pero ***GitLab*** y ***GitHub*** proporciona en un único producto todas estas funcionalidades.

En este sentido, Git es un sistema de control de versiones, creado originalmente por Linus Torvalds, creador de Linux, y utilizado por millones de desarrolladores a lo largo del mundo.

***GitLab*** es un sistema que partiendo de la idea de tener repositorios Git se ha convertido en un sistema completo para realizar integración continua y llevar nuestro desarrollo a buen término.

#### 1.2 Empezando - ¿Qué es Git?

Como bien se ha dicho Git es un sistema de control de versiones, pero en pocas palabras ¿Qué es un sistema de control de versiones? ¿Cual es su importancia?

Básicamente es un sistema que registra los cambios realizados sobre un archivo o conjunto de archivos almacenados en uno o varios directorios a lo largo del tiempo, de modo que puedas recuperar versiones específicas más adelante.

Te permite revertir archivos a un estado anterior, revertir el proyecto entero a un estado anterior, comparar cambios a lo largo del tiempo, ver quién modificó por última vez algo que puede estar causando un fallo, quién introdujo un error, cuándo, y mucho más.

Si te estas preguntando, si Git te ofrece todo esto. Pues sí y más. Git hace una foto del aspecto de todos tus archivos en ese momento, y guarda una referencia a esa instantánea.

Para ser eficiente, si los archivos no se han modificado, Git no almacena el archivo de nuevo, sólo un enlace al archivo anterior idéntico que ya tiene almacenado.

#### 1.3 Nociones básicas

Es importante que se tengan algunos aspectos en consideración para sacarle el máximo provecho a esta poderosa herramienta.

Git es sistemas de control de versiones distribuido, por lo general se implementa tanto para el uso local como para el uso remoto mediante servidores.

Git organiza y gestiona los repositorios de los proyectos, a través de unidades llamada ramas (branch), por lo general existe una rama principal la cual suele estar almacena en el servidor remoto, por lo general recibe el nombre de rama master.

A su vez, cada usuario puede poseer su rama personal, y en el inicio de los ciclo de desarrollo clona la rama principal (master) y comienza a realizar cambios y mejoras sobre su rama y cuando este considere que su rama esta estable sube sus cambios realizados a la rama principal o ramas previas como development o testing.

#### 1.4 Repositorios y Ramas del Proyecto

Los repositorios principales del proyecto (archivos, directorios, etc.) suelen ser almacenado en servidores remotos de las empresas o mediante servicios que ofrecen plataformas como GitLab y GitHub para el manejo en la nube.

El equipo de trabajo al iniciar sus tares descargan la última instantánea de los archivos: replican completamente el repositorio (clonan). Así, de esta forma si un servidor falla, y estos sistemas estaban colaborando a través de él, cualquiera de los repositorios de los participantes puede copiarse en el servidor para restaurarlo.

### 2. Comenzando a usar Git desde la Línea de Comandos

#### 2.1 Registro en GitLab

Si usted quiere iniciar utilizando Git, es recomendable iniciar creando una cuenta en algunas de las plataformas sugeridas (GitLab o GitHub) e iniciado sesión con una cuenta en Git.

**Notas:**
* Es importante que utilice una dirección de correo electrónica que esté totalmente operativa, debido que la misma se utilizada por las plataformas de GitLab o GitHub para confirmar, validar y recuperar su cuenta.
* También recuerde el nombre de usuario que suministro que lo usarás más adelante.

#### 2.2 Abra una Shell

Dependiendo de su sistema operativo, usted podrá utilizar la shell de su preferencia. Aquí se encuentran algunas sugerencias:

• Terminal on Mac OSX
• GitBash on Windows
• Linux Terminal on Linux

#### 2.3 Compruebe si Git esta previamente instalado

Git viene usualmente pre-instalado en los sistemas operativos Mac y Linux. Teclea el siguiente comando y presiona la tecla enter:

```bash
git -–version
```

Usted debe recibir un mensaje diciéndole cual es la versión de Git que tiene en su computadora. Si usted no recibió un mensaje con la versión del Git, entonces proceda a descargar el Git.

Si Git no se descarga automáticamente, existe otra opción en el sitio web para su descarga manual.

Entonces siga los pasos en la ventana de instalación

Después de haber finalizado la instalación del Git, abre de nueva la Shell y teclea el comando anterior así verificas que se haya instalado correctamente.

```bash
git--version
```
#### 2.4 Configurando Git por primera vez
##### 2.4.1 Agrega tu nombre de usuario de Git y tu correo electrónico

Es importante para configurar el Git su nombre de usuario y la dirección de correo electrónico, desde este momento Git comenzará a utilizar esta información para identificarte como el autor.

En tu shell, teclea el siguiente comando para agregar tu nombre de usuario:

```bash
git config --global user.name "nombre_de_usuario"
```

Entonces verifica que se haya agregado correctamente el nombre de usuario:

```bash
git config --global user.name
```

Para asignar tu dirección de correo electrónico, tecle el siguiente comando:

```bash
git config --global user.email "direccion_de_correo@ejemplo.com"
```

Para verificar que se haya asignado tu correo electrónico correctamente, teclea:

```bash
git config --global user.email
```

##### 3.2.3.2 Verifica tu información
Para ver la información que ha ingresado, tanto como otras opciones globales, teclea:

```bash
git config --global –-list
```

#### 2.5 Comandos básicos de Git

##### 2.5.1 Crea un directorio donde almacenar tus repositorios locales

Para ello teclea el siguiente comando:


```bash
mkdir repositories
```

Asegúrate que se haya creado de forma satisfactoria para ello teclee el siguiente comando:

```bash
ls
```

También puedes utilizar el siguiente en plataforma MS Window:

```bash
dir
```

##### 2.5.2 Accede al directorio de tus repositorios locales

Para entrar en la carpeta creada anteriormente:

```bash
cd repositories
```


##### 2.5.3 Clona el repositorio principal al directorio creado

```bash
git clone https://github.com/user/name-of-project.git
```

Comprueba que se han descargados los archivos correctamente mediante el comando ls o dir.

##### 2.5.4 Muévete a tu rama (branch)

```bash
git checkout name-of-branch
```

Notas:

* Asegúrate de haberla creado previamente desde el entorno web de GitLab.

##### 2.5.5 Descargar los últimos cambios en una rama

Esto es para trabajar en una copia de lo que está al día (es importante hacer esto todo el tiempo que se esté trabajando en el proyecto), mientras usted está al tanto de las ramas se pueden evitar algunos inconvenientes.

```bash
git pull
```
Tambien puedes utilizar el siguiente comando para actualizar una rama especifica.

```bash
git pull name-of-branch
```

##### 2.5.5 Comprobando el estado de tus archivos (status)

Esto es importante para estar cociente de que ha pasado y cuál es el status de sus cambios. Al añadir cambio o eliminar archivos /carpetas, Git sabe acerca de esto. Para verificar el status de sus cambios:

```bash
git status
```

##### 2.5.6 Ver diferencias

Para ver las diferencias entre su local, sus cambios inmediatos y los repositorios de la versión clonada o bajada. Teclee
git diff

##### 2.5.7 Añadir y comentar los cambios locales (commit)

Usted ha visto sus cambios locales en rojo al teclear git status. Los nuevos cambios hechos: modificación o eliminación de archivos/carpetas. Usa git add y añada archivo/carpeta.

Entonces usa git commit para describir el cambio o las mejoras realizadas.

```bash
git add archivos o carpetas
```

```bash
git commit -m "Modifique el template que lista los tipos de disponibilidad, para realizar pruebas desde el git."
```

##### 2.5.8 Enviar cambios al servidor de GitLab o GitHub

Para hacer push de los cambios y comentarios de los cambios realizados.

```bash
git push origin name-of-branch
```

Por ejemplo, para hacer push de sus cambios locales a la rama master agregue la palabra origen remoto.

```bash
git push origin master
```

```bash
git push origin developmet
```

##### 2.5.9 Fusionar ramas

Pasar a la rama que desea fusionar.

Para moverse entre ramas se utiliza el comando "git checkout" seguido del nombre de la rama que queremos que sea la activa, luego agrega el comando con la rama que desea adsorbe o fusionar con la primera.

```bash
git checkout master
```

```bash
git merge name-of-branch-for-merge
```


### Glosario

#### ¡En Construcción!

