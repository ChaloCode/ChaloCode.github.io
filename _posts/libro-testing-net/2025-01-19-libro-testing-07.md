---
layout: single
title: "Capítulo 07: Contract Testing"
permalink: /libro-de-testing-en-net/ejercicios/07
header:
    teaser: "/assets/images/book/testing-net/miniatura-libro.png"
date: 2025-01-19 -0500
categories:
  - "LIBRO TESTING .NET"
sidebar:
  nav: "libro"
---

## Ejercicios Prácticos

Contract testing con PactNet para validar contratos entre servicios.

| Nivel | Ejercicio | Descripción |
|-------|-----------|-------------|
| Básico | Hello Pact | Crear microservicio "Provider" simple con `GET /orders/{id}`. Crear proyecto test `Consumer` con PactNet para generar pact y guardarlo localmente. |
| Intermedio | Publish & Verify | Instalar Pact Broker local o usar PactFlow trial. Publicar pact desde CI y ejecutar verificación desde pipeline del provider. |
| Intermedio | WireMock vs Pact | Implementar mismo test con WireMock.Net. Comparar velocidad, facilidad de depuración y qué aporta cada herramienta. |
| Avanzado | Provider States | Añadir casos donde provider necesita estado ("orden existe"/"orden no existe"). Configurar provider states en verificación. |

## Recursos Adicionales

- **Directorio de contratos:** [contracts/payments](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/contracts)
- **Documentación del capítulo:** [07-contract-testing.md](https://github.com/ChaloCode/libro-de-testing-en-net/blob/main/docs/07-contract-testing.md)
