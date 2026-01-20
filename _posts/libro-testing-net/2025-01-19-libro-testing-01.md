---
layout: single
title: "Capítulo 01: Pruebas Unitarias"
permalink: /libro-de-testing-en-net/ejercicios/01
header:
    teaser: "/assets/images/book/testing-net/miniatura-libro.png"
date: 2025-01-19 -0500
categories:
  - "LIBRO TESTING .NET"
sidebar:
  nav: "libro"
---

## Ejercicios Prácticos

Pruebas unitarias con xUnit, NSubstitute y FluentAssertions.

| Nivel | Ejercicio | Descripción |
|-------|-----------|-------------|
| Básico | Calculadora | Crear clase `Calculadora` con métodos Sumar, Restar, Multiplicar, Dividir. Escribir pruebas para entradas positivas, negativas y cero. División por cero debe lanzar excepción. |
| Básico | Validador de contraseñas | Método `EsPasswordValida(string password)` que valide: mínimo 8 caracteres, al menos una mayúscula, una minúscula, un número. Probar múltiples combinaciones. |
| Intermedio | Generador de números primos | Método `EsPrimo(int numero)`. Probar con números primos, no primos y negativos. Usar `[Theory]` con `[InlineData(...)]`. |
| Intermedio | Conversor de temperatura | `ConvertirCelsiusAFahrenheit(double celsius)`. Usar `[Fact]` y `[Theory]` para conversiones conocidas y casos límite. |
| Intermedio | Clase de usuario | Clase `Usuario` con propiedades `Nombre`, `Edad` y método `EsMayorDeEdad()`. Verificar con edades límite (17, 18, 19). |
| Avanzado | Repositorio de datos | Interfaz `IRepositorio` con `Guardar()` y `ObtenerPorId()`. Clase `Servicio` que depende de `IRepositorio`. Usar **Moq** para simular el repositorio. |
| Avanzado | Carrito de compras | Clase `Carrito` con `AgregarProducto`, `EliminarProducto`, `CalcularTotal`. Agregar interfaz `ILogger` e inyectar. Probar que se llama al log. |
| Avanzado | Notificador de correos | Servicio `Notificador` que depende de `IEmailSender`. Probar que no se envía correo si el email es inválido. Usar **Moq** para verificar comportamiento. |

## Recursos Adicionales

- **Código fuente:** [ChaloStore.Inventory](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/src/ChaloStore.Inventory)
- **Tests de ejemplo:** [ChaloStore.UnitTests](https://github.com/ChaloCode/libro-de-testing-en-net/tree/main/chalostore/tests/ChaloStore.UnitTests)
- **Documentación del capítulo:** [01-pruebas-unitarias.md](https://github.com/ChaloCode/libro-de-testing-en-net/blob/main/docs/01-pruebas-unitarias.md)
