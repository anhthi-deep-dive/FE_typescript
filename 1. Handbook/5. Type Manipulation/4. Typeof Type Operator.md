# # Typeof Type Operator

TypeScript adds a typeof operator you can use in a type context to `refer to the type of a variable or property`

```
  let s = "hello";
  let n: typeof s; // let n: string
```

```
  const person = {
    name: "John",
    age: 28,
  };

  type P = typeof person;
  /*
    type P = {
      name: string;
      age: number;
    }
  */
```

```
  function fn() {
    return { x: 10, y: 3 };
  }

  type TypeOfFn = typeof fn;
  /*
    function f(): {
      x: number;
      y: number;
    }
  */

  type ReturnTypeOfFn = ReturnType<typeof fn>;
  /*
    type P = {
      x: number;
      y: number;
    }
  */
```
