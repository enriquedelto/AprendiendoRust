# Sintaxis Básica de Funciones en Rust

## Definición de una Función

Una función se define usando la palabra clave `fn`, seguida del nombre de la función, paréntesis que pueden incluir parámetros, y un bloque de código encerrado en llaves `{}`.

```rust
fn saludar() {
    println!("Hola, mundo!");
}
```

Esta función, llamada `saludar`, imprime "Hola, mundo!" cuando se llama. No toma parámetros y no devuelve un valor porque termina en ;.

## Parámetros

Las funciones pueden tomar parámetros, que son valores pasados a la función para que trabaje con ellos. Cada parámetro debe tener un tipo especificado. Esto es un ejemplo de una función con parámetros:

```rust
fn sumar(a: i32, b: i32) -> i32 {
    a + b
}
```

En este caso, `sumar` toma dos parámetros, `a` y `b`, ambos de tipo `i32` (un tipo de dato entero de 32 bits). La función suma estos dos parámetros.

## Retorno de Valores

El tipo del valor de retorno de una función se especifica después de una flecha `->`. Si una función no devuelve un valor, se utiliza el tipo `()` (que se pronuncia como "unidad"), aunque generalmente no es necesario escribirlo explícitamente. Aquí un ejemplo de función que devuelve un valor:

```rust
fn es_mayor(a: i32, b: i32) -> bool {
    a > b
}
```

Esta función, `es_mayor`, toma dos enteros como parámetros y devuelve un valor booleano (`true` o `false`) dependiendo de si `a` es mayor que `b`. Rust devuelve automáticamente el valor de la última expresión en la función, por lo que no es necesario usar la palabra `return`; sin embargo, puedes usarla si deseas retornar antes de que termine la función:

```rust
fn dividir(a: i32, b: i32) -> i32 {
    if b == 0 {
        return 0; // Retorna inmediatamente si b es 0
    }
    a / b
}
```

En este ejemplo, `dividir` retorna 0 inmediatamente si el segundo parámetro `b` es 0, previniendo así una división por cero que resultaría en un error.
