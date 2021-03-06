# Tarjeta de crédito válida

Código que pide al usuario el número de su tarjeta de crédito mediante un prompt, para luego validarlo según el algoritmo de Luhn con la función isValidCard.

## Pseudocódigo

FUNCION `isValidCard` de `creditCard`{

VAR `centinel` = false  
VAR `evenDigits` = []  
VAR `sum` = 0  

BUCLE for (Iniciar contador i en `creditCard.length - 2`; validar si es `>= 0`; disminuir en 2){  
Si (`creditCard[i] * 2 > 9)` &rarr;
  `creditCard[i] * 2 - 9` ingresa como elemento de `evenDigits`  
Sino &rarr; (`creditCard[i] * 2`) ingresa como elemento de `evenDigits`}  

BUCLE for (Iniciar i en `creditCard.length -1`; validar si es `>= 0`; disminuir i en 2){  
`sum = sum + evenDigits[i]`}

BUCLE for (Iniciar i en 0; validar que sea menor que `evenDigits.length`; aumentar i en 1){  
`sum = sum + [Elemento en posición i]` 
}

Si (`sum % 10 == 0`) &rarr; Alerta 'Tarjeta válida' &rarr; `centinel = true`  
Sino &rarr; Alerta 'Tarjeta inválida' &rarr; `centinel = false`

**RETORNA `centinel`**

## Diagrama de flujo

![](assets/docs/flow-diagram-credit-card-validation.jpeg "Diagrama de flujo")