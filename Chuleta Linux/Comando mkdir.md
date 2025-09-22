> `mkdir` $=>$ crea directorios

- Notación del comando:

> `mkdir [OPCIÓN]... DIRECTORIO...

- Opciones del comando:

> `-p`, `--parents` $=>$ No lanza un error si existe el directorio intermedio, si no
> existe lo crea.

- Ejemplo:

```shell
ls PRUEBA
# dir2
# dir3
mkdir -p PRUEBA/dir1/dir11
ls PRUEBA/*
# PRUEBA/dir1:
# dir11

# PRUEBA/dir2:

# PRUEBA/dir3:
# dir31
```

De esta forma si no existe la carpeta `dir1`, la crea, además de crear la carpeta `dir11`, si no se escribe la opción `-p` nos lanzará un error si la carpeta `dir1` no existe.

Para poder crear de forma rápida carpetas con `mkdir` podemos utilizar atajos mediante llaves:

```shell
mkdir -p PRUEBA/{dir1/dir11,dir2,dir3/dir31/{dir311,dir312}}
```

> De esta forma podemos crear el árbol de directorios
> PRUEBA
> ├── dir1
> │   └── dir11
> ├── dir2
> └── dir3
>     └── dir31
>         ├── dir311
>         └── dir312