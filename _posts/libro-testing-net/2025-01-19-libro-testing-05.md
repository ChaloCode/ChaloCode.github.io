---
layout: single
title: "Capítulo 05: Code Coverage"
permalink: /libro-de-testing-en-net/ejercicios/05
header:
    teaser: "/assets/images/book/testing-net/miniatura-libro.png"
date: 2025-01-19 -0500
categories:
  - "LIBRO TESTING .NET"
sidebar:
  nav: "libro"
---

## Ejercicios Prácticos

Cobertura de código con Coverlet y ReportGenerator.

| Nivel | Ejercicio | Descripción |
|-------|-----------|-------------|
| Básico | Configura cobertura | Crear/reutilizar `tests/ChaloStore.UnitTests`. Instalar `coverlet.collector`. Generar `lcov.info` y abrir en VS Code con Coverage Gutters. Anotar 3 líneas no cubiertas y escribir tests para cubrirlas. |
| Intermedio | Line vs Branch | Implementar regla en `PricingService` (descuentos escalonados) con varias condiciones. Observar cómo aumenta line coverage pero branch puede quedarse bajo. Aumentar pruebas para subir branch coverage. |
| Avanzado | Pipeline básico | Crear workflow en GitHub Actions que ejecute `ChaloStore.UnitTests`, genere cobertura y suba HTML como artifact. |

## Comandos Útiles

```bash
# Generar lcov
dotnet test /p:CollectCoverage=true /p:CoverletOutputFormat=lcov

# Generar HTML con ReportGenerator
reportgenerator -reports:./coverage/coverage.opencover.xml \
  -targetdir:./coverage-report -reporttypes:Html
```

## Recursos Adicionales

- **Tests de ejemplo:** [ChaloStore.UnitTests](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/tests/ChaloStore.UnitTests)
- **Documentación del capítulo:** [05-code-coverage.md](https://github.com/ChaloCode/libro-de-testing-en-net/blob/main/docs/05-code-coverage.md)
