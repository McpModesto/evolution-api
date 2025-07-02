
# Evolution API

Este proyecto tiene el objetivo de arrancar la api de evolution-api de forma rápida y sencilla.

## 📦 Requisitos

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## 🚀 Puesta en marcha

1. **Clona el repositorio**:

   ```bash
   git clone https://github.com/McpModesto/evolution-api.git
   cd evolution-api
   ```

2. **Configura el archivo `.env`**

   ```env
   # Sustituye con tu clave de autenticación
   AUTHENTICATION_API_KEY=tu_clave_de_autenticación
   ```

   Para generar un Hash (Clave de acceso), accede al siguiente sitio y copia la clave de cifrado de 256 bits generada en el campo:

   [Generador de Claves](https://acte.ltd/utils/randomkeygen)


3. **Levanta los contenedores con Docker Compose**:

   ```bash
   docker compose up --build
   ```

   Esto arrancará tres servicios:

   - `evolution_postgres`: base de datos PostgreSQL
   - `evolution_redis`: servidor Redis
   - `evolution_api`: la API principal que se conecta a ambos servicios

   Puedes usar el siguiente comando para ver que están arrancados correctamente:
      ```bash
   docker ps
   ```

4. **Accede al dashboard de la API**

   Una vez desplegado, la API estará disponible en:

   ```
   http://localhost:8080\manager
   ```

   Desde ahí podrás acceder al dashboard o punto de entrada de evolution-api.