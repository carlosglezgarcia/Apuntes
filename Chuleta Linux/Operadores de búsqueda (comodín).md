En este caso voy a poner ejemplos y los voy a explicar más que poner los operadores de búsqueda sin más.

| Comodín  | Descripción                                                                               |
| -------- | ----------------------------------------------------------------------------------------- |
| `?`      | Esto se intercambia por cualquier carácter pero solo una vez                              |
| `*`      | Esto significa cualquier carácter, ninguna, una y más veces                               |
| `[abc]`  | Esto significa cualquiera de los caracteres entre corchetes, pero solo uno y solo una vez |
| `[^abc]` | Todo lo que NO empiece por ninguno de los caracteres entre corchetes, pero solo uno       |

Los últimos no lo explico muy bien pero en los ejemplos quedará mejor.

- Ejemplos de uso:

> `ls -d /home/carlos/*` $=>$ Esto dará como resultado todos los archivos y directorios
> que contenga la carpeta `carlos` excepto los ocultos, de esta forma con el asterisco
> estoy filtrando por cualquier carácter y cualquier longitud.

> `ls -d /home/carlos/M?????` $=>$ Esto dará como resultado, en mi caso que solo
> tengo esa carpeta que coincida con esa expresión, `# /home/carlos/Música`.

> [!IMPORTANT]
> El resultado de `# /home/carlos/Música` se obtiene por escribir la ruta completa, si
> escribimos la ruta desde el directorio `carlos` (el usuario que tenga cada uno),
> por ejemplo `ls -d ./M?????` esto dará como resultado `# ./Música`.

> `ls -d /dev/tty*[1-5]` $=>$ Este patrón dará como resultado cualquier archivo o
> directorio que comience con `tty` tenga cualquier cadena de caracteres de por
> medio y termine en números del 1 al 5 incluyendo a estos.
> `# tty_cadena_cualquiera_1`
> `# tty_cadena_cualquiera_2`
> `# tty_cadena_cualquiera_3`
> `# tty_cadena_cualquiera_4`
> `# tty_cadena_cualquiera_5`

> `ls -d /etc/[^t]*` $=>$ El resultado será cualquier archivo o directorio que NO
> comience con la letra `t` sin importar la longitud del nombre del archivo o directorio.