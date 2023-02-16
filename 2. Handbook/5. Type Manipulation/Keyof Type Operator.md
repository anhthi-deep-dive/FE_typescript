# # The keyof Type Operator

The keyof operator `takes an object type` and `produces a string or numeric literal union of its keys`

```
  type Arrayish = { [n: number]: unknown };
  type A = keyof Arrayish; // type A = number

  type Mapish = { [k: string]: boolean };
  type M = keyof Mapish; // type M = string | number
```
