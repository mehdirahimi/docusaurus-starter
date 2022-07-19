---
sidebar_position: 2
---

# Local Variable Type Inference with Reference Types

_Traditional declaration_ vs _Type inference_ (substantially shorter):
- `FileInputStream fin = new FileInputStream("test.txt");`
- `var fin = new FileInputStream("test.txt");`

<hr />

Local variable type inference is a feature that you should use wisely:
- `var x = o.getNext();`

In this case, it may not be immediately clear to someone reading your code what the type of `x` is.
