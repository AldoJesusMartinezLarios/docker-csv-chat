# Mi Aplicación Web con IA

## 🚀 Instalación Rápida

### Prerrequisitos
- Docker y Docker Compose instalados
- Cuenta en [Groq](https://console.groq.com) para obtener API Key

### Pasos para ejecutar

1. **Clonar el repositorio**
```bash
git clone https://github.com/AldoJesusMartinezLarios/docker-csv-chat.git
cd docker-csv-chat
```

2. **Configurar variables de entorno**
```bash
cp .env.example .env
nano .env  # Editar con tus API keys
```

3. **Obtener API Key de Groq**
- Ve a [https://console.groq.com](https://console.groq.com)
- Crea una cuenta y obtén tu API Key
- Pégala en el archivo `.env`

4. **Ejecutar la aplicación**
```bash
docker-compose up -d
```

5. **Verificar que funciona**
```bash
# Ver logs
docker-compose logs -f app

# Acceder a la aplicación
# http://localhost:8000
```

## 🔧 Configuración del archivo .env

```env
GROQ_API_KEY=gsk_tu_api_key_real_aqui
API_KEYS=NO_MODIFICAR ESTE APARTADO
ALLOWED_ORIGINS=http://localhost:3000,http://127.0.0.1:3000
DEBUG=true
```

## 📋 Comandos útiles

```bash
# Parar la aplicación
docker-compose down

# Ver logs
docker-compose logs -f app

# Reiniciar
docker-compose restart

# Actualizar imagen
docker-compose pull
docker-compose up -d
```

## 🛠️ Solución de problemas

### Error de API Key
- Verifica que tu `GROQ_API_KEY` sea correcta
- Asegúrate de no tener espacios extra

### Puerto ocupado
- Cambia el puerto en `docker-compose.yml`:
```yaml
ports:
  - "8001:8000"  # Cambiar 8000 por 8001
```

### Ver logs detallados
```bash
docker-compose logs -f app
```
