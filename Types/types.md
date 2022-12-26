# Types

_For more examples, please refer to the [Documentation](https://www.typescriptlang.org/docs/handbook/basic-types.html)_

## Tuple
Tuple types allow you to express an array with a fixed number of elements whose types are known, but need not be the same. For example, you may want to represent a value as a pair of a string and a number:

```
// Declare a tuple type
let x: [string, number];
// Initialize it
x = ["hello", 10]; // OK
// Initialize it incorrectly
x = [10, "hello"]; // Error
Type 'number' is not assignable to type 'string'.
Type 'string' is not assignable to type 'number'.
```

## ENUM/Enumeration

Enums stands for Enumerations. Enums are a new data type supported in TypeScript. It is used to define the set of named constants, i.e., a collection of related values. TypeScript supports both numeric and string-based enums. We can define the enums by using the enum keyword.

Example:
```
enum Color {
  Red,
  Green,
  Blue,
}
let c: Color = Color.Green;
```

There are three types of Enums in TypeScript. These are:

* Numeric Enums

    Numeric enums are number-based enums, which store values as numbers. It means we can assign the number to an instance of the enum.

    Example:
    ```
    enum Direction {  
    Up = 1,  
    Down,  
    Left,  
    Right,  
    }  
    console.log(Direction);  
    ```
    In the above example, we have a numeric enum named Direction. Here, we initialize Up with 1, and all of the following members are auto-incremented from that point. It means Direction.Up has the value 1, Down has 2, Left has 3, and Right has 4.

* String Enums

    String enums are a similar concept to numeric enums, except that the enum has some subtle runtime differences. In a string enum, each enum values are constant-initialized with a string literal, or with another string enum member rather than numeric values.

    String enums do not have auto-incrementing behavior. The benefits of using this enum is that string enums provides better readability.

    Example:
    ```
    enum AppStatus {  
        ACTIVE = 'ACT',  
        INACTIVE = 'INACT',  
        ONHOLD = 'HLD',  
        ONSTOP = 'STOP'  
    }  
    ```
* Heterogeneous Enums

    The heterogeneous enums are enums, which contains both string and numeric values. But it is advised that you don't do this unless there is a need to take advantage of JavaScript runtime behavior.

    Example:
    ```
    enum AppStatus {  
        ACTIVE = 'Yes',  
        INACTIVE = 1,  
        ONHOLD = 2,  
        ONSTOP = 'STOP'  
    }  
    ```