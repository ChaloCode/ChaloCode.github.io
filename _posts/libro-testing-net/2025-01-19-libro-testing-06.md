---
layout: single
title: "Capítulo 06: Mutation Testing"
permalink: /libro-de-testing-en-net/ejercicios/06
header:
    teaser: "/assets/images/book/testing-net/miniatura-libro.png"
date: 2025-01-19 -0500
categories:
  - "LIBRO TESTING .NET"
sidebar:
  nav: "libro"
---

## Ejercicios Prácticos

Mutation testing con Stryker.NET para validar la calidad de tus tests.

| Nivel | Ejercicio | Descripción |
|-------|-----------|-------------|
| Principiante | Primer contacto | Instalar Stryker, ejecutar en proyecto de tests, abrir informe HTML. Buscar mutantes sobre `PricingService`. |
| Principiante | Test débil | Localizar mutantes sobrevivientes en `IsFreeShippingEligible`. Añadir tests para matar mutantes (pedido de exactamente 100, SKU "VIP-001"). |
| Intermedio | Constantes y ramas | Ejecutar Stryker sobre `ApplyPercentageDiscount`. Escribir tests para `0m`, `0.5m`, `-0.1m`, `0.9m` y excepciones. |
| Intermedio | Mutantes equivalentes | Analizar mutantes de `StartsWith("VIP")`. Identificar si alguno es equivalente y documentarlo o ampliar dataset. |
| Intermedio-Avanzado | Excluir mutaciones ruidosas | Crear `stryker-config.json` para excluir mutaciones de strings. Verificar reducción de ruido. |
| Avanzado | Optimización para CI | Configurar workflow para PRs (modo rápido/sample) y job nocturno (análisis completo). |

## Configuración de Ejemplo

```json
{
  "stryker-config": {
    "project": "src/ChaloStore.Pricing/ChaloStore.Pricing.csproj",
    "reporters": ["html", "dots"],
    "thresholds": { "high": 90, "low": 75, "break": 60 }
  }
}
```

## Comando Básico

```bash
dotnet stryker --reporters "html" "console"
```

## Recursos Adicionales

- **Tests de ejemplo:** [ChaloStore.UnitTests](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/tests/ChaloStore.UnitTests)
- **Documentación del capítulo:** [06-mutation-testing.md](https://github.com/ChaloCode/libro-de-testing-en-net/blob/main/docs/06-mutation-testing.md)
