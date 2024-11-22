---
author: Andrea Gómez Fueyo
title: Ejercicio de Git - proyecto labowebs
---

# Ejercicio de Git - proyecto labowebs

> Realizado por Andrea Gómez Fueyo

[TOC]

<div style="page-break-after: always; break-after: page;"></div>

## TRABAJO EN LOCAL

### EJERCICIO 1

**Inicializa un nuevo repositorio Git en una carpeta llamada `"labowebs"` y agrega los**
**archivos proporcionados en el aula virtual. Renombra la rama master a `main` , si es**
**necesario. Realiza el primer commit. Muestra el log del repositorio.**

Antes de nada, descargamos la carpeta `"labowebs"` del campus virtual, la descomprimimos y abrimos desde ella Git.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114091043666-1731571847766-1.png" alt="image-20241114091043666" style="zoom:67%;" />

Una  vez abierto realizamos un `git init` para iniciar un repositorio en dicha carpeta y añadimos los archivos. 

```bash
$ git init
$ git add .
```

![image-20241114091350507](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114091350507-1731572031628-3.png)

Cambiamos el nombre de la rama, realizamos el primer commit y hacemos un `log` para ver que todo está correcto.

![image-20241114091548028](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114091548028-1731572149076-5.png)



##### CAMBIO FICHEROS DESDE VISUAL STUDIO

Tuvimos que realizar unos cambios en algunos de los ficheros descargados.

```bash
$ git add .
$ git commit -m "cambio en los archivos hechos de forma manual desde visual studio"
```

![image-20241114092549278](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114092549278-1731572751264-7.png)



### EJERCICIO 2

**Incluye un fichero `.gitignore` para que los ficheros `README.md` , `LICENCE.txt` y**
**`passwords.txt` sean ignorados por el control de versiones. Realiza el commit y muestra**
**los logs del repositorio en una línea.**

Creo el fichero y utilizo `nano` para editarlo.

```bash
$ touch .gitignore
```

![image-20241114093104659](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114093104659-1731573066399-13.png)

```bash
$ nano .gitignore
```

![image-20241114093032194](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114093032194-1731573032967-11.png)

![image-20241114092947594](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114092947594-1731572988772-9.png)

Guardo el archivo `.gitignore` y hago un commit explicando lo que contiene.

```bash
$ git add .gitignore
$ git commit -m "añadido .gitignore para ignorar README.md, LICENCE.txt y passwords.txt"
```

![image-20241114093429927](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114093429927-1731573271046-15.png)



### EJERCICIO 3

**En el repositorio, crea los archivos `README.md` , `LICENCE.txt` y `passwords.txt` con**
**algún contenido. Muestra el estado del repositorio. Muestra el listado de archivos**
**ignorados.**

```bash
$ echo "hola archivo README" > README.md
$ echo "hola archivo LICENCE" > LICENCE.txt
$ echo "contraseña: hola123" > passwords.txt
```

![image-20241114093812667](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114093812667-1731573493757-17.png)

![image-20241114094329142](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114094329142-1731573810171-19.png)



### EJERCICIO 4

**Crea una rama `feature-estilos` . Cámbiate a ella.**

- **Modifica el archivo `estilos.css` :**

  - **propiedad color del `body` y de `h2` : `#2a2a2a`**
  - **propiedad `background-color` de `header` y `footer`: `#2a75ff`**

  Al crear la rama `feature-estilos` cometí un error al introducir el nombre, lo cambié a través del comando `git branch -m`.

  ```bash
  $ git checkout -b featyre-estilos
  $ git branch -m feature-estilos
  ```

  ![image-20241114094554849](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114094554849-1731573955830-21-1731574038913-23.png)

Para modificar el archivo `estilos.css` utilicé `nano`.

![image-20241114095222694](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114095222694-1731574343818-27.png)

![image-20241114095140511](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114095140511-1731574302344-25.png)

- **Comprueba el estado del repositorio. Añade los cambios, realiza un commit con el**
  **mensaje "actualizados estilos a azules".**

Comprobamos que el sistema reconoció los cambios realizados en `estilos.css` 

```bash
$ git status
$ git add estilos.css
```

