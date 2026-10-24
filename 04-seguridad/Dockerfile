FROM python:3.12-slim
ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1
WORKDIR /app
# 1. Crear grupo y usuario de sistema sin permisos de root
RUN addgroup --system appgroup && adduser --system --ingroup appgroup appuser
# 2. Instalar dependencias
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
# 3. Copiar código asignando la propiedad al nuevo usuario
COPY --chown=appuser:appgroup main.py .
# 4. Cambiar al usuario sin privilegios
USER appuser
EXPOSE 8000
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
