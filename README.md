# proyecto-da-promo-47L-modulo-1-team-2.

````python

# Juego Adivina Capitales Europeas

capitales = {
    "Rusia": "Moscú",
    "Italia": "Roma",
    "España": "Madrid",
    "Lituania": "Vilna",
    "Rumania": "Bucarest"
}

puntos = 0
indice = 0
paises = list(capitales.keys())

print("¡Bienvenida al juego: Adivina Capitales Europeas!")
print("Para finalizar el juego escribe: salir")

while True:
    if indice >= len(paises):
        print("Has terminado todas las preguntas.")
        print(f"Juego terminado. Obtuviste {puntos} puntos.")
        break

    pais = paises[indice]
    capital = capitales[pais]
    print(f"¿Cuál es la capital de {pais}?")
    respuesta = input("Tu respuesta (o escribe 'salir' para terminar): ")
    
    if respuesta.lower() == "salir":
        print("Saliste del juego.")
        print(f"Juego terminado. Obtuviste {puntos} puntos.")
        break
    
    if respuesta.lower() == capital.lower():
        print("¡Correcto!")
        puntos += 1
    else:
        print(f"Incorrecto, la respuesta correcta es: {capital}")
    
    indice += 1



#Juego del ahorcado

import random

lista_palabras = ["perro", "alcachofa", "ratón", "jarra", "anillo"]
dibujo_horca = [
    """
      ------
      |    |
           |
           |
           |
           |
    =========
    """,
    """
      ------
      |    |
      O    |
           |
           |
           |
    =========
    """,
    """
      ------
      |    |
      O    |
      |    |
           |
           |
    =========
    """,
    """
      ------
      |    |
      O    |
     /|    |
           |
           |
    =========
    """,
    """
      ------
      |    |
      O    |
     /|\\   |
           |
           |
    =========
    """,
    """
      ------
      |    |
      O    |
     /|\\   |
     /     |
           |
    =========
    """,
    """
      ------
      |    |
      O    |
     /|\\   |
     / \\   |
           |
    =========
    """
]


palabra = random.choice(lista_palabras)
tablero = ["_"] * len(palabra)
intentos_fallidos = 0

print("¡Bienvenido al Ahorcado!")
print(dibujo_horca[intentos_fallidos])
print(" ".join(tablero))

while intentos_fallidos < len(dibujo_horca) - 1:
    letra = input("Adivina una letra: ").lower()

    if letra in palabra:
        for i, l in enumerate(palabra):
            if l == letra:
                tablero[i] = letra
        print("¡Correcto!")
    else:
        intentos_fallidos += 1
        print("¡Fallaste!")

    print(dibujo_horca[intentos_fallidos])
    print(" ".join(tablero))

    if "_" not in tablero:
        print("¡Ganaste! La palabra era:", palabra)
        break
else:
    print("¡Perdiste! La palabra era:", palabra)


