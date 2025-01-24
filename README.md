# pseudocodigo
# Algoritmo para calcular el promedio de 5 notas y determinar si la materia de programación está aprobada o reprobada

# Función principal
def main():
    # Declaración de variables
    notas = []
    suma = 0

    # Asignación del nombre de la materia
    nombreMateria = "Programación"

    # Entrada de las notas
    for i in range(5):
        while True:
            try:
                nota = float(input(f"Ingrese la nota {i + 1} (entre 1 y 20): "))
                if 1 <= nota <= 20:
                    notas.append(nota)
                    break
                else:
                    print("Nota no válida. Debe estar entre 1 y 20.")
            except ValueError:
                print("Por favor, ingrese un número válido.")

    # Calculo de la suma de las notas
    suma = sum(notas)

    # Calculo del promedio
    promedio = suma / 5

    # Determinación del estado de aprobación
    if promedio >= 10:
        aprobado = "Aprobado"
    else:
        aprobado = "Reprobado"

    # Salida de los resultados
    print(f"Materia: {nombreMateria}")
    print(f"Promedio General: {promedio}")
    print(f"Estado: {aprobado}")

# Llamada a la función principal
if __name__ == "__main__":
    main()
