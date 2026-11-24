---
title: Code blocks
date: 2026-11-24
description: An example post showing syntax highlighted code.
---

Fenced code blocks are highlighted at build time. Name the language after the opening fence. Colors follow your system's light or dark mode.

## Python

```python
import numpy as np

def softmax(z: np.ndarray) -> np.ndarray:
    z = z - z.max(axis=-1, keepdims=True)  # numerical stability
    e = np.exp(z)
    return e / e.sum(axis=-1, keepdims=True)

print(softmax(np.array([1.0, 2.0, 3.0])))
```

## C

```c
#include <stdio.h>

static unsigned long fib(unsigned n) {
    unsigned long a = 0, b = 1;
    while (n--) {
        unsigned long t = a + b;
        a = b;
        b = t;
    }
    return a;
}

int main(void) {
    printf("%lu\n", fib(90));
    return 0;
}
```

## Highlighted lines

Add options after the language to highlight lines or show line numbers:

```go {linenos=inline hl_lines=[4]}
package main

func main() {
	ch := make(chan int)
	go func() { ch <- 42 }()
	println(<-ch)
}
```

## Shell

```sh
hugo new content posts/my-post/index.md
hugo server
```

A code block without a language is shown as plain text:

```
no highlighting here
```
