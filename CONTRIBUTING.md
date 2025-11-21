# Guía de Contribución

Gracias por tu interés en contribuir a PayTo. Este documento proporciona directrices para contribuir al proyecto.

## Estructura del Proyecto

PayTo es un monorepo con dos aplicaciones principales:

- **backend/** - API REST con Laravel 12
- **frontend/** - Aplicación React con Next.js 15

## Configuración del Entorno de Desarrollo

### 1. Clonar el Repositorio

```bash
git clone https://github.com/alefeas/payto.git
cd payto
```

### 2. Configurar Backend

```bash
cd backend
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve
```

### 3. Configurar Frontend

```bash
cd frontend
npm install
npm run dev
```

## Estándares de Código

### Backend (Laravel/PHP)
- Seguir PSR-12 para estilo de código
- Usar type hints en todas las funciones
- Escribir tests con Pest PHP
- Documentar métodos públicos

### Frontend (React/TypeScript)
- Usar TypeScript para type safety
- Seguir convenciones de ESLint
- Componentes funcionales con hooks
- Documentar componentes complejos

## Proceso de Contribución

1. **Fork** el repositorio
2. **Crea una rama** para tu feature (`git checkout -b feature/AmazingFeature`)
3. **Commit** tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. **Push** a la rama (`git push origin feature/AmazingFeature`)
5. **Abre un Pull Request**

## Convenciones de Commits

Usa commits descriptivos siguiendo este formato:

```
[tipo]: descripción breve

Descripción más detallada si es necesario.

Fixes #123
```

**Tipos de commits:**
- `feat:` Nueva funcionalidad
- `fix:` Corrección de bug
- `docs:` Cambios en documentación
- `style:` Cambios de formato (sin cambios de lógica)
- `refactor:` Refactorización de código
- `test:` Adición o modificación de tests
- `chore:` Cambios en configuración o dependencias

## Testing

### Backend
```bash
cd backend
php artisan test
```

### Frontend
```bash
cd frontend
npm run test
```

Asegúrate de que todos los tests pasen antes de enviar un Pull Request.

## Reportar Bugs

Usa GitHub Issues para reportar bugs. Incluye:
- Descripción clara del problema
- Pasos para reproducir
- Comportamiento esperado vs actual
- Capturas de pantalla si es relevante
- Información del entorno (OS, versiones, etc.)

## Solicitar Nuevas Características

Abre una GitHub Issue con:
- Descripción clara de la funcionalidad
- Caso de uso
- Beneficios potenciales
- Ejemplos si es posible

## Preguntas

Si tienes preguntas, abre una GitHub Discussion o contacta a los mantenedores.

---

¡Gracias por contribuir a PayTo!
