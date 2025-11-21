# PayTo

PayTo es una solución de gestión financiera full-stack diseñada específicamente para empresas argentinas. Proporciona un robusto backend API REST construido con Laravel 12 y un moderno frontend basado en React con Next.js 15. La plataforma maneja operaciones complejas multi-empresa incluyendo gestión de facturas, seguimiento de pagos, cobranzas e integración perfecta con AFIP para validación de facturas electrónicas. Con aislamiento completo de datos entre empresas, control de acceso basado en roles y notificaciones en tiempo real, PayTo permite que las empresas gestionen sus operaciones financieras de manera eficiente y cumplida.

## 📚 Repositorios

- **[payto-backend](https://github.com/alefeas/payto-backend)** - API REST con Laravel 12
- **[payto-frontend](https://github.com/alefeas/payto-frontend)** - Aplicación React con Next.js 15

## ✨ Características Principales

- Gestión de Facturas Multi-Empresa
- Integración Electrónica AFIP
- Seguimiento de Pagos y Cobranzas
- Panel Financiero en Tiempo Real
- Cuentas por Cobrar y Pagar
- Cálculos de Saldo de IVA
- Conexiones de Red B2B
- Auditoría y Cumplimiento
- Soporte Multi-Moneda
- Control de Acceso Basado en Roles

## 🎯 Desafíos y Soluciones

Los desafíos principales implicaron implementar una integración segura con AFIP con autenticación basada en certificados, garantizar aislamiento completo de datos en un entorno multi-empresa y construir un panel financiero en tiempo real que maneje cálculos complejos manteniendo un rendimiento óptimo. Además, gestionar la sincronización del estado de pagos entre múltiples sistemas requirió una cuidadosa gestión de estado y manejo de errores.

## 📖 Lo que Aprendí

Este proyecto profundizó mi comprensión de la arquitectura de sistemas financieros, requisitos de cumplimiento AFIP para empresas argentinas, patrones de diseño de aplicaciones multi-tenant y la importancia del registro de auditoría en aplicaciones financieras. También adquirí experiencia en la construcción de APIs REST escalables con Laravel y la creación de paneles financieros responsivos con React.

## 🛠️ Construido con

- Laravel 12
- PHP 8.2
- Next.js 15
- React 19
- TypeScript
- MySQL
- Tailwind CSS
- shadcn/ui
- Recharts
- Sanctum
- Pest PHP
