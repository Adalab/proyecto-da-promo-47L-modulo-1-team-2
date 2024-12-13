<<<<<<< HEAD
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


=======

# Grupo 2 - Promo L47

## **Integrantes del equipo**
- **Elena Alique Baumann**  
- **Antonia Aguiar Gordillo**  
- **Rosa Cardoso Gomes**  
- **Neyde Gabriela Fernández Meza**  


 

## **Sobre nuestro grupo**
<font color="blue">Somos un equipo comprometido con el aprendizaje y el desarrollo de soluciones creativas en programación. Este repositorio es un espacio colaborativo donde plasmaremos nuestras ideas y avanzaremos juntas hacia el éxito.</font>  

> **"El talento gana juegos, pero el trabajo en equipo y la inteligencia ganan campeonatos." – Michael Jordan**

¡Sigamos aprendiendo, creciendo y apoyándonos mutuamente en este emocionante camino! 🚀✨

##### Este proyecto tiene como objetivo el desarrollo de tres juegos clásicos: Preguntas y Respuestas, Juego del Ahorcado y Piedra, Papel o Tijera. El propósito de este trabajo es crear una experiencia interactiva y divertida que permita a los jugadores disfrutar de juegos tradicionales mediante la programación.

##### El proyecto fue realizado en grupo, y cada miembro del equipo contribuyó con diferentes tareas.El juego de Preguntas y Respuestas ofrece un formato de trivia, mientras que el Juego del Ahorcado desafía a los jugadores a adivinar palabras con un número limitado de intentos. Finalmente, el clásico Piedra, Papel o Tijera es una competencia simple entre dos jugadores.

##### A través de este proyecto, nuestro equipo ha podido aprender y aplicar conceptos de programación, trabajar en colaboración y desarrollar juegos sencillos pero entretenidos que pueden ser disfrutados por cualquier persona.


1. **Preguntas y Respuestas**  
2. **Juego del ahorcado** 
3. **Piedra, Papel o Tijera**



# Preguntas y Respuestas


- Reglas del Juego de "Preguntas y Respuestas de Geografía":
    - El juego consiste en hacer preguntas de geografía y que el jugador adivine la respuesta correcta.

    - Cada pregunta tiene una respuesta única y correcta.

    - El jugador tiene un número limitado de intentos para responder correctamente a cada pregunta.

    - El juego sigue hasta que el jugador responda incorrectamente 3 de veces o haya respondido 5 preguntas correctamente.


# Piedra Papel & Tijera

- Reglas del Juego "Piedra, Papel y Tijera":

    - Dos jugadores eligen una de las tres opciones: "Piedra", "Papel" o "Tijera".

    - Las reglas para determinar al ganador son:
        
        - Piedra vence a Tijera.

        - Tijera vence a Papel.

        - Papel vence a Piedra.

        - El jugador que gana una ronda obtiene un punto.
        
        - El juego continúa hasta que un jugador haya acumulado 3 puntos, convirtiéndose en el ganador.


        # Ahorcado

- Reglas del juego del "Ahorcado":

    - Un jugador elige una palabra secreta y dibuja un espacio para cada letra de la palabra.

    - El otro jugador intenta adivinar letras para completar la palabra.

    - Si el jugador adivinador adivina una letra correctamente, se revela en su lugar correspondiente.

    - Si el jugador adivinador adivina incorrectamente, se dibuja una parte del cuerpo en la horca.

    - El objetivo del jugador adivinador es adivinar la palabra antes de que se dibuje el dibujo completo en la horca.
>>>>>>> 78ac86ad4e1ea6dccc3ca553c3452d3bfc4cdf28
