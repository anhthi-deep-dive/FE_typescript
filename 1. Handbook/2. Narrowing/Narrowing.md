# # Narrowing (thu hẹp lại)

Within our if check, TypeScript sees `typeof padding === "number"` and `understands that as a special form of code` called a `type guard`. The process of `refining types to more specific types than declared` is called `narrowing`

```
  function padLeft(padding: number | string, input: string) {
    if (typeof padding === "number") { // narrowing
      return " ".repeat(padding) + input;
    }
    return padding + input;
  }
```

# # Typeof Type Guards

TypeScript expects Typeof to return a certain set of strings

- string
- number
- bigint
- boolean
- symbol
- undefined
- object
- function

In TypeScript, `checking against the value returned by typeof` is `a type guard`

# # Truthiness narrowing

```
  const sayHello = (msg?: string) => {
    if (msg) { // truthiness narrowing
      return `Hello!, ${msg}`;
    }
  };
```

# # Equality narrowing

```
  const getLocation = (x: number | string, y: number | string) => {
    if (x === y) { // equality narrowing
      return `Location is ${x} and ${y}`;
    }
  };
```

# # The in operator narrowing

```
  type Person = {
    name: string;
    isMale: boolean;
  };

  const person = {
    name: "John",
    isMale: true,
  };

  const getMale = (person: Person) => {
    if ("isMale" in person) {
      return "This is a male";
    }
  };
```

# # Instanceof narrowing

```
  const getDay = (date: Date | string) => {
    if (date instanceof Date) {
      return date.getDay();
    }
  };
```

# # Assignments

```
  let personIndex: number | string = Math.random() < 0.5 ? "10" : 10;
  personIndex = 20;
  console.log(personIndex); // let personIndex: number
```

# # Using type predicates

```
  function isFish(pet: Fish | Bird): pet is Fish {
    return (pet as Fish).swim !== undefined;
  }
```
