# Laboratorio 01 - Primera imagen Docker con Nginx
- Nombre: Gerson Sonapo Andrade
- Imagen: gerson-apo-web:v1
- Puerto: 8080

## Procedimiento
1. docker build -t gerson-apo-web:v1 .
2. docker run -d --name gerson-apo-web -p 8080:80 gerson-apo-web:v1
