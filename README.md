# ProyectoGrupoIA

# preprocesamiento.py

import numpy as np



def limpiar_texto(texto):

  """Simula una limpieza básica de texto."""

  print(f"Preprocesando texto: '{texto}'")

  return texto.strip().lower().replace(" ", " ").replace(",", "").replace(".", "")



def normalizar_datos(lista_numeros):

  """Normaliza una lista de números a un rango de 0 a 1."""

  print(f"Normalizando datos numéricos: {lista_numeros}")

  if not lista_numeros:

    return []

  min_val = min(lista_numeros)

  max_val = max(lista_numeros)

  if max_val == min_val: # Evita división por cero si todos los números son iguales

    return [0.0] * len(lista_numeros)

  return [(x - min_val) / (max_val - min_val) for x in lista_numeros]



if __name__ == "__main__":

  print("--- Módulo de Preprocesamiento cargado ---")

  texto_ejemplo = " Hola Mundo ,esto es una PrueBa. "

  numeros_ejemplo = [10, 20, 5, 25]



  texto_limpio = limpiar_texto(texto_ejemplo)

  print(f"Texto limpio final: '{texto_limpio}'")



  numeros_normalizados = normalizar_datos(numeros_ejemplo)

  print(f"Números normalizados finales: {numeros_normalizados}")



  # Este módulo no interactúa con OpenCV directamente, pero podría preprocesar datos para él.

Mensaje
Editor de texto
