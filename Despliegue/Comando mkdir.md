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

```
De esta forma podemos crear el árbol de directorios:
PRUEBA
├── dir1
│    └── dir11
├── dir2
└── dir3
    └── dir31
        ├── dir311
        └── dir312
```

Si desglosamos el comando anterior lo que realmente estamos haciendo es una sucesión de comandos:

```bash
mkdir -p PRUEBA/dir1/dir11
mkdir -p PRUEBA/dir2
mkdir -p PRUEBA/dir3/dir31/dir311
mkdir -p PRUEBA/dir3/dir31/dir312
```

Con las llaves lo que hacemos es entregarle una lista de direcciones que se pondrán al nivel en el que nosotros le asignemos con la barra, como dentro de `dir31` hay 2 carpetas en el mismo nivel se pone otra lista en el siguiente nivel de `dir31`.

> [!CAUTION]
> En bash no se dejan espacios entre llaves o luego de comas, lo toma como órdenes distintas.
