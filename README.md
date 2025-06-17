# interfaz_usuario.py
import os

def mostrar_menu():
    """Muestra un menú simple de la aplicación."""
    print("\n--- Aplicación de Detección de IA ---")
    print("1. Cargar y procesar imagen")
    print("2. Mostrar resultados")
    print("3. Salir")
    print("-------------------------------------")

def obtener_opcion_usuario():
    """Pide al usuario que elija una opción del menú."""
    opcion = input("Elige una opción (1-3): ")
    return opcion

def mostrar_mensaje(tipo, mensaje):
    """Muestra mensajes al usuario con un prefijo de tipo."""
    if tipo == "info":
        print(f"[INFO] {mensaje}")
    elif tipo == "error":
        print(f"[ERROR] {mensaje}")
    elif tipo == "resultado":
        print(f"[RESULTADO] {mensaje}")
    else:
        print(mensaje)

def limpiar_pantalla():
    """Limpia la consola."""
    os.system('cls' if os.name == 'nt' else 'clear')

if __name__ == "__main__":
    print("--- Módulo de Interfaz de Usuario cargado ---")
    # Este bucle simula la interacción del usuario
    while True:
        mostrar_menu()
        opcion = obtener_opcion_usuario()

        if opcion == '1':
            mostrar_mensaje("info", "Simulando carga y procesamiento de imagen...")
            # Aquí se integrarían funciones de preprocesamiento y reconocimiento
            pass
        elif opcion == '2':
            mostrar_mensaje("info", "Simulando muestra de resultados...")
            mostrar_mensaje("resultado", "Detectados 2 objetos en la imagen.")
        elif opcion == '3':
            mostrar_mensaje("info", "Saliendo de la aplicación. ¡Adiós!")
            break
        else:
            mostrar_mensaje("error", "Opción no válida. Intenta de nuevo.")

        input("\nPresiona Enter para continuar...") # Pausa para ver los mensajes
        limpiar_pantalla()