![image-20241114095805256](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114095805256-1731574686326-29.png)

Una vez comprobados y añadidos los cambios, realizamos un commit y un `log`.

```bash
$ git commit -m "actualizados estilos a azules"
$ git log --oneline
```

![image-20241114095834608](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114095834608-1731574715440-31.png)



### EJERCICIO 5

**Vuelve a la rama `main` . En el archivo `index.html` añade un comentario donde se indique**
**tu nombre como autor de la página. Comprueba el estado del repositorio. Añade los**
**cambios, realiza un commit con el mensaje ' añadido autor en index'. Muestra los logs del**
**repositorio en una línea, gráficamente y con 'decoración'**

Compruebo la rama en la que estoy a través de `branch` y al ver que no estoy en `main` cambio a ella con `checkout`.

```bash
$ git branch
$ git checkout main
```

![image-20241114100911199](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114100911199-1731575352327-33-1731575394800-35.png)

![image-20241114101731016](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114101731016-1731575851867-39.png)

![image-20241114101502555](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114101502555-1731575704312-37.png)

![image-20241114101757927](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114101757927-1731575878930-41.png)

![image-20241114101815048](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114101815048-1731575895920-43.png)



### EJERCICIO 6

**Fusiona la rama `feature-estilos` en la rama `main` . Muestra los logs del repositorio en**
**una línea, gráficamente y con 'decoración'**.

```bash
$ git branch
$git merge feature-estilos
```

![image-20241114102013213](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114102013213-1731576014735-47.png)

Se abre este archivo en el block de notas.

![image-20241114101926669](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241114101926669-1731575967565-45.png)

Comprobamos si funcionó:

```bash
$ git log --oneline --graph --decorate
```

![image-20241115084110129](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115084110129-1731656471193-1.png)



<div style="page-break-after: always; break-after: page;"></div>

<div style="page-break-after: always; break-after: page;"></div>

## TRABAJO EN REMOTO

### EJERCICIO 1

**Continúa con el repositorio `labowebs` . Añade el repositorio a Sourcetree.**

Para añadir el repositorio a Sourcetree voy al "+" y selecciono la carpeta `"labowebs"`.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115090857894-1731658139198-26.png" alt="image-20241115090857894" style="zoom:67%;" />



<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115085016147-1731657017542-3.png" alt="image-20241115085016147" style="zoom: 67%;" />

Una vez seleccionada nos aparece esto y damos al OK.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115085032327-1731657033532-5.png" alt="image-20241115085032327" style="zoom:67%;" />

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115085107800-1731657068875-7.png" alt="image-20241115085107800" style="zoom: 33%;" />



### EJERCICIO 2

**Crea un repositorio remoto y sube al remoto los ficheros de tu repositorio local. Debes
subir todas las ramas.**

Abrimos nuestra cuenta de Github y desde el inicio creamos el nuevo repositorio vacío `labowebs`.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115091528016-1731658529828-28.png" alt="image-20241115091528016" style="zoom:50%;" />

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115085544361-1731657346034-11.png" alt="image-20241115085544361" style="zoom: 33%;" />

Una vez creado abrimos Sourcetree para vincular el respositorio. Desde `REPOSITORY` en el menú superior vamos a `Repository Settings...` y nos aparece una pantalla.

![image-20241115085730228](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115085730228-1731657451432-13.png)

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115085824814-1731657506427-15.png" alt="image-20241115085824814" style="zoom: 50%;" />

Clickamos en `Add`. Ponemos como  nombre `origin` (Github es el nombre que usa para el repositorio remoto principal) y copiamos la URL del repositorio de Github.

```http
https://github.com/andreafueyo/labowebs.git
```

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115085914184-1731657555447-17.png" alt="image-20241115085914184" style="zoom: 67%;" />

Una vez hecho, damos a OK y hacemos un `PUSH`. Nos aparece esta ventana, seleccionamos todas las ramas y lo enviamos.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115090035175-1731657636424-19.png" alt="image-20241115090035175" style="zoom:50%;" />

Comprobamos que se haya subido correctamente:

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115090125205-1731657686198-21.png" alt="image-20241115090125205" style="zoom:50%;" />



### EJERCICIO 3

