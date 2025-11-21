# PayTo

PayTo is a full-stack financial management solution designed specifically for Argentine businesses. It provides a robust REST API backend built with Laravel 12 and a modern React-based frontend with Next.js 15. The platform handles complex multi-company operations including invoice management, payment tracking, collections, and seamless AFIP integration for electronic invoice validation. With complete data isolation between companies, role-based access control, and real-time notifications, PayTo enables businesses to manage their financial operations efficiently and compliantly.

## 📚 Repositories

- **[payto-backend](https://github.com/alefeas/payto-backend)** - REST API with Laravel 12
- **[payto-frontend](https://github.com/alefeas/payto-frontend)** - React Application with Next.js 15

## ✨ Key Features

- Multi-Company Invoice Management
- AFIP Electronic Invoice Integration
- Payment & Collection Tracking
- Real-time Financial Dashboard
- Accounts Receivable & Payable
- VAT Balance Calculations
- B2B Network Connections
- Audit Logging & Compliance
- Multi-Currency Support
- Role-Based Access Control

## 🎯 Challenges & Solutions

The primary challenges involved implementing secure AFIP integration with certificate-based authentication, ensuring complete data isolation in a multi-company environment, and building a real-time financial dashboard that handles complex calculations while maintaining optimal performance. Additionally, managing payment status synchronization across multiple systems required careful state management and error handling.

## 📖 What I Learned

This project deepened my understanding of financial systems architecture, AFIP compliance requirements for Argentine businesses, multi-tenant application design patterns, and the importance of audit logging in financial applications. I also gained expertise in building scalable REST APIs with Laravel and creating responsive financial dashboards with React.

## 🛠️ Built with

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
