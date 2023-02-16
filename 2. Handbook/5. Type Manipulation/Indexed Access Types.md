# # Indexed Access Types

```
  type Person = { age: number; name: string; alive: boolean };

  type I1 = Person["age" | "name"]; // type I1 = string | number

  type I2 = Person[keyof Person]; // type I2 = string | number | boolean
```
