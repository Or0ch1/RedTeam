- A function is a block of code that does a specific task, code is separated into blocks based on task making it easier to understand and maintain.
- Every rust program must have one function named _main_ , it is always the first code to run and other functions are called from within it.

``` Rust
fn main(){
	println!("Hello world!");
}
```

- Declaring a function requires the _fn_ keyword, after the function name we tell the compiler how many parameters or arguments the function expects as input these are listed inside the parentheses _()_  
- Function body is the code that does the task of the function and is defined inside the curly brackets _{}_  

## Code Indentation

- Most code statements end with a semicolon, rust processes these statements one after the other in order. When a statement doesn't end in a semicolon rust knows that the next line of code must be executed before the starting statement
- To help see the execution relationships in code we use indentation as below

``` Rust
fn main() { // The function declaration is not indented 
	// First step in function body 
		// Substep: execute before First step can be complete 
		
	// Second step in function body 
		// Substep A: execute before Second step can be complete 
		// Substep B: execute before Second step can be complete 
			// Sub-substep 1: execute before Substep B can be complete 
	
	// Third step in function body, and so on... 
}
```

## todo! macro

- A macro is like a function that takes a variable number of input arguments
- The **todo!** macro is used to identify unfinished code in a rust program, helpful in prototyping or when you want to indicate behavior that isn't complete.

``` Rust
fn main() {
    // Display the message "Hello, world!"
    todo!("Display the message by using the println!() macro");
}
```

- When you compile code that uses the **todo!** macro the compiler returns a panic message where it expects to find completed functionality.

## println! macro

- This macro outputs to screen or  _standard output_ , it expects one or more input arguments.
- We can substitute arguments using curly braces and the **println!** macro will process them in order

``` Rust
fn main() {
    // Call println! with three arguments: a string, a value, a value
    println!("The first letter of the English alphabet is {} and the last letter is {}.", 'A', 'Z');
}
```

``` zsh
$ The first letter of the English alphabet is A and the last letter is Z.
```

