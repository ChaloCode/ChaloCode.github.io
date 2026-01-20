---
layout: single
title: "Capítulo 09: Behavior-Driven Development (BDD)"
permalink: /libro-de-testing-en-net/ejercicios/09
header:
    teaser: "/assets/images/book/testing-net/miniatura-libro.png"
date: 2025-01-19 -0500
categories:
  - "LIBRO TESTING .NET"
sidebar:
  nav: "libro"
---

## Ejercicios Prácticos

Desarrollo guiado por comportamiento con Gherkin y Reqnroll.

| Nivel | Ejercicio | Descripción |
|-------|-----------|-------------|
| Básico | Checkout con pago aprobado/rechazado | Redactar feature en Gherkin para checkout exitoso y pago rechazado (402). Implementar step definitions con stubs de pasarela. |
| Básico | Carrito de compras | Escenarios: "Agregar ítem al carrito", "Actualizar cantidad excedente de stock", "Vaciar carrito". Automatizar conectando a `CartService` con fakes. |
| Intermedio | Gestión de inventario | Escenarios: verificar stock, rebaja automática, alerta sin stock. Usar `Scenario Outline` con diferentes cantidades. |
| Intermedio | Devoluciones y notificaciones | Escenarios: devolución aprobada, fuera de tiempo, reembolso parcial. Automatizar con LightBDD o xBehave validando liberación de stock y envío de correo. |
| Avanzado | Proceso de pago con tarjeta | Escenarios: pago exitoso, fondos insuficientes, error de red. Relacionar a servicio de pago simulado (mock HTTP + Pact) e integrar en CI con Reqnroll. |

## Feature de Ejemplo

```gherkin
Feature: Checkout
  Scenario: Crear un pedido válido
    Given the cart contains "SKU-001" with quantity 2
    When the checkout is confirmed
    Then the order should be marked as "Pending Payment"
```

## Herramientas Recomendadas

- **Reqnroll** (open source recomendado)
- **LightBDD**
- **xBehave**

## Recursos Adicionales

- **Features de ejemplo:** [ChaloStore.AcceptanceTests/Features](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/tests/ChaloStore.AcceptanceTests/Features)
- **Documentación del capítulo:** [09-behavior-driven-development.md](https://github.com/ChaloCode/libro-de-testing-en-net/blob/main/docs/09-behavior-driven-development.md)
