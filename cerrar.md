# Operación de Cierre y Liberación de Recursos ([[cerrar]])

## 1. Resumen Conciso
La acción de **cerrar** (`close`) en programación hace referencia a la liberación explícita o implícita de recursos del sistema operativo, tales como descriptores de archivos, conexiones de red o sockets y gestores de bases de datos. Un manejo adecuado del cierre previene los [[Resource Leaks]] (fugas de recursos) y garantiza la [[Integridad de Datos]] al asegurar que los búferes de memoria se vacíen correctamente en el almacenamiento secundario.

## 2. Conceptos Clave
- [[Resource Leaks]]: Pérdida de recursos por no liberar archivos, memoria o conexiones adecuadamente.
- [[Context Managers]]: Abstracciones sintácticas (como la sintaxis `with` en Python) para el manejo automatizado del ciclo de vida del recurso.
- [[Try-Finally]]: Patrón defensivo que asegura la ejecución de la instrucción de cierre sin importar si ocurre un error.
- [[File Descriptors]]: Identificadores numéricos que el sistema operativo asigna a archivos o canales de E/S abiertos.

## 3. Script de Ejemplo Funcional

```python
# Ejemplo minimalista: Cierre seguro de recursos de archivos

# Método 1: Cierre manual con bloque try-finally defensivo
def escritura_manual(ruta: str, contenido: str) -> None:
    archivo = open(ruta, "w", encoding="utf-8")
    try:
        archivo.write(contenido)
        print("Escritura completada.")
    finally:
        archivo.close()  # Se asegura de ejecutar el cierre
        print(f"Estado del recurso: cerrado={archivo.closed}")

# Método 2: Cierre automático usando Context Manager (Práctica recomendada)
def escritura_automatica(ruta: str, contenido: str) -> None:
    with open(ruta, "w", encoding="utf-8") as archivo:
        archivo.write(contenido)
    # Al salir del bloque 'with', el archivo se cierra automáticamente
    print(f"Estado del recurso post-with: cerrado={archivo.closed}")

# Ejecución de prueba
if __name__ == "__main__":
    escritura_manual("ejemplo_1.txt", "Prueba de cierre manual.")
    escritura_automatica("ejemplo_2.txt", "Prueba de cierre automático.")
```
