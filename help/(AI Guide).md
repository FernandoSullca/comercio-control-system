# 🤖 AI Development Guide

This document provides guidance for AI assistants (such as GitHub Copilot, Claude, Gemini, ChatGPT) to understand and contribute effectively to this project.

---

## 🧠 Project Context

**Comercio Control System** is a full-stack inventory and sales management application.

- Backend: Java 21 + Spring Boot
- Frontend: Angular 20
- Database: PostgreSQL
- Architecture: Monorepo

---

## 🎯 Goals

AI tools should help:

- Maintain clean architecture
- Follow best practices (enterprise-level)
- Avoid legacy or deprecated patterns
- Ensure scalability and maintainability

---

## 🏗️ Architecture Overview

### Backend (Spring Boot)

Layered architecture:
controller → service → repository → database

Additional layers:
dto → data transfer objects
security → JWT authentication
exception → global error handling
config → configuration classes

### Frontend (Angular 20)

Modular architecture:
core/ → authentication, interceptors, global services
shared/ → reusable components
features/ → domain modules (products, sales, dashboard)

---

## ⚙️ Tech Constraints

### Backend
- Use Java 21 features (records, streams, optional, etc.)
- Use DTOs instead of exposing entities
- Use Spring Security with JWT
- Follow RESTful conventions

### Frontend
- Use Angular 20 best practices
- Prefer standalone components (if applicable)
- Use RxJS properly (avoid unnecessary subscriptions)
- Keep services thin and reusable

---

## 🔐 Security Rules

- Never expose entities directly
- Always validate input (DTO + validation annotations)
- Use JWT for authentication
- Protect endpoints with roles (ADMIN / EMPLOYEE)

---

## 🧱 Coding Guidelines

### Backend
- Controllers must be thin
- Business logic must be in services
- Use interfaces for services
- Handle exceptions globally

### Frontend
- Separate UI from logic
- Avoid logic inside templates
- Use services for API calls
- Keep components small and focused

---

## 📡 API Communication

- Use JSON format
- Follow REST naming conventions:
  - GET /products
  - POST /products
  - PUT /products/{id}
  - DELETE /products/{id}

---

## 🚀 Development Priorities

1. Authentication (JWT)
2. User management
3. Products module
4. Sales module
5. Dashboard & analytics

---

## ⚠️ Avoid

- Mixing layers (controller with business logic)
- Direct DB access from controllers
- Tight coupling between frontend and backend
- Deprecated Angular or Spring features

---

## 🧪 Testing (optional but encouraged)

- Backend: unit + integration tests
- Frontend: component testing

---

## 📌 Notes for AI Assistants

- Prefer clarity over cleverness
- Generate maintainable code
- Follow existing project structure
- Do not introduce unnecessary complexity

---

## 🏆 Final Goal

Help transform this project into a **production-ready system** that reflects real-world software engineering practices.