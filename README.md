# Fibonacci-Sequence
Originally called fib.c


#include <stdio.h>

void fib(int *array, int size)
{
    for(int i = 2; i <= size; i++)
    {
        array[i] = array[i - 1] + array[i - 2];
    }
}

int main(void)
{
    int size;

    printf("How many? ");
    scanf("%d", &size);

    int array[size];
    
    array[0] = 1;
    array[1] = 1;

    fib(array, size);

    printf("Fibonacci sequence:\n");
    for(int i = 0; i < size; i++)
    {
        printf("%d ", array[i]);
    }

    return 0;
}
