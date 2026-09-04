# PostgreSQL

## 📌 Resumen Conciso
**PostgreSQL** es un sistema de gestión de [[Base de Datos Relacional]] (RDBMS) orientado a objetos, de código abierto y altamente extensible. Se destaca por su estricto cumplimiento de las propiedades [[ACID]], su soporte avanzado para [[SQL]] estándar y capacidad para manejar tipos de datos estructurados y no estructurados como [[JSONB]]. Es una elección fundamental en el desarrollo de software moderno y [[Backend]].

## 🛠️ Script de Ejemplo
```sql
-- 1. Crear tabla de usuarios
CREATE TABLE IF NOT EXISTS usuarios (
    id SERIAL PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    email VARCHAR(150) UNIQUE NOT NULL,
    creado_en TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- 2. Insertar registros
INSERT INTO usuarios (nombre, email) 
VALUES 
    ('Alice', 'alice@example.com'),
    ('Bob', 'bob@example.com');

-- 3. Consulta con filtro
SELECT id, nombre, email, creado_en 
FROM usuarios 
WHERE email LIKE '%@example.com'
ORDER BY creado_en DESC;
```

## 🔗 Conceptos Clave
- [[Base de Datos]]
- [[SQL]]
- [[ACID]]
- [[JSONB]]
- [[Indexación]]
- [[PL/pgSQL]]
- [[Transacciones]]
