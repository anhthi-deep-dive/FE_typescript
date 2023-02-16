# # Generic Functions

```
  function getFirstElement<Type>(arr: Type[]): Type | undefined {
    return arr[0];
  }
```

## Inference

```
  function map<Input, Output>(arr: Input[], func: (arg: Input) => Output): Output[] {
    return arr.map(func);
  }
```

## Constraints

```
  type AnimalBase = {
    alive: boolean;
  };

  type Duck = {
    name: string;
    alive: boolean;
  };

  const getAnimal = <Animal extends AnimalBase>(animal: Animal) => {
    if (animal.alive) {
      return `The animal is still alive`;
    }
  };

  getAnimal<Duck>({
    name: "Donal",
    alive: true,
  });
```

## Specifying Type Arguments

```
  function combineArrays<Type>(arr1: Type[], arr2: Type[]): Type[] {
    return arr1.concat(arr2);
  }
```

Will throw error if there are mismatched arrays

```
  const arr = combineArrays([1, 2, 3], ["hello"]); // Type 'string' is not assignable to type 'number'
```

Fix

```
  const arr = combineArrays<string | number>([1, 2, 3], ["hello"]);
```
