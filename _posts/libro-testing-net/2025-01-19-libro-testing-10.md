---
layout: single
title: "Capítulo 10: El Futuro es Hoy - IA aplicada a Testing"
permalink: /libro-de-testing-en-net/ejercicios/10
header:
    teaser: "/assets/images/book/testing-net/miniatura-libro.png"
date: 2025-01-19 -0500
categories:
  - "LIBRO TESTING .NET"
sidebar:
  nav: "libro"
---

## Ejercicios Prácticos

Inteligencia Artificial aplicada a la generación y validación de tests.

| Nivel | Ejercicio | Descripción |
|-------|-----------|-------------|
| Básico | Prompts para pruebas unitarias | Usar GitHub Copilot para generar tests de `InventoryService`. Evaluar calidad de tests generados vs escritos manualmente. |
| Básico | Completar tests con Copilot | Escribir nombre de test descriptivo y dejar que Copilot complete AAA. Revisar y ajustar. |
| Intermedio | MCP Context Testing | Configurar `.mcpconfig.json` básico. Observar cómo el asistente sugiere tests más específicos con contexto del proyecto. |
| Intermedio | Validar tests de IA | Ejecutar tests generados por IA. Verificar cobertura. Identificar edge cases faltantes y completarlos manualmente. |
| Avanzado | Pipeline con análisis IA | Crear workflow que ejecute tests, envíe resultados a endpoint de análisis, genere reporte con insights de flakey tests y tendencias. |
| Avanzado | Refactoring asistido | Usar IA para refactorizar código legacy. Verificar que tests existentes siguen pasando. Identificar tests frágiles vs robustos. |

## Configuración MCP de Ejemplo

```json
{
  "server": "testing-mcp-server",
  "context": {
    "include": ["src/**/*.cs", "tests/**/*.cs"],
    "testPatterns": ["**/*Tests.cs"]
  }
}
```

## Herramientas Mencionadas

- **GitHub Copilot**
- **Cursor**
- **Windsurf**
- **Claude / GPT / Gemini**

## Recursos Adicionales

- **Repositorio principal:** [libro-de-testing-en-net](https://github.com/ChaloCode/libro-de-testing-en-net)
- **Documentación del capítulo:** [10-futuro-es-hoy.md](https://github.com/ChaloCode/libro-de-testing-en-net/blob/main/docs/10-futuro-es-hoy.md)
