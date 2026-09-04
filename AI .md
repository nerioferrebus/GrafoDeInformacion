# Inteligencia Artificial ([[AI]])

## 1. Resumen Conciso
La [[Inteligencia Artificial]] (IA) es la disciplina informática dedicada al desarrollo de sistemas capaces de realizar tareas que requieren cognición humana, tales como el aprendizaje, la inferencia y la resolución de problemas. Se sustenta principalmente en el [[Machine Learning]], el [[Deep Learning]] y el [[Procesamiento del Lenguaje Natural]] (NLP). Actualmente, la arquitectura de [[Transformers]] y los [[LLM]] representan el estado del arte en la generación e interpretación de información.

## 2. Conceptos Clave
- [[Machine Learning]]: Aprendizaje supervisado y no supervisado basado en datos.
- [[Deep Learning]]: Redes neuronales profundas para patrones complejos.
- [[Transformers]]: Mecanismo de atención para el procesamiento secuencial.
- [[LLM]]: Modelos de lenguaje a gran escala para tareas generativas.

## 3. Script de Ejemplo Funcional

```python
# Ejemplo minimalista: Sistema de Inferencia Simplificado
def consultar_ia(prompt: str) -> str:
    base_conocimiento = {
        "ia": "Capacidad de un sistema para imitar funciones cognitivas humanas.",
        "ml": "Subconjunto de la IA centrado en el aprendizaje a partir de datos."
    }
    
    for clave, definicion in base_conocimiento.items():
        if clave in prompt.lower():
            return f"[Respuesta IA]: {definicion}"
            
    return "[Respuesta IA]: Prompt no reconocido en la base de reglas."

# Ejecución de prueba
if __name__ == "__main__":
    print(consultar_ia("Explícame qué es la IA por favor."))
```
