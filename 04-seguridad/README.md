# Laboratorio 04 - Seguridad y buenas prácticas (Non-root)
- Alumno: Gerson Sonapo Andrade
- Imagen: gerson-apo-api:v3
- Puerto: 8083 -> 8000

## Implementación de Seguridad
1. Se creó el grupo y usuario del sistema sin privilegios: appuser / appgroup.
2. Se utilizó la directiva USER appuser para evitar la ejecución como root (UID 0).
3. Se asignaron los permisos de los archivos mediante COPY --chown=appuser:appgroup.

## Verificación de UID
Al ejecutar 'docker exec gerson-apo-api-v3 id', se evidencia que el UID es distinto de 0.
