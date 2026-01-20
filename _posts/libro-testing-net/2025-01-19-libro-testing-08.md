---
layout: single
title: "Capítulo 08: Test-Driven Development (TDD)"
permalink: /libro-de-testing-en-net/ejercicios/08
header:
    teaser: "/assets/images/book/testing-net/miniatura-libro.png"
date: 2025-01-19 -0500
categories:
  - "LIBRO TESTING .NET"
sidebar:
  nav: "libro"
---

## Ejercicios Prácticos

Desarrollo guiado por pruebas con el ciclo Red-Green-Refactor.

| Nivel | Ejercicio | Descripción |
|-------|-----------|-------------|
| Muy fácil | Carrito de compras | Escribir test para `CartService.AddItem("SKU-001", 2)`. Implementar clase mínima. Añadir tests para quitar ítems, actualizar cantidades, rechazar cantidades negativas. Refactorizar. |
| Medio | Procesador de pedidos | Definir `IInventory` e `INotificationService`. Test: `OrderProcessor.PlaceOrder(sku, qty, email)` debe reservar stock y notificar. Implementar mínimo. Añadir test para "no hay stock". |
| Medio-Alto | Repositorio con DB in-memory | TDD con `ProductRepository.Add` y `GetById` usando EF Core InMemory. Añadir tests de concurrencia opcional. |
| Alto | Servicio HTTP con cliente externo | Diseñar `IWeatherClient`. Test unitario mockeando `HttpMessageHandler`. Test de integración con WireMock.Net. |
| Real-mundo | Refactor de código heredado | Tomar método grande sin tests. Escribir tests de caracterización. Refactorizar manteniendo tests verdes. Añadir tests de casos límite. |

## Ciclo Red-Green-Refactor

1. **🔴 RED** - Escribir un test que falle
2. **🟢 GREEN** - Escribir el código mínimo para que pase
3. **🔵 REFACTOR** - Mejorar el código sin romper tests

## Comandos

```bash
dotnet new xunit -n Store.Tests
dotnet add Store.Tests package Moq
dotnet add Store.Tests package FluentAssertions
```

## Recursos Adicionales

- **Código fuente:** [ChaloStore.Orders](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/src/ChaloStore.Orders)
- **Documentación del capítulo:** [08-test-driven-development.md](https://github.com/ChaloCode/libro-de-testing-en-net/blob/main/docs/08-test-driven-development.md)
