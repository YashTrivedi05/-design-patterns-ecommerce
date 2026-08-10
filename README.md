# -design-patterns-ecommerce
A practical, real-world implementation of Creational, Structural, and Behavioral Design Patterns in TypeScript based on an E-Commerce Checkout System.  Topics / Tags to add on GitHub:  typescript design-patterns gof-patterns software-architecture clean-code ecommerce-checkout oop
# 🛒 E-Commerce Checkout System – TypeScript Design Patterns

![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue?style=for-the-badge&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-18+-green?style=for-the-badge&logo=node.js&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

A hands-on, real-world practical implementation of **Gang of Four (GoF) Software Design Patterns** in modern **TypeScript**. Instead of isolated abstract examples, this repository demonstrates design patterns integrated into an end-to-end **E-Commerce Checkout & Order Management System**.

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Design Patterns Implemented](#-design-patterns-implemented)
  - [Creational Patterns](#1-creational-patterns)
  - [Structural Patterns](#2-structural-patterns)
  - [Behavioral Patterns](#3-behavioral-patterns)
- [Project Architecture](#-project-architecture)
- [Getting Started](#-getting-started)
- [How to Run](#-how-to-run)
- [License](#-license)

---

## 🧐 Overview

Software design patterns provide reusable solutions to common object-oriented design problems. This repository shows how to leverage TypeScript’s strong typing system, interfaces, and classes to write clean, maintainable, and scalable backend services.

The system simulates a **Checkout Engine** handling:
- Multi-channel notification delivery.
- Pluggable payment strategies & legacy system integration.
- Dynamic delivery option cost enhancements.
- Event-driven order status updates to observers.
- Thread-safe application logging.

---

## 🚀 Design Patterns Implemented

### 1. Creational Patterns
> *Focus on object creation mechanisms.*

* **Singleton Pattern (`Logger.ts`)**
  * Ensures a single shared logging instance across the application to manage system logs.
* **Factory Pattern (`NotificationFactory.ts`)**
  * Dynamically creates notification services (Email, SMS, Push) based on user preference without exposing instantiation logic.

### 2. Structural Patterns
> *Focus on class and object composition.*

* **Adapter Pattern (`LegacyPaymentAdapter.ts`)**
  * Wraps a legacy payment processing gateway into a standardized modern payment interface.
* **Decorator Pattern (`ExpressDeliveryDecorator.ts`)**
  * Dynamically extends order options with extra services (e.g., Express Delivery fees and features) without modifying the original order structure.

### 3. Behavioral Patterns
> *Focus on algorithms and communication between objects.*

* **Strategy Pattern (`PaymentStrategy.ts`)**
  * Encapsulates payment methods (Credit Card, PayPal, Crypto, etc.) allowing seamless switching at runtime.
* **Observer Pattern (`OrderEventManager.ts`)**
  * Implements an event listener architecture to notify subsystems (Inventory, Billing, Analytics) whenever an order state changes.

---

## 🏗️ Project Architecture

```text
Design Patterns in TypeScript/
├── src/
│   ├── demo/
│   │   ├── system/
│   │   │   └── CheckoutSystem.ts       # Integrates all patterns into an end-to-end checkout flow
│   │   └── index.ts                    # Entry point to execute the demo
│   ├── patterns/
│   │   ├── behavioral/
│   │   │   ├── observer/
│   │   │   │   └── OrderEventManager.ts # Observer Pattern
│   │   │   └── strategy/
│   │   │       └── PaymentStrategy.ts   # Strategy Pattern
│   │   ├── creational/
│   │   │   ├── factory/
│   │   │   │   ├── NotificationFactory.ts # Factory Pattern
│   │   │   │   └── types.ts
│   │   │   └── singleton/
│   │   │       └── Logger.ts            # Singleton Pattern
│   │   └── structural/
│   │       ├── adapter/
│   │       │   └── LegacyPaymentAdapter.ts # Adapter Pattern
│   │       └── decorator/
│   │           └── ExpressDeliveryDecorator.ts # Decorator Pattern
│   └── tsconfig.json
├── package.json
└── README.md