**Crea una rama feature-index . Añade el siguiente código dentro de la `<section
class="about">` . Añade los cambios y crea un commit. Sube los cambios al remoto.**

Compruebo que esté en `main` haciendo click derecho y pulsando en `checkout main`. Una vez comprobado, pulsamos `BRANCH`.

![image-20241120131943476](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241120131943476-1732105185363-1.png)

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241120132631071-1732105593012-3.png" alt="image-20241120132631071" style="zoom:50%;" />

Abro el archivo `index` en el Visual Studio Code, añado el texto en el apartado `<section class="about">` y guardo los cambios.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115093525021-1731659726861-30.png" alt="image-20241115093525021" style="zoom:50%;" />

En Sourcetree voy a `File Status` y compruebo que hay cambios sin actualizar. Lo selecciono y pulso `Stage Selected`.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121000524718-1732143929096-5.png" alt="image-20241121000524718" style="zoom:50%;" />

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121000749156-1732144071013-7-1732144222149-9.png" alt="image-20241121000749156" style="zoom: 50%;" />

Para subir los cambios, pulso en `PULL` y añado un comentario notificando que realicé cambios en `index.html`. Compruebo los cambios.

![image-20241121001146522](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121001146522-1732144308043-11.png)

![image-20241121001217594](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121001217594-1732144339515-13.png)

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121001300308-1732144381949-15.png" alt="image-20241121001300308" style="zoom:50%;" />

Subo los cambios al remoto usando `PUSH` y seleccionando la rama que quiero subir.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121001435484-1732144477105-17.png" alt="image-20241121001435484" style="zoom: 50%;" />

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121001534646-1732144535927-19.png" alt="image-20241121001534646" style="zoom: 50%;" />



### EJERCICIO 4

**En el repositorio local, fusiona la rama `feature-index` en la rama `main` .**

Cambio a `main` haciendo click derecho sobre la rama y `checkout main...`. Una vez hecho, selecciono `MERGE`.

![image-20241121002406310](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121002406310-1732145048218-21.png)

![image-20241121002506914](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121002506914-1732145108315-23.png)

![image-20241121002601965](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121002601965-1732145163312-25.png)

![image-20241121002712184](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121002712184-1732145233539-27.png)

### EJERCICIO 5

**Edita el fichero `contacto.html` . Borra unas líneas. Muestra los ficheros con cambios pendientes y las diferencias. Añade los cambios y haz un commit.**

Abro el fichero en Visual Studio Code y borro las lineas 23, 24 y 25.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241115100928087-1731661770703-50.png" alt="image-20241115100928087" style="zoom:50%;" />

Vuelvo a Sourcetree y compruebo el estado, al ver que reconoce los cambios continuo con el commit.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121002936146-1732145377497-29.png" alt="image-20241121002936146" style="zoom:50%;" />



### EJERCICIO 6

**Te das cuenta del error. Deshaz el commit anterior. Captura el estado actual del
repositorio.**

Click derecho en el commit anterior al que quiero eliminar y selecciono `reset current branch to this commit` para que ese sea el último.

![image-20241121005044612](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121005044612-1732146646143-31.png)

![image-20241121005124284](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121005124284-1732146685881-33.png)

Compruebo que se realizó correctamente:

![image-20241121005212655](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121005212655-1732146734925-35.png)



### EJERCICIO 7

**Crea una rama `feature-mapa` . Incluye este código en el archivo `contacto.html` . Añade los cambios. Realiza un commit. Sube los cambios al remoto. Muestra en el remoto los cambios del archivo `contacto.html` en la rama `feature-mapa`.**

Para crear la rama voy a `BRANCH` y escribo `feature-mapa`.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121005530743-1732146932562-37.png" alt="image-20241121005530743" style="zoom:50%;" />

Abro el VisualStudio Code para añadir el código al archivo `contacto.html`

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121005724851-1732147046264-39.png" alt="image-20241121005724851" style="zoom: 50%;" />

Vuelvo a Sourcetree y veo que reconoció los cambios así que realizo un commit para comentarlos.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121005842588-1732147124292-41.png" alt="image-20241121005842588" style="zoom:50%;" />

Hago un `PUSH`.

