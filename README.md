# Small-Project-in-C

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
