> `cp` $=>$ copia archivos y directorios.

- Notación del comando:

> `cp [OPCIÓN]... [-T] ORIGEN DEST`
> `cp [OPCIÓN]... ORIGEN... DIRECTORIO`
> `cp [OPCIÓN]... -t DIRECTORIO ORIGEN`

- Opciones del comando:

> `-t`, `--target-directory=DIRECTORIO` $=>$ Copia todos los argumentos `ORIGEN` al `DIRECTORIO`.

> `-T`, `--no-target-directory` $=>$ trata `DESTINO` como archivo normal.

Como tampoco los he probado no puedo explicar muy bien estas 2 opciones, de momento quedarán ahí por darle un poco más de información a la notación del comando.

- Ejemplos:
> `cp /etc/rc.d/* PRUEBA/dir3/dir31` $=>$ `cp` puede copiar varios archivos o directorios pero a la hora de querer copiar algo debemos tener en cuenta que de todas las rutas que le entreguemos al comando se copiará todo en la última ruta que exista.

