# Cajero automático en Python

Programa de consola que simula retiros en un cajero automático. Lo desarrollé para el curso **Principios de Programación 1** (CENFOTEC), como la Tarea 2, Problema 1.

## Qué hace

Parte de un saldo inicial de ₡250 000 y permite hacer varios retiros seguidos. En cada retiro valida el monto antes de descontarlo y, al terminar, muestra un resumen con el saldo restante y la cantidad de retiros exitosos.

## Reglas de validación

| Caso | Resultado |
|---|---|
| Monto menor a ₡5 000 | Se rechaza: "Monto menor al mínimo" |
| Monto mayor a ₡100 000 | Se rechaza: "Monto mayor al máximo" |
| Monto mayor al saldo disponible | Se rechaza: "Fondos insuficientes" |
| Monto dentro del rango y con saldo suficiente | Se realiza el retiro y se descuenta del saldo |

Después de cada intento se muestra el saldo actual. Si el saldo llega a cero, el programa avisa "Saldo agotado" y termina.

## Conceptos que practiqué

- Constantes para los valores fijos (`SALDO_INICIAL`, `RETIRO_MINIMO`, `RETIRO_MAXIMO`)
- Ciclo `while` con condición doble (respuesta del usuario y saldo mayor a cero)
- Condicionales `if / elif / else` para validar cada monto
- Contadores y acumuladores (`retiros_exitosos`, `saldo_actual`)
- Lectura de datos con `input()` y conversión con `int()`

## Cómo ejecutarlo

Necesitas tener Python 3 instalado. Desde una terminal, en la carpeta del archivo:

```bash
python cajero_automatico.py
```

## Ejemplo de uso

```
¿Desea realizar un retiro? (s/n): s
Ingrese el monto a retirar (₡): 50000
Retiro realizado
Saldo: 200000
¿Desea realizar otro retiro? (s/n): n

----------- Resumen -----------
Saldo restante: 200000
Retiros exitosos: 1
```

## Posibles mejoras

- Validar que el monto ingresado sea un número, para que el programa no se detenga si se escribe texto.
- Aceptar respuestas como `S` o `si` además de `s`.
- Agregar un PIN de acceso y otras operaciones, como depósitos o consulta de saldo.

## Autor

Julián Salazar Solís, estudiante de Ingeniería del Software en la Universidad CENFOTEC.
