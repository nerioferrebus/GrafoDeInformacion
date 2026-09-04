# Fundación Universitaria Colombo Internacional ([[UNICOLOMBO CARTAGENA]])

## 1. Resumen Conciso
La [[Unicolombo]] (Fundación Universitaria Colombo Internacional) es una institución privada de [[Educación Superior]] ubicada en [[Cartagena de Indias]], [[Colombia]]. Su propuesta educativa destaca por un fuerte enfoque en el [[Bilingüismo]], la [[Internacionalización]] y la innovación metodológica. Ofrece programas académicos de pregrado y posgrado en áreas como [[Ingeniería de Sistemas]], [[Licenciatura en Inglés]], [[Administración de Empresas]] y [[Diseño Gráfico]].

## 2. Conceptos Clave
- [[Educación Superior]]: Formación profesional, académica e investigativa.
- [[Bilingüismo]]: Integración del idioma inglés en el desarrollo curricular.
- [[Cartagena de Indias]]: Sede institucional y contexto socio-cultural de la entidad.
- [[Internacionalización]]: Convenios académicos e intercambio cultural global.

## 3. Script de Ejemplo Funcional

```python
# Ejemplo minimalista: Verificación de requisito de bilingüismo estudiantil
def evaluar_requisito_ingles(estudiante: str, nivel_cefr: str) -> str:
    niveles_aprobados = ["B2", "C1", "C2"]
    
    if nivel_cefr.upper() in niveles_aprobados:
        return f"Estudiante: {estudiante} | Estado: Aprobado (Nivel {nivel_cefr} - [[Bilingüismo]])"
    else:
        return f"Estudiante: {estudiante} | Estado: Pendiente (Nivel {nivel_cefr} insuficiente)"

# Ejecución de prueba
if __name__ == "__main__":
    print(evaluar_requisito_ingles("María Delgado", "B2"))
    print(evaluar_requisito_ingles("Juan Pérez", "A2"))
```
