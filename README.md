## About
A linear congruential generator is a simple RNG that produces a sequence of psuedorandom numbers using a discontinuous piecewise linear equation. The algorithm is well known for it's high performance and ease of use.  
This particular implementation is capable of generating sequences of positive and negative integers, as well as floating-point values.
> [!NOTE] 
> Support for the latest C23 standard is required since the library uses variable integer widths `_BitInt()`

## Example code
```c
#include <stdio.h>

#include "lcg.h"

int main() {
    const int N = 50;
    int numbers[N];

    lcg_randi(numbers, N, 2137, 0, 100);

    printf("50 random integers in range [0 - 100) with seed 2137: ");
    for (int i = 0; i < N; ++i) {
        printf("%d ", numbers[i]);
    }
    puts("");

    return 0;
}
```
