# Programación de 1º

Aquí pondré algo que pueda ayudar a quién necesite con Programación de primero.

## POO

Para poder entender un poco mejor lo que es la **programación
orientada a objetos** quiero poner un ejemplo que se salga un poco
de lo que siempre nos enseñan diciendo que hay que "abstraerse".

Bien, se supone que debemos entender que en programación un objeto
puede ser cualquier cosa. Un ejemplo puede ser una "Sugerencia":

```py
class Sugerencia:
    def __init__(self, sugerencia: str, motivo: str):
        self.sugerencia = sugerencia
        self.motivo = motivo

    def sugerir(self):
        print(f"{self.sugerencia}, {self.motivo}")


sugerencia1 = Sugerencia("Sonríe", "nos están sacando una foto")
sugerencia1.sugerir()
# Sonríe, nos están sacando una foto.
```

Esto es solo un ejemplo de como cualquier cosa puede ser un objeto
y nosotros podemos darle unos atributos (sugerencia, motivo) y hacer que tenga
unos métodos (sugerir), de esta forma cualquier cosa puede ser un objeto
o lo podemos entender como tal.

También un pensamiento podría servir como ejemplo de objeto,
no tiene porqué ser algo tangible, tampoco tenemos que crear algo completo
nada más declarar la clase.

```py
class Pensamiento:
    def __init__(self, tipo = "recomendación"):
        self.tipo = tipo

psmto = Pensamiento()
print(psmto.tipo) # recomendación
psmto.tipo = "aviso"
print(psmto.tipo) # aviso
```

Aquí por ejemplo pongo un objeto muy a medias pero que podemos inicializar sin
asignarle ningún atributo. De todas formas de esta manera podemos seguir
ampliando el objeto con atributos y métodos.
