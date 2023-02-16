# # Extending Types

```
  interface Colorful {
    color: string;
  }

  interface Circle {
    radius: number;
  }

  interface ColorfulCircle extends Colorful, Circle {}
```
