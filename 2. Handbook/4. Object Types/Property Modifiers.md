# # Property Modifiers

## 1. Optional Properties

```
  interface PaintOptions {
    shape: Shape;
    xPos?: number;
    yPos?: number;
  }
```

## 2. Readonly Properties

```
  interface SomeType {
    readonly prop: string;
  }
```

## 3. Index Signatures

```
  interface StringArray {
    [index: number]: string;
  }
```
