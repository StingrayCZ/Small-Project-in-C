# Task N.3

```c
#include <stdio.h>
#include <stdlib.h>

#define EMPTYLINE printf("\n");                                // too lazy to type printf("\n") for several times
#define PRINTARRAY                                             // do you wish to know how to looks array from Honeywell?
#define PRINTRESULTS                                           // do you wish to know what the app have found?

int main()
{

    int hop = 0;                                                 // hop to next value
    int counter = 0;                                             // counter of duplicated values

//    int array[] = {5, 3, 3, 1, 0, 0, -2, -2, -5};                // Tested 1# array from Honeywell :o)
    int array[] = {1, 2, 3, 3, 3, 4, 4, 10, 13, 15, 15, 17};     // Tested 2# array from Honeywell :o)

    int SizeArray = sizeof(array) / sizeof(array[0]);            // Size of array (used for printed array in a consola)


    #ifdef PRINTARRAY
    printf("Size of the array is %d.\n", SizeArray);

    printf("The array contains these numbers:\n");
    printArray(array, SizeArray);                               // App for printing array
    EMPTYLINE
    #endif // PRINTARRAY


    for(int i = 0; i < SizeArray; i++){                         // For loop based on size of array value

        hop = i + 1;

        if(array[i] == array[hop]){                                                                    // Checking the conformity of numbers

            #ifdef PRINTRESULTS
            printf("Matched numbers: arr[%d] = %d == arr[%d] = %d\n", i, array[i], hop, array[hop]);   // print which numbers are matched
            #endif // PRINTRESULTS

            counter += 1;                                                                              //  increase value of duplicate numbers count

        }

    }

    EMPTYLINE
    printf("Number of duplicated values is %d", counter);   // print number of duplicate values
    EMPTYLINE


    return 0;
}


void printArray(int pole[], int size)
{
    for (int i = 0; i < size; i++)
        printf("%d ", pole[i]);
    EMPTYLINE
}

```

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int velikostpole;

    printf("Zvol hodnotu pole\n");
    scanf("%d", &velikostpole);
    printf("Velikost pole je: %d\n", velikostpole);

    int pole[velikostpole];

    for(int i = 0; i < velikostpole; i++){

       printf("Napis hodnotu pro hodnotu pole[%d]", i);
       scanf("%d", &pole[i]);

    }


    return 0;
}
```

```c
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int velikostpole;

    printf("Zvol hodnotu pole\n");
    scanf("%d", &velikostpole);
    printf("Velikost pole je: %d\n", velikostpole);

    int pole[velikostpole];

    for(int i = 0; i < velikostpole; i++){

       printf("Napis hodnotu pro hodnotu pole[%d]", i);
       scanf("%d", &pole[i]);

    }

    ArrayPrinter(pole, velikostpole);


    return 0;
}


void ArrayPrinter(int array[], int ArSize)
{
    int i;
    for (i = 0; i < ArSize; i++)
        printf("%d ", array[i]);
    printf("\n");
}


```
