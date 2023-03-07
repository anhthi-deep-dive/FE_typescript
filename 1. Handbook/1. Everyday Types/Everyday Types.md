# # Primitives Types

JavaScript has three very commonly used primitives: `string, number, and boolean`. Each `has a corresponding type in TypeScript`

```
  const hi: string = 'hello';
  const pi: number = 3.14;
  const isMale: boolean = true;
```

# # Arrays

```
  const fruits: string[] = ['apple', 'banana'];
  const stocks: Array<number> = [1.12, 2.21, 3.67, 4.01]
```

# # Any

Any you can use `whenever you don’t want a particular value` to cause typechecking errors. When a value is of type any, `you can access any properties of it`

The any type `is useful` when `you don’t want to write out a long type` just to `convince TypeScript` that a `particular line of code is okay`

```
  const obj: any = {
    name: 'Ben'
  };
  console.log(obj.age); // no type checking error
```

# # Function

```
  const sayHi = (name: string): string => {
    return `Hello!, ${name}`;
  };
```

# # Object Types

```
  const printCoord = (location: { x: number; y: number }) => {
    const { x, y } = location;

    console.log("The coordinate's x value is " + pt.x);
    console.log("The coordinate's y value is " + pt.y);
  };
```

# # Union Types

Union Types are `your self-build new types` that `use operators to combine types`

```
  const ages: Array<string | number> = [28, 45, "12", 7, "14"];

  function printId(id: number | string) {
    if (typeof id === "string") {
      console.log(id.toUpperCase());
    }
  }
```

# # Type Aliases

It's convenient when we want to `use the same type more than once` and refer to it `by a single name`

```
  type ID = number | string;

  const getUserById = (id: ID) => {
    return services.getUserById(Id);
  }
```

# # Interfaces

An interface declaration is `another way to name an object type`. The key distinction between Type and Interfaces is that `a type cannot be re-opened to add new properties` vs `an interface which is always extendable`

```
  interface Point {
    x: number;
    y: number;
  }
```

# # Type Assertions

Sometimes `you have information about the type of a value` that `TypeScript can’t know about`

```
  const myCanvas = document.getElementById("main_canvas") as HTMLCanvasElement;
```

You can `also use the angle-bracket syntax`

```
  const myCanvas = <HTMLCanvasElement>document.getElementById("main_canvas");
```

Sometimes `this rule can be too conservative` and `will disallow more complex coercions` that `might be valid`. If this happens, you can use two assertions

```
  const a = (expr as any) as T;
```

# # Literal Types

```
  const apac = 'vietnam' | 'singapore' | 'thailand'
```

# # Null and Undefined

JavaScript has `two primitive values` used to `signal absent or uninitialized value`: null and undefined

```
  const takeNote = (note?: string | null) => {
    if (!note) {
      return `There is no note`;
    }

    return `Write down ${note}`;
  };
```

# # Enums

```
  enum DayInWeek {
    monday = 1,
    tuesday = 2,
  }
```
