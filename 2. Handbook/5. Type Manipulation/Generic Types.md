# # Genetic Types

```
  interface GenericIdentityFn {
    <Type>(arg: Type): Type;
  }

  function identity<Type>(arg: Type): Type {
    return arg;
  }
```

## Generic Classes

```
  class GenericNumber<NumType> {
    zeroValue: NumType;
    add: (x: NumType, y: NumType) => NumType;
  }
```

## Using Class Types in Generics

```
  function create<Type>(c: { new (): Type }): Type {
    return new c();
  }
```
