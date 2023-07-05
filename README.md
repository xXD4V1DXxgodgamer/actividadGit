# **Actividad Git**

### **¿Qué es Git?**<br><br>
  Git es el sistema de control de versiones moderno más utilizado del mundo. Es un proyecto de código abierto maduro y con un mantenimiento activo desarrollado por Linus Torvalds, el creador del kernel del sistema operativo Linux. Un asombroso número de proyectos de software dependen de Git para el control de versiones, incluidos proyectos comerciales y de código abierto. Los sistemas de control de versiones son herramientas de software que ayudan a los equipos de software a gestionar los cambios en el código fuente a lo largo del tiempo.
  
  Git permite controlar todos los cambios que se hacen en nuestra aplicación y en nuestro código y vamos a tener control absoluto de todo lo que pasa en el código, pudiendo volver atrás en el tiempo, pudiendo abrir diferentes ramas de desarrollo, etc.
  Vamos a poder trabajar en equipo de una manera muy sencilla y optimizada,con más personas trabajando en un mismo proyecto. Al terminar nuestro código, usamos Git para mezclar los cambios con los otros compañeros. Así el código se mezcla de manera perfecta sin generar ningún tipo de fallo y de forma rápida.

### **Instalación de Git**

***Windows***<br>
Descarga el instalador de GIT para Windows.
Una vez que hayas descargado el instalador, haz doble clic sobre el ejecutable para que comience el proceso de instalación y sigue las instrucciones que te aparecerán en pantalla. Al igual que cualquier otro programa, tendrás que dar “Next” (siguiente) en varias ocasiones hasta que aparezca la opción “Finish” (terminar) para completar la instalación.<br>
Ahora tienes que abrir el símbolo de sistema y escribir los siguientes comandos en la terminal:<br><br>
~git config --global user.name "Tu nombre"<br>
~git config --global user.email "ejemplo@email.com"<br><br>
***MacOS***<br>
Descarga el instalador oficial para Mac.
Sigue las instrucciones que te aparecerán en el programa de instalación.<br>
Al finalizar el proceso de instalación del instalador, vuelve a revisar usando el comando git – -version para confirmar si la instalación se ha hecho correctamente.<br>
Ahora ejecuta los siguientes comandos en la terminal para configurar tu correo y el nombre de usuario que están asociados a tu cuenta GIT:<br><br>
~git config --global user.name "Tu nombre"

~git config --global user.email "ejemplo@email.com"

***Linux***<br>
Abre la terminal y ejecuta los siguientes comandos:<br>
~Sudo apt-get update

~sudo apt-get install git


Verifica que la instalación se haya hecho correctamente usando el comando:       git –version.<br>
A continuación, ejecuta los siguientes comandos en la terminal para poder configurar tu correo y nombre de usuario que están asociados a tu cuenta GIT:<br>
 git config --global user.name "Tu nombre"

git config --global user.email "ejemplo@email.com".


### **Configuración de Git**

***Nombre de usuario***<br>
Abra la Terminal.
Establece un nombre de usuario en Git:
~$ git config --global user.name "David"
Confirma que has establecido correctamente el nombre de usuario en Git:
~$ git config --global user.name<br>
.> David<br><br>
***Correo electrónico***<br>
Abra Terminal.<br>
Configurar una dirección de correo electrónico en Git. Puede usar la dirección de correo electrónico noreply proporcionada por GitHub o cualquier dirección de correo electrónico.

~$ git config --global user.email "TU_EMAIL"

Confirma que has establecido correctamente la dirección de correo electrónico en Git:

~$ git config --global user.email
email@example.com

Agregue la dirección de correo electrónico a su cuenta en GitHub, de modo que las confirmaciones se le atribuyan y aparezcan en el gráfico de contribuciones. Para obtener más información.


### **Comandos básicos de Git**

***git init:*** El comando "git init" se utiliza para crear un nuevo repositorio Git en un directorio específico. Cuando ejecutas este comando, Git inicializa un repositorio vacío en la ubicación actual y crea una carpeta oculta llamada ".git" que contiene todos los archivos y metadatos necesarios para el control de versiones.

***git add:*** El comando "git add" se utiliza para agregar archivos o cambios específicos al área de preparación (también conocida como "index") de Git. El área de preparación es donde se seleccionan los cambios que se incluirán en el próximo commit.}

***git commit:*** El comando "git commit" se utiliza para crear un nuevo commit (una instantánea de los cambios) en el repositorio. Un commit en Git representa un conjunto de cambios que se guardan permanentemente en la historia del proyecto.

***git status:*** El comando "git status" muestra el estado actual del repositorio Git. Proporciona información sobre los archivos modificados, los archivos que han sido agregados al área de preparación, los cambios sin rastrear y otros detalles relevantes.


	


