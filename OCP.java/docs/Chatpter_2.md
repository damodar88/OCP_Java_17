# Capítulo 2: Operators (Operadores) #

- Tipos de Operadores: Unarios, binarios, ternarios.
- Precedencia de Operadores: Orden de evaluación de operaciones.
  - Operadores Unarios:Complemento lógico (!), complemento bit a bit (~), más (+), negación (-).
  - Incremento (++) y Decremento (--): Pre-incremento/decremento vs. Post-incremento/decremento (¡Crítico para el examen!).
  - Casting explícito ((tipo)).
- Operadores Aritméticos Binarios: Suma (+), resta (-), multiplicación (*), división (/), módulo (%).
  - División entera y flotante.
  - Numeric Promotion: Reglas de promoción de tipos numéricos (byte a short, short a int, int a long, int/long a float, float a double).
  - Asignación de Valores:Operador de asignación (=).
  - Casting de valores: Requisito de casting explícito para asignaciones de tipos mayores a menores. Overflow y underflow.
  - Operadores de asignación compuestos (+=, -=, *=, etc.): Realizan casting automático.
  - Valor de retorno de operadores de asignación (la asignación misma tiene un valor).
  - Comparación de Valores:Operadores de igualdad (==, !=): Comparan valores primitivos o referencias de objetos.
  - Operadores relacionales (>, >=, <, <=).
  - instanceof: Comprueba el tipo de un objeto en tiempo de ejecución. Patron Matching con instanceof. null instanceof Object siempre es false.
  - Operadores lógicos (&, |, ^): Tablas de verdad.
  - Operadores condicionales (&&, ||): Short-circuit evaluation.
- Operador Ternario (? :): booleanExpression ? expression1 : expression2.
