# proyecto-da-promo-47L-modulo-1-team-2.
# Grupo 2 - Promo L47

## **Integrantes del equipo**
- **Elena Alique Baumann**  
- **Antonia Aguiar Gordillo**  
- **Rosa Cardoso Gomes**  
- **Neyde Gabriela Fernández Meza**  

## **Proyectos del grupo**
1. **Preguntas y Respuestas**  
2. Proyecto aún por definir  
3. Proyecto aún por definir  
4. Proyecto aún por definir  

## **Sobre nuestro grupo**
Somos un equipo comprometido con el aprendizaje y el desarrollo de soluciones creativas en programación. Este repositorio es un espacio colaborativo donde plasmaremos nuestras ideas y avanzaremos juntas hacia el éxito.  

> **"El talento gana juegos, pero el trabajo en equipo y la inteligencia ganan campeonatos." – Michael Jordan**

¡Sigamos aprendiendo, creciendo y apoyándonos mutuamente en este emocionante camino! 🚀✨



```python

#Juego Adivina Capitales Europeas

capitales = [
    ("Rusia", "Moscú"),
    ( "Italia", "Roma"),
    ("España", "Madrid"),
    ( "Lituania", "Vilna"),
    ("Rumania", "Bucarest")
]

puntos = 0
indice = 0


while indice < len(capitales):
    pais, capital = capitales[indice]
    print(f"¿Cuál es la capital de {pais}?")
    
    respuesta = input("Tu respuesta (o escribe 'salir' para terminar): ")
    
    if respuesta.lower() == "salir":
        print("Saliste del juego.")
        break
    if respuesta.lower() == capital.lower():
        print("¡Correcto!")
        puntos += 1
    else:
        print(f"Incorrecto, la respuesta correcta es: {capital}")
    indice += 1
    
print(f"Juego terminado. Obtuviste {puntos} puntos.")


--------------------------------------------------------


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


# Selección de palabra y configuración inicial
palabra = random.choice(lista_palabras)
tablero = ["_"] * len(palabra)
intentos_fallidos = 0

print("¡Bienvenido al Ahorcado!")
print(dibujo_horca[intentos_fallidos])
print(" ".join(tablero))

# Juego principal
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




--------------------------------------------------------

#Juego Piedra Papel Tijera

import random

import random

# Configuración inicial
puntos_jugador = 0
puntos_computadora = 0
puntos_objetivo = 3

print("¡Bienvenido al juego Piedra, Papel y Tijera!")

# Bucle principal del juego
while puntos_jugador < puntos_objetivo and puntos_computadora < puntos_objetivo:
    print(f"Puntos - Jugador: {puntos_jugador}, Computadora: {puntos_computadora}")

    # Elección del jugador
    opciones = ["piedra", "papel", "tijera"]
    jugador = input("Elige piedra, papel o tijera: ").lower()
    while jugador not in opciones:
        print("Opción no válida. Intenta de nuevo.")
        jugador = input("Elige piedra, papel o tijera: ").lower()

    # Elección de la computadora
    computadora = random.choice(opciones)

    print(f"Tú elegiste: {jugador}")
    print(f"La computadora eligió: {computadora}")

    # Determinar el ganador
    if jugador == computadora:
        print("¡Es un empate!")
    elif (jugador == "piedra" and computadora == "tijera") or \
         (jugador == "tijera" and computadora == "papel") or \
         (jugador == "papel" and computadora == "piedra"):
        puntos_jugador += 1
        print("¡Ganaste esta ronda!")
    else:
        puntos_computadora += 1
        print("La computadora ganó esta ronda.")

# Resultado final
if puntos_jugador == puntos_objetivo:
    print("¡Felicidades! Ganaste el juego.")
else:
    print("La computadora ganó el juego. Mejor suerte la próxima vez.")

