---
layout: single
title: "Capítulo 04: Pirámide de Testing"
permalink: /libro-de-testing-en-net/ejercicios/04
header:
    teaser: "/assets/images/book/testing-net/miniatura-libro.png"
date: 2025-01-19 -0500
categories:
  - "LIBRO TESTING .NET"
sidebar:
  nav: "libro"
---

## Ejercicios Prácticos

Distribución de suites y balance entre niveles de testing.

| Nivel | Ejercicio | Descripción |
|-------|-----------|-------------|
| Básico | Base de la pirámide | Añadir reglas de negocio a `ChaloStore.InventoryService` (prevenir reservas mayores al stock, validar SKUs). Escribir **5 pruebas unitarias** con xUnit/NSubstitute para casos felices y errores. |
| Intermedio | Probando la integración | Implementar `OrderRepository` con EF Core y base temporal (Testcontainers o SQLite). Escribir **2 pruebas de integración** para creación y consulta de órdenes. Limpiar datos entre tests. |
| Avanzado | Simulando la cima | Usar **Playwright para .NET** y automatizar checkout: agregar producto, completar datos, confirmar orden. Reflexionar sobre complejidad del entorno y riesgos de solo E2E. |

## Recursos Adicionales

### Distribución recomendada de la pirámide

| Nivel | Porcentaje | Velocidad | Costo |
|-------|------------|-----------|-------|
| Unitarias | 70% | Rápidas | Bajo |
| Integración | 20% | Moderadas | Medio |
| E2E | 10% | Lentas | Alto |

- **Código fuente:** [ChaloStore.Inventory](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/src/ChaloStore.Inventory)
- **Documentación del capítulo:** [04-piramide-de-testing.md](https://github.com/ChaloCode/libro-de-testing-en-net/blob/main/docs/04-piramide-de-testing.md)
