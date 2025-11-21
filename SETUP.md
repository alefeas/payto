# Guía de Configuración - PayTo

Instrucciones detalladas para configurar el entorno de desarrollo de PayTo.

## Requisitos del Sistema

### Mínimos
- **Node.js:** 18.0.0 o superior
- **PHP:** 8.2 o superior
- **MySQL:** 8.0 o superior
- **Composer:** 2.0 o superior
- **Git:** 2.0 o superior

### Recomendados
- **Node.js:** 20 LTS o superior
- **PHP:** 8.3 o superior
- **MySQL:** 8.0.35 o superior

## Instalación Paso a Paso

### 1. Clonar el Repositorio

```bash
git clone https://github.com/alefeas/payto.git
cd payto
```

### 2. Configurar Backend (Laravel)

#### 2.1 Instalar Dependencias

```bash
cd backend
composer install
```

#### 2.2 Configurar Variables de Entorno

```bash
cp .env.example .env
```

Edita `.env` con tus configuraciones:

```env
APP_NAME=PayTo
APP_ENV=local
APP_DEBUG=true
APP_URL=http://localhost:8000

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=payto
DB_USERNAME=root
DB_PASSWORD=

# AFIP Configuration
AFIP_CERT_PATH=/path/to/cert.crt
AFIP_KEY_PATH=/path/to/key.key
AFIP_CUIT=20123456789
```

#### 2.3 Generar Clave de Aplicación

```bash
php artisan key:generate
```

#### 2.4 Crear Base de Datos

```bash
# Asegúrate de que MySQL está corriendo
mysql -u root -p -e "CREATE DATABASE payto CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;"
```

#### 2.5 Ejecutar Migraciones

```bash
php artisan migrate
```

#### 2.6 Ejecutar Seeds (Opcional)

```bash
php artisan db:seed
```

#### 2.7 Iniciar Servidor Backend

```bash
php artisan serve
```

El backend estará disponible en `http://localhost:8000`

### 3. Configurar Frontend (Next.js)

#### 3.1 Instalar Dependencias

```bash
cd ../frontend
npm install
```

#### 3.2 Configurar Variables de Entorno

```bash
cp .env.example .env.local
```

Edita `.env.local`:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000/api
NEXT_PUBLIC_APP_NAME=PayTo
```

#### 3.3 Iniciar Servidor Frontend

```bash
npm run dev
```

El frontend estará disponible en `http://localhost:3000`

## Verificar la Instalación

### Backend
```bash
# Desde la carpeta backend
php artisan tinker
# Ejecuta: User::count()
# Debería retornar un número
```

### Frontend
Abre `http://localhost:3000` en tu navegador. Deberías ver la página de inicio de PayTo.

## Configuración de AFIP (Producción)

Para integración con AFIP necesitas:

1. **Certificado Digital** - Obtén de AFIP
2. **Clave Privada** - Generada con el certificado
3. **CUIT** - Tu número de CUIT

Coloca los archivos en:
```
backend/storage/afip/
├── cert.crt
└── key.key
```

Actualiza `.env`:
```env
AFIP_CERT_PATH=storage/afip/cert.crt
AFIP_KEY_PATH=storage/afip/key.key
AFIP_CUIT=20123456789
```

## Troubleshooting

### Error: "SQLSTATE[HY000]: General error: 1030"
**Solución:** Asegúrate de que MySQL está corriendo y la base de datos existe.

### Error: "Class not found" en Laravel
**Solución:** Ejecuta `composer dump-autoload`

### Error: "Module not found" en Next.js
**Solución:** Ejecuta `npm install` nuevamente

### Puerto 8000 o 3000 en uso
**Solución:** Cambia el puerto:
```bash
# Backend
php artisan serve --port=8001

# Frontend
npm run dev -- -p 3001
```

## Comandos Útiles

### Backend
```bash
# Ejecutar tests
php artisan test

# Crear migración
php artisan make:migration create_table_name

# Crear modelo
php artisan make:model ModelName

# Limpiar caché
php artisan cache:clear
```

### Frontend
```bash
# Ejecutar tests
npm run test

# Build para producción
npm run build

# Iniciar servidor de producción
npm run start

# Linting
npm run lint
```

## Próximos Pasos

1. Lee la [documentación del backend](./backend/README.md)
2. Lee la [documentación del frontend](./frontend/README.md)
3. Revisa la [guía de contribución](./CONTRIBUTING.md)
4. Explora la estructura del proyecto

¡Estás listo para comenzar a desarrollar en PayTo!