![image-20241121005939975](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121005939975-1732147181501-43.png)

Compruebo que se están subiendo correctamente a Github.

![image-20241121010121322](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121010121322-1732147282764-45.png)



### EJERCICIO 8

**En GitHub, en la rama `main` , fusiona la rama `feature-mapa` . Baja los cambios del remoto
a local. Deja los dos repositorios sincronizados.**

Desde el repositorio, voy a `pull requests` y selecciono la rama que quiero fusionar, en este caso `feature-mapa`.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121010611758-1732147573895-47.png" alt="image-20241121010611758" style="zoom: 33%;" />

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121010833253-1732147715401-49.png" alt="image-20241121010833253" style="zoom: 50%;" />

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121010922236-1732147763809-51.png" alt="image-20241121010922236" style="zoom:50%;" />

Añado un comentario.

![image-20241121011045082](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121011045082-1732147846889-53.png)

Bajo los cambios al repositorio local a través de `PULL`.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121011238167-1732147960165-55.png" alt="image-20241121011238167" style="zoom:50%;" />

![image-20241121012011502](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241121012011502-1732148413636-57.png)



<div style="page-break-after: always; break-after: page;"></div>

## CONFLICTOS

### EJERCICIO 1

**Crea una rama `hotfix-js` . Cámbiate a ella. Añade este código en el fichero `script.js` .**
**Confirma el cambio y haz un commit. (Fíjate en los números de línea...)**.

Desde `main` entramos en `BRANCH` y creamos la rama `hotfix-js`.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122122121143-1732274482969-1.png" alt="image-20241122122121143" style="zoom:50%;" />

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122122235701-1732274557506-3.png" alt="image-20241122122235701" style="zoom:50%;" />

Abro `script.js` en VisualStudio y realizo los cambios. Vuelvo a Sourcetree donde los cambios aparecer como `Uncommitted Changes` y hago un commit con ellos.

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122122424702-1732274666878-5.png" alt="image-20241122122424702" style="zoom:50%;" />

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122122608977-1732274770776-7.png" alt="image-20241122122608977" style="zoom:50%;" />

### EJERCICIO 2

**Vuelve a la rama `main` . En el fichero `script.js` en las mismas líneas que en la cuestión** **anterior, añade el código siguiente. Confirma el cambio y haz un commit.**

Hago click derecho en `main` y selecciono `checkout main` para cambiar de rama.

![image-20241122190047462](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122190047462-1732298450166-9.png)



![image-20241122192509904](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122192509904-1732299912686-11.png)

<img src="./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122192650854-1732300013224-13.png" alt="image-20241122192650854" style="zoom: 50%;" />

![image-20241122192837511](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122192837511-1732300119300-15.png)





### EJERCICIO 3

**Fusiona la rama `hotfix-js` en `main` . Debe producirse un conflicto. Resuélvelo. Cuando**
**termines la resolución del conflicto sube los cambios al remoto - Deja los repositorios**
**sincronizados.**
Selecciono `MERGE` estando en la rama `main`. Al hacerlo, salta una notificación de alerta.

![image-20241122194442949](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122194442949-1732301084769-17.png)

![image-20241122195012942](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122195012942-1732301418847-19.png)

Hacemos click derecho en el archivo que da error, `resolve conflicts` y `launch external merge tool`.  Al entrar se abre el documento en VisualStudio Code.

![image-20241122195339611](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122195339611-1732301623932-21.png)

![image-20241122200955848](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122200955848-1732302598363-25.png)

Pulsamos sobre el texto azul `Accept script...` marcando así la solución que preferimos.

![image-20241122201702925](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122201702925-1732303025005-27.png)

Guardamos los cambios y volvemos a Sourcetree para realizar el commit y el push de los cambios.

![image-20241122212104728](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122212104728-1732306866986-29.png)

![image-20241122212156914](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122212156914-1732306918718-31-1732306943678-33.png)

El árbol queda así:

![image-20241122212305058](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122212305058-1732306986908-35.png)

Y el repositorio en Github así:

![image-20241122212542185](./Ejercicio-de-Git---proyecto-labowebs.assets/image-20241122212542185-1732307143956-37.png)