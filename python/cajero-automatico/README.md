# ATM Simulator in Python

Console program that simulates withdrawals at an ATM. I built it for **Programming Principles 1** at CENFOTEC University (Assignment 2, Problem 1). The program's prompts and messages are in Spanish.

## What it does

It starts with an initial balance of ₡250,000 and allows several withdrawals in a row. For each withdrawal it validates the amount before subtracting it and, at the end, shows a summary with the remaining balance and the number of successful withdrawals.

## Validation rules

| Case | Result |
|---|---|
| Amount below ₡5,000 | Rejected: "Monto menor al mínimo" (below minimum) |
| Amount above ₡100,000 | Rejected: "Monto mayor al máximo" (above maximum) |
| Amount greater than the available balance | Rejected: "Fondos insuficientes" (insufficient funds) |
| Amount within range and enough balance | Withdrawal is made and subtracted from the balance |

After each attempt the current balance is shown. If the balance reaches zero, the program prints "Saldo agotado" (balance depleted) and ends.

## Concepts practiced

- Constants for fixed values (`SALDO_INICIAL`, `RETIRO_MINIMO`, `RETIRO_MAXIMO`)
- `while` loop with a double condition (user answer and balance greater than zero)
- `if / elif / else` conditionals to validate each amount
- Counters and accumulators (`retiros_exitosos`, `saldo_actual`)
- Reading input with `input()` and converting it with `int()`

## How to run it

You need Python 3 installed. From a terminal, in the file's folder:

```bash
python cajero_automatico.py
```

## Example

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

## Possible improvements

- Validate that the amount entered is a number, so the program does not crash if text is typed.
- Accept answers such as `S` or `si` in addition to `s`.
- Add an access PIN and other operations, such as deposits or balance inquiry.

## Author

Julián Salazar Solís, software engineering student at CENFOTEC University.ría del Software en la Universidad CENFOTEC.
