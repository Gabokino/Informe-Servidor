# De un servidor de pruebas a una plataforma universitaria con Proxmox VE

Propuesta técnica para organizar el servidor del laboratorio 302 y convertirlo en una plataforma de virtualización útil para actividades académicas, desarrollo, pruebas y servicios universitarios.

> **Estado del repositorio:** en preparación. El documento disponible actualmente es un informe de laboratorio sobre snapshots en Proxmox VE. Sirve como evidencia práctica, pero **no sustituye al informe técnico completo solicitado por la tarea**.

## Objetivo

Analizar la infraestructura existente y proponer un diseño viable basado en Proxmox VE, con cuatro entornos separados:

- **Producción:** servicios y proyectos universitarios en uso, con respaldos y recuperación.
- **Laboratorios docentes:** espacios aislados para hasta cuatro docentes y sus estudiantes.
- **Desarrollo:** proyectos en construcción, separados de producción.
- **Pruebas:** máquinas virtuales y contenedores temporales para experimentar.

Las decisiones deben estar justificadas con datos reales del servidor, sus límites y las necesidades académicas. No se deben presentar como hechos las capacidades que todavía no hayan sido verificadas.

## Contenido

### Documento disponible

- **Informe de laboratorio: Gestión de Snapshots en Proxmox VE** — práctica grupal con Alpine Linux, creación de un snapshot, simulación de pérdida de un archivo y recuperación mediante rollback. El archivo original está actualmente en la raíz del repositorio.

### Entregables previstos

1. **Diagnóstico:** modelo del servidor, CPU, RAM, almacenamiento, capacidad máxima soportada, máquinas virtuales existentes, consumo y limitaciones.
2. **Diseño de arquitectura:** distribución de CPU, RAM y almacenamiento entre producción, laboratorios docentes, desarrollo y pruebas.
3. **Plan de expansión:** ampliaciones necesarias, capacidad objetivo y precios referenciales con fuentes y fecha de consulta.
4. **Diagrama:** arquitectura, entornos y asignación de recursos.
5. **Operación:** permisos, seguridad, plantillas, snapshots, backups, restauración, monitorización y tareas automatizables mediante la API.
6. **Evolución:** riesgos, prioridades y requisitos para clúster, quorum, migración o alta disponibilidad, distinguiendo qué puede hacerse con el equipo actual.
7. **Informe final en PDF:** conclusiones, fuentes consultadas y síntesis de los cambios realizados después de la revisión con IA.
8. **Guía de estudio:** exactamente 10 preguntas con respuestas razonadas sobre los conceptos del Hito 3.
9. **Prompt Espejo:** evaluación honesta del proceso de aprendizaje y síntesis incorporada al PDF. También se debe publicar en Moodle el comentario obligatorio con el título exacto **«Prompt Espejo»** y el prompt completo.

## Estructura recomendada

Cuando se incorporen los entregables finales, organizar el repositorio de esta forma:

```text
Informe-Servidor/
├── README.md
├── docs/
│   ├── informe-tecnico.pdf
│   └── practicas/
│       └── informe-laboratorio-snapshots.docx
├── diagramas/
│   └── arquitectura-proxmox.png
├── evidencias/
│   └── capturas-proxmox/
└── referencias/
    └── fuentes-y-precios.md
```

La estructura es una **propuesta de organización**, no una descripción exacta de los archivos que ya están cargados. El informe técnico, el PDF final, el diagrama y las evidencias deben agregarse cuando estén listos.

## Criterios técnicos

- Usar datos de la auditoría del servidor del laboratorio 302; no inventar modelo, memoria instalada, límites de ampliación, consumo ni precios.
- Explicar para cada decisión qué necesidad resuelve, cómo se aplicaría y cómo se verificaría.
- Diferenciar snapshots de backups: un snapshot facilita volver a un estado anterior, pero no reemplaza una copia de seguridad independiente.
- Diferenciar funciones disponibles en un único nodo de las que requieren nodos adicionales u otra infraestructura.
- No subir contraseñas, claves, tokens ni capturas con datos sensibles. Revisar y ocultar direcciones IP internas y otros datos que no deban hacerse públicos.

## Estado de avance

| Elemento | Estado |
|---|---|
| Informe práctico de snapshots | Disponible en DOCX |
| Auditoría e inventario del servidor | Pendiente de integrar y verificar |
| Diseño de los cuatro entornos y recursos | Pendiente |
| Plan de ampliación y precios documentados | Pendiente |
| Diagrama de arquitectura | Pendiente |
| Operación, seguridad, recuperación y API | Pendiente |
| PDF técnico final y 10 preguntas razonadas | Pendiente |
| Prompt Espejo y síntesis de aprendizaje | Pendiente |

## Integrantes del informe de laboratorio

El documento práctico disponible identifica a los integrantes del Grupo 3. La autoría y composición del informe técnico final deben reflejar la modalidad individual indicada en la tarea.

## Uso académico

Repositorio personal de apoyo a la entrega universitaria. Las propuestas de capacidad, compra y arquitectura deben validarse con el inventario real del equipo y con fuentes técnicas y comerciales fechadas.
