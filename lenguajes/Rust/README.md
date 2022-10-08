# Definición

## Modo de escritura

En Rust, esta establecido el modo Snake_case.

## Ejecutar y compilar sin mensajes verbose

```Rust
    cargo run --quiet
    cargo run -q
```

## Tipos de datos

### String

Es un conjunto de caracteres de todo tipo, que se pueden modificar.

### &str

Un conjunto de caracteres, con tamaño conocido y inmutable.

## Estructuras

### String

Todos los campos de una estructura deben de ser del tipo String,
para pasar de un tipo &str a tipo tipo String y poder introducirlo en la estructura usaremos el método String::from("");.

```Rust
  struct Student{ name: String, level: u8, remote: bool }

fn main() {
    let name_1 = Studen { name: String::from("Shateryon"), level: 5, remote: false}
}
```

### Finalizar estructuras

Al crear las estructuras estas solo la última debe acabar en ";";

```Rust
struct Student{ name: String, level: u8, remote: bool }

struct Grades(char, char, char, char, f32);

fn main() {

}

```

## Funciones

Para indicar que una función va a devolver un valor, debemos indicarlo con una `->` y el tipo de valor a devolver.
Para devolver un valor de una función en Rust, es habitual que el último valor de la función sea el valor a devolver.

```Rust
fn divide_by_5(num: u32) -> u32 {
num / 5
}

fn main() {
let num = 25;
println!("{} divided by 5 = {}", num, divide_by_5(num));
}
```

## Ciclos

### Loop

si existen varias interrupciones (breaks) en el ciclo, todas deben de ser del mismo tipo.

cuando un break no devuelve un valor, este devuelve una tupla vacía ().

## Gestión de memoria

### Transferencia de propiedad

Cuando asignamos el contenido de un enlace, a otro, el contenido de este se transfiere dejando
el primer enlace inservible.

```Rust
{
    let mascot = String::from("ferris");

    let ferris = mascot;

    println!("{}", mascot) // We'll try to use mascot after we've moved ownership of the string data from mascot to ferris.

}
```

## Varios

### assert_eq!()

assert_eq!(a,b) es un a == b que si devuelve falso crashea el programa, es util para escribir tests

## Aportes de seguidores

@Patatas_del_papa
