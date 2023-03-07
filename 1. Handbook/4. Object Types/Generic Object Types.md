# # Generic Object Types

```
  interface Box<Type> {
    contents: Type;
  }
```

## The Array Type

`Array itself is a generic type`

```
  const arr: Array<string> = ['duck', 'dog'];
```

## The Readonly Array Type

The ReadonlyArray is a special type that describes `arrays that shouldn’t be changed`

```
  const fixedArr: ReadonlyArray<string> = ['duck', 'dog'];
```

## Tuple Types

```
  const arrTypePair: [string, number] = ["duck", 2];
```

## The Readonly Tuple Types

```
  function doSomething(pair: readonly [string, number]) {
    pair[0] = "hello!"; // Cannot assign to '0' because it is a read-only property.
  }
```
