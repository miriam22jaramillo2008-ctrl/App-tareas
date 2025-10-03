# App de Tareas - Versión básica

tareas = []

def mostrar_tareas():
    if not tareas:
        print("No hay tareas pendientes.")
    else:
        print("Tareas pendientes:")
        for i, tarea in enumerate(tareas, 1):
            print(f"{i}. {tarea}")

def agregar_tarea(tarea):
    tareas.append(tarea)
    print(f"Tarea '{tarea}' agregada correctamente.")

def completar_tarea(num):
    if 0 < num <= len(tareas):
        tarea = tareas.pop(num - 1)
        print(f"Tarea '{tarea}' completada.")
    else:
        print("Número de tarea inválido.")

# Ejemplo de uso:
agregar_tarea("Estudiar para el examen")
agregar_tarea("Hacer ejercicio")
mostrar_tareas()
completar_tarea(1)
mostrar_tareas()
