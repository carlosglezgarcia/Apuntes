> `ls` $=>$ lista el contenido de un directorio

- Notación del comando:

> `ls [OPCIÓN]... [ARCHIVO]...`

- Opciones del comando:

> `-d`, `--directory` $=>$ muestra los propios directorios, no su contenido.

```sh
ls --directory /home/carlos/D????????
# /home/carlos/Descargas
```

> [!NOTE]
> Si en este caso no utilizamos `--directory` cuando encontrase el directorio que coincida con ese patrón listaría todo su contenido.

> `-l` $=>$ utiliza un formato de listado largo que aporta más información de archivos y carpetas.

```shell
ls -l /home/carlos/Descargas
# .rw-r--r-- carlos carlos 98 B Sun May 26 17:39:57 2025 mi_texto.txt
```

> `-a`, `--all` $=>$ no oculta las entradas al guardar.

```shell
ls -a /home/carlos/Descargas
# .
# ..
# .carpeta_de_matemáticas
# mi_texto.txt
```

> [!IMPORTANT]
> En Linux se considera un archivo oculto a los que empiezan por "." (punto).

> `-r`, `--reverse` $=>$ invierte el orden

```shell
ls -ar /home/carlos/Descargas
# mi_texto.txt
# .carpeta_de_matemáticas
# ..
# .
```

> [!NOTE]
> En Linux puedes concatenar más de una opción, también pueden escribirse las opciones por separado o incluso la opción completa.
> `ls --reverse --all /home/carlos/Descargas`
> `ls --reverse -a /home/carlos/Descargas
> `ls -r -a /home/carlos/Descargas`
> Todas estas opciones son válidas.

> `-i`, `--inode` $=>$ muestra el número de índice (i-node) de cada archivo.

```shell
ls -i $HOME/Descargas/PRUEBA
# 4330165 dir1
# 4330167 dir2
# 4330168 dir3
```

El número nos muestra el índice de cada archivo o directorio.

> [!NOTE]
> En bash para poder utilizar el valor de una variable se utiliza el símbolo `$` (shift+4) y `HOME` es una variable interna de Linux que contiene `/home/carlos` en mi caso, en caso de otro usuario será `/home/nombre_usuario`, por lo tanto el comando hace la misma función que `ls -i /home/nombre_usuario`.