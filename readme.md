# Tiny Bool

## Description

A tiny boolea type for C.

Due to the size of stdbool bool is an int,
which is not very efficient for storing a single bit,
this is a tiny bool type that is only one byte.

( And a tiny library too =D )

## Usage

Just include _tinybool.h_ instead of _stdbool.h_

```c
#include <stdio.h>
#include "tinybool.h"

int main() {

    printf("size of tinybool: %d\n", sizeof(bool));  // output:1
    printf("size of true: %d\n", sizeof(true));  // output:1
    printf("size of false: %d\n", sizeof(false));  // output:1
    printf("----------\n");

    bool truthy = true;
    bool falsy = false;

    if (truthy && falsy) {
        printf("both are true\n");
    }

    else if (truthy || falsy) {
        printf("only one is true\n");  // output: only one is true
    }

    else {
        printf("both are false\n");
    }

}
```