***git log:*** El comando "git log" se utiliza para ver el historial de commits en un repositorio Git. Muestra una lista de commits realizados, en orden cronológico inverso, lo que significa que los commits más recientes aparecerán primero.<br>
"--oneline": Muestra cada commit en una sola línea, con información resumida.<br>
"--graph": Muestra una representación gráfica de las ramificaciones del repositorio.<br>
"--author": Filtra los commits por autor específico.<br>
"--since" y "--until": Filtran los commits por rango de fechas.

***git diff:*** El comando "git diff" se utiliza para mostrar las diferencias entre versiones, ya sea entre archivos sin seguimiento y el área de preparación, o entre el área de preparación y la última versión confirmada (commit).<br>
Cuando ejecutas "**git diff**" sin opciones, muestra las diferencias entre los archivos modificados pero no agregados al área de preparación. Esto te permite ver los cambios que aún no se han incluido en un commit.<br>
"--cached": Muestra las diferencias entre el área de preparación y el último commit.<br>
"< commit >": Compara el estado actual con un commit específico.<br>
"< branch1 > < branch2 >": Compara dos ramas diferentes del repositorio.





### **Trabajando con repositorios remotos**

***Clonar un repositorio remoto***<br>
Abra Terminal.


Cambia el directorio de trabajo actual a la ubicación en donde quieres clonar el directorio.


Escriba “git clone” y pegue la dirección URL del repositorio.
	~$ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
  
 Presione Entrar para crear el clon local.
	~$ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY<br><br>
.> Cloning into `Spoon-Knife`...<br>
.> remote: Counting objects: 10, done.<br>
.> remote: Compressing objects: 100% (8/8), done.<br>
.> remove: Total 10 (delta 1), reused 10 (delta 1)<br>
.> Unpacking objects: 100% (10/10), done.<br>

***Trabajar con ramas***<br><br>
***git branch:*** El comando "git branch" se utiliza para administrar y listar las ramas en un repositorio Git.<br>
Para listar las ramas existentes en el repositorio, simplemente ejecuta el comando **"git branch"**. La rama actual se resaltará con un asterisco (*).<br>
Para crear una nueva rama, puedes utilizar **"git branch"** seguido del nombre de la nueva rama. Por ejemplo, "git branch nueva-rama" creará una nueva rama llamada "nueva-rama".<br>
Puedes utilizar la opción "-d" junto con "git branch" para eliminar una rama. Por ejemplo, "git branch -d rama-a-borrar" eliminará la rama llamada "rama-a-borrar".

***git checkout:*** El comando **"git checkout"** se utiliza para cambiar entre ramas o para crear una nueva rama y cambiar a ella al mismo tiempo.<br>
Para cambiar a una rama existente, ejecuta "git checkout" seguido del nombre de la rama.<br> Por ejemplo, **"git checkout nombre-de-rama"** cambiará a la rama llamada "nombre-de-rama".<br>
Para crear una nueva rama y cambiar a ella al mismo tiempo, utiliza "git checkout -b" seguido del nombre de la nueva rama. Por ejemplo, "git checkout -b nueva-rama" creará una nueva rama llamada "nueva-rama" y cambiará a ella.

***git merge:*** El comando "git merge" se utiliza para fusionar cambios de una rama a otra. Es común fusionar una rama secundaria en la rama principal (por lo general, la rama "master" o "main").<br>
Asegúrate de estar en la rama de destino (la rama en la que deseas fusionar los cambios). Puedes usar "git branch" para verificar la rama actual y "git checkout" para cambiar a la rama deseada.<br>
Ejecuta "git merge" seguido del nombre de la rama que deseas fusionar. Por ejemplo, "git merge nombre-de-rama" fusionará los cambios de la rama "nombre-de-rama" en la rama actual.
Cambios a un repositorio remoto.

El comando git push toma dos argumentos:<br>
Un nombre remoto, por ejemplo, **origin**<br>
Un nombre de rama, por ejemplo, **main**<br>
Por ejemplo:<br>
**~$ git push REMOTE-NAME BRANCH-NAME**

Para cambiar el nombre de una rama, tendría que usar el mismo comando git push, pero agregar un argumento más: el nombre de la nueva rama.<br>
 Por ejemplo:<br>
**~$ git push REMOTE-NAME LOCAL-BRANCH-NAME:REMOTE-BRANCH-NAME**

De manera predeterminada, y sin parámetros adicionales, git push envía todas las ramas que coinciden para que tengan el mismo nombre que las ramas remotas.<br>
Para subir una etiqueta única, puedes emitir el mismo comando que al subir una rama:<br>
**~$ git push REMOTE-NAME TAG-NAME**<br>
Para subir todas tus etiquetas, puede escribir el comando:<br>
**~$git push REMOTE-NAME --tags**

***Para borrar una rama***
	
	~$ git push REMOTE-NAME :BRANCH-NAME