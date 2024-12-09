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

# Juego Capitales Europeas con for con opcion salir

preguntas = {"Rusia": "Moscú", "Italia": "Roma", "España": "Madrid", "Lituania": "Vilna", "Rumania":"Bucarest" }
puntos = 0

for pais, capital in preguntas.items():
    print(f"¿Cuál es la capital de {pais}?")
    jugador = input("Tu respuesta: ")

    if jugador.lower() == "salida":
        print("Saliste del juego.")
        break

    if jugador.lower() == capital.lower():
        print("Capital correcta")
        puntos += 1
    else:
        print("Incorrecto, respuesta correcta es: ", capital)

print(f"Game over, ganaste {puntos} puntos") 


# Juego Capitales Europeas con while con opcion salir

preguntas = {"Rusia": "Moscú", "Italia": "Roma", "España": "Madrid", "Lituania": "Vilna", "Rumania": "Bucarest"}
puntos = 0

iterador = iter(preguntas.items())

while True:
    try:
        pais, capital = next(iterador)
        print(f"¿Cuál es la capital de {pais}?")
        jugador = input("Tu respuesta: ")

        if jugador.lower() == "salida":
            print("Saliste del juego.")
            break

        if jugador.lower() == capital.lower():
            print("Capital correcta")
            puntos += 1
        else:
            print("Incorrecto, respuesta correcta es: ", capital)
    except StopIteration:
        break

print(f"Game over, ganaste {puntos} puntos")
