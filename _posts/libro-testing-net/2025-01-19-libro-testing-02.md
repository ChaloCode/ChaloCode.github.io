---
layout: single
title: "Capítulo 02: Pruebas de Integración"
permalink: /libro-de-testing-en-net/ejercicios/02
header:
    teaser: "/assets/images/book/testing-net/miniatura-libro.png"
date: 2025-01-19 -0500
categories:
  - "LIBRO TESTING .NET"
sidebar:
  nav: "libro"
---

## Ejercicios Prácticos

Pruebas de integración con WebApplicationFactory, Testcontainers y WireMock.

| Nivel | Ejercicio | Descripción |
|-------|-----------|-------------|
| Básico | Endpoint de salud | Levantar `ChaloStore.Web` con `WebApplicationFactory<Program>`. Verificar que `GET /health` devuelve `StatusCode 200` y cabecera `Content-Type: application/json`. |
| Básico | Creación de órdenes con SQLite | Configurar `ChaloStoreDbContext` con `UseSqlite("Filename=:memory:")`. Asegurar que `POST /orders` persiste la orden y decrementa el stock. |
| Básico | Respuestas 404 | Simular `GET /orders/{id}` para ID inexistente. Comprobar respuesta 404 con JSON explicativo. |
| Básico | Cabeceras obligatorias | Usar `[Theory]` + `[InlineData]` para solicitudes con y sin `X-Correlation-ID`. Confirmar 400 sin cabecera. |
| Básico | Aislar con WireMock.Net | Arrancar `WireMockServer` para simular proveedor de pagos. Validar que ante respuesta 502 del mock, la API responde 503. |
| Intermedio | Checkout con reserva | Ejecutar `POST /orders` con stock precargado. Comprobar orden en estado `Pending` y stock reducido. |
| Intermedio | Reintentos de pago | Usar `WireMock.Net` para devolver primero 500 y luego 200. Verificar reintento exitoso. |
| Intermedio | Persistencia con Testcontainers | Levantar PostgreSQL con Testcontainers, aplicar migraciones, ejecutar checkout completo. |
| Intermedio | Fixtures compartidos | Implementar `IClassFixture` o `CollectionFixture` para compartir `WebApplicationFactory`. Medir diferencia de tiempo. |
| Intermedio | Eventos y mensajería | Stub de `IEventBus` para capturar eventos `OrderCreated`. Asegurar mensajes con `OrderId`, `Status`, `CorrelationId`. |
| Avanzado | Suite multi-servicio | Orquestar app web, base de datos y mocks externos en único fixture. Ejecutar E2E y registrar tiempos. |
| Avanzado | Personalizar WebApplicationFactory | Override de `ConfigureWebHost` para inyectar dobles de `IEmailService` e `IEventBus`. |
| Avanzado | Contratos consumer-driven | Generar pact `OrderConsumer` -> `PaymentsProvider`. Integrar en `contracts/payments/pacts`. |
| Avanzado | Observabilidad | Agregar `ILogger` o `ActivitySource` a tests para capturar trazas del checkout. |
| Avanzado | Resiliencia y timeouts | Introducir latencia en mock de envíos. Validar políticas de timeout/reintento y respuesta 504. |

## Recursos Adicionales

- **Código fuente:** [ChaloStore.Orders](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/src/ChaloStore.Orders)
- **Tests de ejemplo:** [ChaloStore.IntegrationTests](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/tests/ChaloStore.IntegrationTests)
- **Documentación del capítulo:** [02-pruebas-de-integracion.md](https://github.com/ChaloCode/libro-de-testing-en-net/blob/main/docs/02-pruebas-de-integracion.md)
