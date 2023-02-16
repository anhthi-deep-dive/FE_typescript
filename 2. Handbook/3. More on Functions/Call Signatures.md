# # Call Signatures

```
  type RunnableTask = {
    (taskName: string): void;
  };

  const doSomething = (task: RunnableTask) => {
    task("Delete products");
  };
```
