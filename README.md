# Caso de Estudio: Red Social Pascualina

**Integrante:** Juan Camilo Padilla

## 1. Contexto y Problemática

En el entorno universitario, las plataformas institucionales tradicionales suelen ser rígidas y formales, lo que dificulta la integración casual entre los estudiantes. Se identificó la necesidad de contar con un espacio digital propio que fomente la comunicación abierta, la colaboración académica entre pares, la mentoría y la organización de actividades comunitarias.

## 2. Objetivo del Proyecto

Diseñar el **Modelo Entidad-Relación (MER)** y la **Estructura Lógica Relacional** para la base de datos de la **Red Social Pascualina**, aplicando principios de normalización (hasta 3FN) e integridad referencial para soportar la interacción de la comunidad estudiantil.

---

## 3. Requerimientos Funcionales Clave

El sistema se estructuró en torno a cinco ejes de interacción:

* **Gestión de Perfiles y Habilidades:** Registro de datos personales y académicos (carrera, semestre, biografía) junto con la gestión de intereses y competencias (deportes, tecnologías, áreas académicas).
* **Red de Conexiones e Interacción:** Relación autorreferenciada de seguimiento entre usuarios para fomentar redes de contacto y programas de mentoría entre estudiantes avanzados y principiantes.
* **Publicaciones y Comentarios:** Muro dinámico para compartir dudas de tareas, recursos educativos, noticias tecnológicas e interacciones informales (memes), con soporte para hilos de comentarios.
* **Grupos de Interés:** Creación de comunidades internas para asignaturas específicas, conformación de equipos para hackatones y clubes recreativos.
* **Gestión de Eventos:** Programación y coordinación de talleres, tutorías, sesiones de estudio y eventos sociales, con registro de estado de asistencia.

---

## 4. Enfoque Técnico del Modelo de Datos

El diseño del esquema de base de datos se basa en las siguientes reglas estructurales:

* **Especialización / Herencia:** Modelo de jerarquía donde la subclase `Estudiante` extiende a la superclase `Persona` (`Extends`).
* **Normalización (3FN):** Resolución de todas las relaciones *Muchos a Muchos* ($N:M$) mediante tablas de intersección (`Estudiante_Interes`, `Seguidor_Estudiante`, `Membresia_Grupo`, `Asistencia_Evento`).
* **Estándar de Nomenclatura:** Identificación explícita de Claves Primarias (`#PK`) y Claves Foráneas (`FK`) para asegurar la consistencia del esquema.
