# # Construct Signatures

You can write a construct signature by `adding the new keyword` in front of `a call signature`

```
  type RunnableTask = {
    new (taskName: string): void;
  };

  const doSomething = (ctor: RunnableTask) => {
    return new ctor("Delete product");
  };
```
