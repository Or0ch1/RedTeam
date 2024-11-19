- Declared with the keyword _let_ , when declared it can be bound to a value or the value can be bound later in the program.

``` Rust 
// declare variable
let a_number;

// declare variable and bind value
let a_number = 10;

println!("The number is {}.", a_number);
```

> [!Note]
> If you call a variable before it has a value bound the compiler will return an error


- In Rust bindings are immutable by default meaning values cannot be changed once bound. Trying to change the value results in an error.
- To make a value mutable we use the _mut_ keyword when declaring a variable

``` Rust
// The `mut` keyword lets the variable be changed
let mut a_number = 10; 
println!("The number is {}.", a_number);

// Change the value of an immutable variable
a_number = 15;
println!("Now the number is {}.", a_number);
```

## Shadowing

- We can declare a new variable that uses the name of an existing one creating a new binding, this is called **Shadowing** since the new variable shadows the old.
- The old variable still exists but you cannot refer to it in that particular scope anymore

``` Rust
// Declare first variable binding with name "shadow_num"
let shadow_num = 5;

// Declare second variable binding, shadows existing variable "shadow_num" 
let shadow_num = shadow_num + 5; 

// Declare third variable binding, shadows second binding of variable "shadow_num"
let shadow_num = shadow_num * 2; 

println!("The number is {}.", shadow_num);
```

