# ⚽ Playing with Arrays

## 01 Write a program to read and display n numbers using an array.

### <u>Solution in C language 🦭</u>

```c
#include <stdio.h>

int main()
{
    int i, n, arr[20];

    printf("\n Enter the number of elements in the array: ");
    scanf("%d", &n);

    for (i = 0; i < n; i++)
    {
        printf("\n arr[%d] = ", i);
        scanf("%d", &arr[i]);
    }

    printf("\n The array elements are");
    
    for (i = 0; i < n; i++)
        printf("\t%d", arr[i]);
    return 0;
}
```

### Output 😶‍🌫️

```text
 Enter the number of elements in the array: 5

 arr[0] = 12

 arr[1] = 13

 arr[2] = 14

 arr[3] = 15

 arr[4] = 16

 The array elements are        12     13     14     15     16
```

---

## 02 Write a program to find the mean of n numbers using arrays.
### <u>Solution in C language 🦭</u>

```c
#include <stdio.h>

int main()
{
    int i, n, arr[20], sum = 0;
    float mean = 0.0;

    printf("\n Enter the number of elements in the array : ");
    scanf("%d", &n);
    for (i = 0; i < n; i++)
    {
        printf("\n arr[%d] = ", i);
        scanf("%d", &arr[i]);
    }
    for (i = 0; i < n; i++)
        sum += arr[i];
    mean = (float)sum / n;
    printf("\n The sum of the array elements = %d", sum);
    printf("\n The mean of the array elements = %.2f", mean);
    return 0;
}
```

### Output 😶‍🌫️

```text
 Enter the number of elements in the array : 5

 arr[0] = 1

 arr[1] = 2

 arr[2] = 3

 arr[3] = 4

 arr[4] = 5

 The sum of the array elements = 15
 The mean of the array elements = 3.00
 ```