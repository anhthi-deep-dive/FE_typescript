# # Other Types to Know About

## void

Void represents `the return value of functions` which `don’t return a value`

## object

The special type object refers to `any value` that `isn’t a primitive` (string, number, bigint, boolean, symbol, null, or undefined)

## unknown

The unknown type `represents any value` and similar to the any type, but `is safer` because `it’s not legal to do anything` with an unknown value

```
  const msg: unknown;
  msg.print(); // Object is of type 'unknown'.
```

## never

The never type represents values which `are never observed`. In a return type, this means that `the function throws an exception` or `terminates execution of the program`

## Function

The global type Function `describes properties like bind, call, apply`, and `others present on all function values` in JavaScript

```
  function doSomething(f: Function) {
    return f(1, 2, 3);
  }
```
