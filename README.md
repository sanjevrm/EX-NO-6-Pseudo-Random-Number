# EX-NO-6-Pseudo-Random-Number

# AIM: 

Implementation of Pseudorandom Number Generation Using Standard library
## Algorithm:
Step 1: Import the secrets module: This module provides cryptographically secure random functions.

Step 2: Generate a secure random integer: Use secrets.randbelow(n) to get a random integer between 0 and n-1.

Step 3: Generate a secure random number with a specific bit length: Use secrets.randbits(bit_length) to generate a random number with a given number of bits.

Step 4: Generate a secure random token (hexadecimal): Use secrets.token_hex(nbytes) to generate a secure random token in hex format. The nbytes parameter specifies the number of bytes, and the result will be a string with twice that number of hex characters.

Step 5: Display or use the generated random values: Print or use the generated values for your cryptographic needs.

## PROGRAM:
~~~
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main()
{
    int count, min, max;
    printf("Enter the number of random numbers to generate: ");
    scanf("%d", &count);
    printf("Enter the minimum value: ");

    scanf("%d", &min);
    printf("Enter the maximum value: ");
    scanf("%d", &max);
    srand(time(NULL));
    printf("Pseudorandom numbers:\n");
    for (int i = 0; i < count; i++)
    {
        int random_number = (rand() % (max - min + 1)) + min;
        printf("%d\n", random_number);
    }
    return 0;
}

~~~

## OUTPUT:
![image](https://github.com/user-attachments/assets/288d6644-7de0-47c3-83d2-237a3b0453a7)

## RESULT:
Thus Pseudorandom Number Generation Using Standard library has been executed successfully.
