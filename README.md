import random

# Declaración de variables
opcion = ""
nombre = ""
jugador = ""
computadora = ""
seguir = "si"

while opcion != "3":

    print("\n===================================")
    print("     PIEDRA, PAPEL O TIJERA")
    print("===================================")
    print("1. Ver reglas")
    print("2. Iniciar juego")
    print("3. Salir")

    opcion = input("Seleccione una opción: ")

    if opcion == "1":

        print("\n========== REGLAS ==========")
        print("1. Piedra gana a Tijera.")
        print("2. Tijera gana a Papel.")
        print("3. Papel gana a Piedra.")
        print("4. Si ambos eligen lo mismo, es empate.")

    elif opcion == "2":

        nombre = input("\nIngrese su nombre: ")

        seguir = "si"

        while seguir.lower() == "si":

            print("\n==============================")
            print("Turno de", nombre)
            print("==============================")
            print("Opciones:")
            print("Piedra")
            print("Papel")
            print("Tijera")

            jugador = input("Ingrese su elección: ").lower()

            opciones = ["piedra", "papel", "tijera"]
            computadora = random.choice(opciones)

            print("\n", nombre, "eligió:", jugador)
            print("La computadora eligió:", computadora)

            if jugador == computadora:
                print("Resultado: ¡Empate!")

            elif jugador == "piedra" and computadora == "tijera":
                print("Resultado: ¡Ganaste!")

            elif jugador == "papel" and computadora == "piedra":
                print("Resultado: ¡Ganaste!")

            elif jugador == "tijera" and computadora == "papel":
                print("Resultado: ¡Ganaste!")

            elif jugador not in opciones:
                print("Opción inválida. Intente nuevamente.")

            else:
                print("Resultado: ¡La computadora ganó!")

            seguir = input("\n¿Desea jugar otra vez? (si/no): ").lower()

        print("\n===================================")
        print("Gracias por jugar con nosotros.")
        print("¡Esperamos verte pronto!")
        print("===================================")

    elif opcion == "3":

        print("\n===================================")
        print("Gracias por jugar con nosotros.")
        print("¡Esperamos verte pronto!")
        print("===================================")

    else:
        print("\nOpción incorrecta. Intente nuevamente.")
