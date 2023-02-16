# # Intersection Types

An intersection type is defined `using the & operator`

```
  interface Colorful {
    color: string;
  }
  interface Circle {
    radius: number;
  }

  type ColorfulCircle = Colorful & Circle;
```
