---
layout: single
title: "Capítulo 03: Pruebas de Aceptación"
permalink: /libro-de-testing-en-net/ejercicios/03
header:
    teaser: "/assets/images/book/testing-net/miniatura-libro.png"
date: 2025-01-19 -0500
categories:
  - "LIBRO TESTING .NET"
sidebar:
  nav: "libro"
---

## Ejercicios Prácticos

Pruebas de aceptación con Reqnroll y Playwright.

| Nivel | Ejercicio | Descripción |
|-------|-----------|-------------|
| Fundamental | Criterios de aceptación | Escribir 3 features en Gherkin (.feature): registro de usuario, iniciar sesión, crear pedido. Usar Given/When/Then en lenguaje de negocio. |
| Básico | SpecFlow: primer feature | Implementar `.feature` y step definitions en .NET. Ejecutar al menos 1 escenario "verde" con objetos en memoria. |
| Básico | API acceptance con WebApplicationFactory | Probar endpoint `POST /api/pedidos` end-to-end sin navegador. Validar respuesta y estado en BD. |
| Intermedio | UI E2E con Playwright | Automatizar checkout: navegar, agregar productos, completar datos, confirmar. Validar pantalla de confirmación. |
| Intermedio | Aislar con WireMock.Net | Levantar WireMock para endpoint de pago. Validar comportamiento ante respuesta exitosa y error. |
| Intermedio | Entorno con Testcontainers | Levantar PostgreSQL/MySQL real, aplicar migraciones, ejecutar pruebas y destruir contenedor. |
| Avanzado | Integración en CI | GitHub Actions workflow: build, iniciar app, instalar Playwright, ejecutar tests, subir artefactos. |
| Avanzado | Arreglar tests frágiles | Identificar 5 fallos aleatorios, aplicar `WaitForSelector`, selectores estables, eliminar sleeps. |
| Avanzado | Steps reutilizables | Refactor de steps SpecFlow: parametrización, helpers, page objects. Documentar guía de estilo. |

## Recursos Adicionales

- **Features de ejemplo:** [ChaloStore.AcceptanceTests/Features](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/tests/ChaloStore.AcceptanceTests/Features)
- **Step Definitions:** [ChaloStore.AcceptanceTests/Steps](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/tests/ChaloStore.AcceptanceTests/Steps)
- **Documentación del capítulo:** [03-pruebas-de-aceptacion.md](https://github.com/ChaloCode/libro-de-testing-en-net/blob/main/docs/03-pruebas-de-aceptacion.md)
