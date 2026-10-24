# Laboratorio 03 - Optimización del Dockerfile
- Alumno: Gerson Sonapo Andrade
- Imagen: gerson-apo-api:v2
- Puerto: 8082 -> 8000

## Optimizaciones aplicadas
1. Archivo .dockerignore para excluir archivos innecesarios (.git, __pycache__, .env).
2. Variables de entorno PYTHONDONTWRITEBYTECODE=1 y PYTHONUNBUFFERED=1.
3. Reordenamiento de capas: se copia requirements.txt e instala con pip ANTES de copiar el código 
fuente, aprovechando el caché (CACHED).
