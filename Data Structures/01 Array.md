# ⚽ Playing with Arrays

## 👺 01 Write a program to read and display n numbers using an array.

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

## 👺 02 Write a program to find the mean of n numbers using arrays.
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
 ---

 ## 👺 03 Write a program to print the position of the smallest number of n numbers using arrays.
### <u>Solution in C language 🦭</u>
```c
#include <stdio.h>

int main()
{
    int i, n, arr[20], small, pos;

    printf("\nEnter the number of elements in the array: ");
    scanf("%d", &n);
    printf("\n Enter the elements : ");
    for (i = 0; i < n; i++)
        scanf("%d", &arr[i]);
    small = arr[0];
    pos = 0;
    for (i = 1; i < n; i++)
    {
        if (arr[i] < small)
        {
            small = arr[i];
            pos = i;
        }
    }
    printf("\nThe smallest element is : %d", small);
    printf("\nThe position of the smallest element in the array is : %d", pos);
    return 0;
}
```
### Output 😶‍🌫️

```text
Enter the number of elements in the array: 5

 Enter the elements : 23 89 67 45 10

The smallest element is : 10
The position of the smallest element in the array is : 4
```
---

## 👺 04 Write a program to find the second largest of n numbers using an array.
### <u>Solution in C language 🦭</u>

```c
#include <stdio.h>

int main()
{
    int i, n, arr[20], large, second_large;
    printf("\nEnter the number of elements in the array: ");
    scanf("%d", &n);
    printf("\nEnter the elements: ");
    for (i = 0; i < n; i++)
        scanf("%d", &arr[i]);
    large = arr[0];
    for (i = 1; i < n; i++)
    {
        if (arr[i] > large)
            large = arr[i];
    }
    second_large = arr[1];
    for (i = 0; i < n; i++)
    {
        if (arr[i] != large)
        {
            if (arr[i] > second_large)
                second_large = arr[i];
        }
    }
    printf("\nThe numbers you entered are : ");
    for (i = 0; i < n; i++)
        printf("\t %d", arr[i]);
    printf("\nThe largest of these numbers is: %d", large);
    printf("\nThe second largest of these numbers is: %d", second_large);
    return 0;
}

```
### Output 😶‍🌫️

```text
Enter the number of elements in the array: 5

Enter the elements: 1 2 3 4 5

The numbers you entered are :    1       2       3       4       5
The largest of these numbers is: 5
The second largest of these numbers is: 4
```
---
## 👺 05 Write a program to enter n number of digits. Form a number using these digits
### <u>Solution in C language 🦭</u>
```c
#include <stdio.h>
#include <math.h>

int main()
{
    int number = 0, digit[10], numofdigits, i;

    printf("\nEnter the number of digits: ");
    scanf("%d", &numofdigits);
    for (i = 0; i < numofdigits; i++)
    {
        printf("\nEnter the digit at position %d: ", i + 1);
        scanf("%d", &digit[i]);
    }
    i = 0;
    while (i < numofdigits)
    {
        number = number + digit[i] * pow(10, i);
        i++;
    }
    printf("\nThe number is: %d", number);
    return 0;
}
```
### Output 😶‍🌫️
```text
Enter the number of digits: 5

Enter the digit at position 1: 9

Enter the digit at position 2: 4

Enter the digit at position 3: 7

Enter the digit at position 4: 1

Enter the digit at position 5: 6

The number is: 61749
```
---

## 👺 06 Write a program to find whether the array of integers contains a duplicate number.
### <u>Solution in C language 🦭</u>
```c
#include <stdio.h>

int main()
{
    int array[10], i, n, j, flag = 0;

    printf("\nEnter the size of the array: ");
    scanf("%d", &n);
    for (i = 0; i < n; i++)
    {
        printf("array[%d] = ", i);
        scanf("%d", &array[i]);
    }
    for (i = 0; i < n; i++)
    {
        for (j = i + 1; j < n; j++)
        {
            if (array[i] == array[j] && i != j)
            {
                flag = 1;
                printf("\nDuplicate numbers found at locations %d and %d", i, j);
            }
        }
    }
    if (flag == 0)
        printf("\nNo Duplicates Found !");
    return 0;
}
```

### Output 😶‍🌫️
```text
Enter the size of the array: 4
array[0] = 12
array[1] = 34
array[2] = 56
array[3] = 12

Duplicate numbers found at locations 0 and 3
```
---
## 👺 07 Write a program to insert a number at a given location in an array
### <u>Solution in C language 🦭</u>
```c
#include "stdio.h"

int main()
{
    int i, n, num, pos, arr[10];

    printf("\nEnter the number of elements in the array : ");
    scanf("%d", &n);
    for (i = 0; i < n; i++)
    {
        printf("arr[%d] = ", i);
        scanf("%d", &arr[i]);
    }
    printf("\nEnter the number to be inserted : ");
    scanf("%d", &num);
    printf("\nEnter the position at which the number has to be added :");
    scanf("%d", &pos);
    for (i = n - 1; i >= pos; i--)
        arr[i + 1] = arr[i];
    arr[pos] = num;
    n = n + 1;
    printf("\nThe array after insertion of %d is : ", num);
    for (i = 0; i < n; i++)
        printf("\narr[%d] = %d", i, arr[i]);

    return 0;
}
```
### Output 😶‍🌫️
```text
Enter the number of elements in the array : 4
arr[0] = 23
arr[1] = 34
arr[2] = 56
arr[3] = 78

Enter the number to be inserted : 50

Enter the position at which the number has to be added :2

The array after insertion of 50 is : 
arr[0] = 23
arr[1] = 34
arr[2] = 50
arr[3] = 56
arr[4] = 78
```
---
## 👺 08 Write a program to insert a number in an array that is already sorted in ascending order
### <u>Solution in C language 🦭</u>
```c
#include <stdio.h>

int main()
{
    int i, n, j, num, arr[10];

    printf("\nEnter the number of elements in the array : ");
    scanf("%d", &n);
    for (i = 0; i < n; i++)
    {
        printf("\n arr[%d] = ", i);
        scanf("%d", &arr[i]);
    }
    printf("\nEnter the number to be inserted : ");
    scanf("%d", &num);
    for (i = 0; i < n; i++)
    {
        if (arr[i] > num)
        {
            for (j = n - 1; j >= i; j--)
                arr[j + 1] = arr[j];
            arr[i] = num;
            break;
        }
    }
    n = n + 1;
    printf("\nThe array after insertion of %d is : ", num);
    for (i = 0; i < n; i++)
        printf("\n arr[%d] = %d", i, arr[i]);

    return 0;
}
```
### Output 😶‍🌫️

```text
Enter the number of elements in the array : 4

 arr[0] = 34

 arr[1] = 76

 arr[2] = 23

 arr[3] = 89

Enter the number to be inserted : 45

The array after insertion of 45 is : 
 arr[0] = 34
 arr[1] = 45
 arr[2] = 76
 arr[3] = 23
 arr[4] = 89
 ```
 ---

 ## 👺 09 Write a program to delete a number from a given location in an array
### <u>Solution in C language 🦭</u>
```c
#include <stdio.h>

int main()
{
    int i, n, pos, arr[10];

    printf("\nEnter the number of elements in the array: ");
    scanf("%d", &n);
    for (i = 0; i < n; i++)
    {
        printf("arr[%d] = ", i);
        scanf("%d", &arr[i]);
    }
    printf("\nEnter the position from which the number has to be deleted: ");
    scanf("%d", &pos);
    for (i = pos; i < n-1; i++)
        arr[i] = arr[i + 1];
    n--;
    printf("\nThe array after deletion is: \n");
    for (i = 0; i < n; i++)
        printf("\narr[%d] = %d", i, arr[i]);

    return 0;
}
```
### Output 😶‍🌫️

```text
Enter the number of elements in the array: 4
arr[0] = 12
arr[1] = 34
arr[2] = 74
arr[3] = 35

Enter the position from which the number has to be deleted: 3

The array after deletion is: 

arr[0] = 12
arr[1] = 34
arr[2] = 74
```
---
 ## 👺 10 Write a program to delete a number from an array that is already sorted in ascending order.
### <u>Solution in C language 🦭</u>
```c
#include <stdio.h>

int main()
{
    int i, n, j, num, arr[10];

    printf("\nEnter the number of elements in the array : ");
    scanf("%d", &n);
    for (i = 0; i < n; i++)
    {
        printf("arr[%d] = ", i);
        scanf("%d", &arr[i]);
    }
    printf("\nEnter the number to be deleted : ");
    scanf("%d", &num);
    for (i = 0; i < n; i++)
    {
        if (arr[i] == num)
        {
            for (j = i; j < n-1; j++)
                arr[j] = arr[j + 1];
        }
    }
    n--;
    printf("\nThe array after deletion is : ");
    for (i = 0; i < n; i++)
        printf("\narr[%d] = %d", i, arr[i]);

    return 0;
}
```
### Output 😶‍🌫️

```text
Enter the number of elements in the array : 4
arr[0] = 1
arr[1] = 2
arr[2] = 3
arr[3] = 4

Enter the number to be deleted : 3

The array after deletion is : 
arr[0] = 1
arr[1] = 2
arr[2] = 4
```
---
 ## 👺 11 Write a program to merge two unsorted arrays.
### <u>Solution in C language 🦭</u>
```c
#include <stdio.h>

int main()
{
    int arr1[10], arr2[10], arr3[20];
    int i, n1, n2, m, index = 0;

    printf("\nEnter the number of elements in array1: ");
    scanf("%d", &n1);
    printf("\nEnter the elements of the first array: \n");
    for (i = 0; i < n1; i++)
    {
        printf("arr1[%d] = ", i);
        scanf("%d", &arr1[i]);
    }
    printf("\nEnter the number of elements in array2: ");
    scanf("%d", &n2);
    printf("\nEnter the elements of the second array: \n");
    for (i = 0; i < n2; i++)
    {
        printf("arr2[%d] = ", i);
        scanf("%d", &arr2[i]);
    }
    m = n1 + n2;
    for (i = 0; i < n1; i++)
    {
        arr3[index] = arr1[i];
        index++;
    }
    for (i = 0; i < n2; i++)
    {
        arr3[index] = arr2[i];
        index++;
    }
    printf("\n\nThe merged array is:");
    for (i = 0; i < m; i++)
        printf("\narr[%d] = %d", i, arr3[i]);

    return 0;
}
```

### Output 😶‍🌫️
```text
Enter the number of elements in array1: 4

Enter the elements of the first array: 
arr1[0] = 34
arr1[1] = 56
arr1[2] = 63
arr1[3] = 82

Enter the number of elements in array2: 5

Enter the elements of the second array: 
arr2[0] = 10
arr2[1] = 30
arr2[2] = 40
arr2[3] = 50
arr2[4] = 70


The merged array is:
arr[0] = 34
arr[1] = 56
arr[2] = 63
arr[3] = 82
arr[4] = 10
arr[5] = 30
arr[6] = 40
arr[7] = 50
arr[8] = 70
```
---
 ## 👺 12 Write a program to merge two sorted arrays.
### <u>Solution in C language 🦭</u>
```c
#include <stdio.h>

int main()
{
    int arr1[10], arr2[10], arr3[20];
    int i, n1, n2, m, index = 0;
    int index_first = 0, index_second = 0;

    printf("\nEnter the number of elements in array1: ");
    scanf("%d", &n1);
    printf("\nEnter the elements of the first array:\n");
    for (i = 0; i < n1; i++)
    {
        printf("arr1[%d] = ", i);
        scanf("%d", &arr1[i]);
    }
    printf("\nEnter the number of elements in array2: ");
    scanf("%d", &n2);
    printf("\nEnter the elements of the second array:\n");
    for (i = 0; i < n2; i++)
    {
        printf("arr2[%d] = ", i);
        scanf("%d", &arr2[i]);
    }
    m = n1 + n2;

    int k, j;

    for (k = 0, j = 0, i = 0; i <= n1 + n2; i++)
    {
        if (arr1[k] < arr2[j])
        {
            arr3[i] = arr1[k];
            k++;
            if (k >= n1)
            {
                for (i++; j < n2; j++, i++)
                    arr3[i] = arr2[j];
            }
        }
        else
        {
            arr3[i] = arr2[j];
            j++;
            if (j >= n2)
            {
                for (i++; k < n1; k++, i++)
                    arr3[i] = arr1[k];
            }
        }
    }
    printf("\n\nThe merged array is:");
    for (i = 0; i < m; i++)
        printf("\n arr[%d] = %d", i, arr3[i]);

    return 0;
}
```

### Output 😶‍🌫️
```text
Enter the number of elements in array1: 4

Enter the elements of the first array:
arr1[0] = 1
arr1[1] = 2
arr1[2] = 3
arr1[3] = 4

Enter the number of elements in array2: 5

Enter the elements of the second array:
arr2[0] = 1
arr2[1] = 2
arr2[2] = 3
arr2[3] = 4
arr2[4] = 5


The merged array is:
 arr[0] = 1
 arr[1] = 1
 arr[2] = 2
 arr[3] = 2
 arr[4] = 3
 arr[5] = 3
 arr[6] = 4
 arr[7] = 4
 arr[8] = 5
```
### <u>Solution in C++ language 🐳</u>

```c++
// Program to merge two 1-D arrays

#include <iostream>

using namespace std;
const int MAX1 = 5;
const int MAX2 = 7;

class array
{
private:
	int *arr;
	int size;

public:
	void create(int sz);
	void sort();
	void display();
	void merge(array &a, array &b);
};

// creates array of given size sz, dynamically
void array ::create(int sz)
{
	size = sz;
	arr = new int[size];

	int n;

	for (int i = 0; i < size; i++)
	{
		cout << "\nEnter the element no. " << (i + 1) << " :";
		cin >> n;
		arr[i] = n;
	}
}

// sorts array in ascending order
void array ::sort()
{
	int temp;
	for (int i = 0; i < size; i++)
	{
		for (int j = i + 1; j < size; j++)
		{
			if (arr[i] > arr[j])
			{
				temp = arr[i];
				arr[i] = arr[j];
				arr[j] = temp;
			}
		}
	}
}

// displays the contents of array
void array ::display()
{
	for (int i = 0; i < size; i++)
		cout << "  " << arr[i];
}

// merges two arrays of different size
void array ::merge(array &a, array &b)
{
	int i, k, j;
	size = a.size + b.size;

	arr = new int[size];

	for (k = 0, j = 0, i = 0; i <= size; i++)
	{
		if (a.arr[k] < b.arr[j])
		{
			arr[i] = a.arr[k];
			k++;
			if (k >= a.size)
			{
				for (i++; j < b.size; j++, i++)
					arr[i] = b.arr[j];
			}
		}
		else
		{
			arr[i] = b.arr[j];
			j++;
			if (j >= b.size)
			{
				for (i++; k < a.size; k++, i++)
					arr[i] = a.arr[k];
			}
		}
	}
}

int main()
{
	array a;
	cout << "\nEnter elements for first array: \n";
	a.create(MAX1);

	array b;
	cout << "\nEnter elements for second array: \n";
	b.create(MAX2);

	a.sort();
	b.sort();

	cout << "\nFirst array: \n";
	a.display();
	cout << "\n\nSecond array: \n";
	b.display();
	cout << "\n\nAfter Merging: \n";

	array c;
	c.merge(a, b);
	c.display();
	return 0;
}

```
### Output 😶‍🌫️

```text
Enter elements for first array: 

Enter the element no. 1 :12

Enter the element no. 2 :34

Enter the element no. 3 :56

Enter the element no. 4 :89

Enter the element no. 5 :90

Enter elements for second array: 

Enter the element no. 1 :34

Enter the element no. 2 :37

Enter the element no. 3 :41

Enter the element no. 4 :68

Enter the element no. 5 :42

Enter the element no. 6 :13

Enter the element no. 7 :58

First array: 
  12  34  56  89  90

Second array:
  13  34  37  41  42  58  68

After Merging:
  12  13  34  34  37  41  42  56  58  68  89  90
```
---
 ## 👺 13 Write a program to read an array of n numbers and then find the smallest and largest number.
### <u>Solution in C language 🦭</u>

```c
#include <stdio.h>

void read_array(int arr[], int n);
int find_them(int arr[], int n);

int main()
{
    int num[10], n, smallest;

    printf("\n Enter the size of the array : ");
    scanf("%d", &n);
    read_array(num, n);
    find_them(num, n);
    return 0;
}
void read_array(int arr[10], int n)
{
    int i;
    for (i = 0; i < n; i++)
    {
        printf("\n arr[%d] = ", i);
        scanf("%d", &arr[i]);
    }
}
int find_them(int arr[10], int n)
{
    int i = 0, small = arr[0], big = 0;
    for (i = 1; i < n; i++)
    {
        if (arr[i] < small)
            small = arr[i];
        if (arr[i] > big)
            big = arr[i];
    }
    printf("\n The smallest number in the array is = %d", small);
    printf("\n The largest number in the array is = %d", big);
}
```
### Output 😶‍🌫️
```text
 Enter the size of the array : 5

 arr[0] = 56

 arr[1] = 21

 arr[2] = 89

 arr[3] = 43

 arr[4] = 67

 The smallest number in the array is = 21
 The largest number in the array is = 89
```
---
 ## 👺 14 Write a program to interchange the largest and the smallest number in an array
### <u>Solution in C language 🦭</u>
```c
#include <stdio.h>


void read_array(int my_array[], int);
void display_array(int my_array[], int);
void interchange(int arr[], int);
int find_biggest_pos(int my_array[10], int n);
int find_smallest_pos(int my_array[10], int n);

int main()
{
    int arr[10], n;

    printf("\nEnter the size of the array: ");
    scanf("%d", &n);
    read_array(arr, n);
    interchange(arr, n);
    printf("\nThe new array is: ");
    display_array(arr, n);

    return 0;
}
void read_array(int my_array[10], int n)
{
    int i;
    for (i = 0; i < n; i++)
    {
        printf("arr[%d] = ", i);
        scanf("%d", &my_array[i]);
    }
}
void display_array(int my_array[10], int n)
{
    int i;
    for (i = 0; i < n; i++)
        printf("\n arr[%d] = %d", i, my_array[i]);
}
void interchange(int my_array[10], int n)
{
    int temp, big_pos, small_pos;
    big_pos = find_biggest_pos(my_array, n);
    small_pos = find_smallest_pos(my_array, n);
    temp = my_array[big_pos];
    my_array[big_pos] = my_array[small_pos];
    my_array[small_pos] = temp;
}
int find_biggest_pos(int my_array[10], int n)
{
    int i, large = my_array[0], pos = 0;
    for (i = 1; i < n; i++)
    {
        if (my_array[i] > large)
        {
            large = my_array[i];
            pos = i;
        }
    }
    return pos;
}
int find_smallest_pos(int my_array[10], int n)
{
    int i, small = my_array[0], pos = 0;
    for (i = 1; i < n; i++)
    {
        if (my_array[i] < small)
        {
            small = my_array[i];
            pos = i;
        }
    }

    return pos;
}
```
### Output 😶‍🌫️

```text
Enter the size of the array: 4
arr[0] = 12
arr[1] = 34
arr[2] = 56
arr[3] = 11

The new array is: 
 arr[0] = 12
 arr[1] = 34
 arr[2] = 11
 arr[3] = 56
```
---

## 👺 15 Write a program to find Duplicate numbers in array using function
### <u>Solution in C++ language 🐳</u>

```c++
#include <stdio.h>
#include <unordered_set>

bool hasDuplicates(int array[], int n);

int main()
{
    int array[] = {1, 2, 3, 4, 4};
    int n = sizeof(array) / sizeof(array[0]);

    if (hasDuplicates(array, n) == true)
        printf("Array has duplicate elements");
    else
        printf("Array does not have duplicate elements");
  
    return 0;
}

bool hasDuplicates(int array[], int n)
{

    if (n == 0)
        return false;

    // Create an empty set
    std::unordered_set<int> s;

    // Iterate through the input array
    for (int i = 0; i < n; i++)
    {
        // If element is already in set, return true
        if (s.count(array[i]) > 0)
            return true;

        s.insert(array[i]);
    }

    // We reach here if element is not present in set
    return false;
}
```
### Output 😶‍🌫️
```text
Array has duplicate elements
```
---
## 👺 16 Write a program to implement Paskal's Triangle using array
### <u>Solution in C language 🦭</u>
```c
#include "stdio.h"

int main()
{
    int arr[7][7] = {0};
    int row = 2, col, i, j;
    arr[0][0] = arr[1][0] = arr[1][1] = 1;
    
    while (row <= 7)
    {
        arr[row][0] = 1;
        for (col = 1; col <= row; col++)
            arr[row][col] = arr[row - 1][col - 1] + arr[row - 1][col];
        row++;
    }
    for (i = 0; i < 7; i++)
    {
        printf("\n");
        for (j = 0; j <= i; j++)
            printf("\t %d", arr[i][j]);
    }

    return 0;
}
```
### Output 😶‍🌫️
```text
         1
         1       1
         1       2       1
         1       3       3       1
         1       4       6       4       1
         1       5       10      10      5       1
         1       6       15      20      15      6       1
```
---

## 👺 17 Write a program to Add two 2-D arrays
### <u>Solution in C language 🦭</u>
```c
#include <stdio.h>
int main() {
  int r, c, a[100][100], b[100][100], sum[100][100], i, j;
  printf("Enter the number of rows (between 1 and 100): ");
  scanf("%d", &r);
  printf("Enter the number of columns (between 1 and 100): ");
  scanf("%d", &c);

  printf("\nEnter elements of 1st matrix:\n");
  for (i = 0; i < r; ++i)
    for (j = 0; j < c; ++j) {
      printf("Enter element a%d%d: ", i + 1, j + 1);
      scanf("%d", &a[i][j]);
    }

  printf("Enter elements of 2nd matrix:\n");
  for (i = 0; i < r; ++i)
    for (j = 0; j < c; ++j) {
      printf("Enter element b%d%d: ", i + 1, j + 1);
      scanf("%d", &b[i][j]);
    }

  // adding two matrices
  for (i = 0; i < r; ++i)
    for (j = 0; j < c; ++j) {
      sum[i][j] = a[i][j] + b[i][j];
    }

  // printing the result
  printf("\nSum of two matrices: \n");
  for (i = 0; i < r; ++i)
    for (j = 0; j < c; ++j) {
      printf("%d   ", sum[i][j]);
      if (j == c - 1) {
        printf("\n\n");
      }
    }

  return 0;
}
```
### Output 😶‍🌫️

```text
Enter the number of rows (between 1 and 100): 2
Enter the number of columns (between 1 and 100): 3

Enter elements of 1st matrix:
Enter element a11: 2
Enter element a12: 3
Enter element a13: 4
Enter element a21: 5
Enter element a22: 2
Enter element a23: 3
Enter elements of 2nd matrix:
Enter element b11: -4
Enter element b12: 5
Enter element b13: 3
Enter element b21: 5
Enter element b22: 6
Enter element b23: 3

Sum of two matrices: 
-2   8   7   

10   8   6 
```
---

## 👺 18 Write a program to Multiply two 2-D arrays
### <u>Solution in C language 🦭</u>

```c
#include <stdio.h>

int main()
{
    int i, j, k;
    int rows1, cols1, rows2, cols2, res_rows, res_cols;
    int mat1[5][5], mat2[5][5], res[5][5];

    printf("\n Enter the number of rows in the first matrix : ");
    scanf("%d", &rows1);
    printf("\n Enter the number of columns in the first matrix : ");
    scanf("%d", &cols1);
    printf("\n Enter the number of columns in the second matrix : ");
    scanf("%d", &cols2);

    rows2 = cols1;
    res_rows = rows1;
    res_cols = cols2;

    // Taking inputs
    printf("\n Enter the elements of the first matrix ");
    for (i = 0; i < rows1; i++)
    {
        for (j = 0; j < cols1; j++)
        {
            scanf("%d", &mat1[i][j]);
        }
    }
    printf("\n Enter the elements of the second matrix ");
    for (i = 0; i < rows2; i++)
    {
        for (j = 0; j < cols2; j++)
        {
            scanf("%d", &mat2[i][j]);
        }
    }

    // Calculating
    for (i = 0; i < res_rows; i++)
    {
        for (j = 0; j < res_cols; j++)
        {
            res[i][j] = 0;
            for (k = 0; k < res_cols; k++)
                res[i][j] += mat1[i][k] * mat2[k][j];
        }
    }

    // Printing Result
    printf("\n The elements of the product matrix are ");
    for (i = 0; i < res_rows; i++)
    {
        printf("\n");
        for (j = 0; j < res_cols; j++)
            printf("\t %d", res[i][j]);
    }
    return 0;
}
```
### Output 😶‍🌫️
```text
 Enter the number of rows in the first matrix : 2

 Enter the number of columns in the first matrix : 3

 Enter the number of columns in the second matrix : 2

 Enter the elements of the first matrix 1 2 3 4 5 6

 Enter the elements of the second matrix 1 2 3 4 5 6

 The elements of the product matrix are 
         7       10
         19      28
```
---

## 👺 19 Write a program to Transpose a Matrix
### <u>Solution in C language 🦭</u>

```c
#include <stdio.h>

int main()
{
    int i, j, mat[3][3], transposed_mat[3][3];

    printf("\n Enter the elements of the matrix ");
    for (i = 0; i < 3; i++)
    {
        for (j = 0; j < 3; j++)
        {
            scanf("%d", &mat[i][j]);
        }
    }
    printf("\n The elements of the matrix are ");
    for (i = 0; i < 3; i++)
    {
        printf("\n");
        for (j = 0; j < 3; j++)
            printf("\t %d", mat[i][j]);
    }
    for (i = 0; i < 3; i++)
    {
        for (j = 0; j < 3; j++)
            transposed_mat[i][j] = mat[j][i];
    }
    printf("\n The elements of the transposed matrix are ");
    for (i = 0; i < 3; i++)
    {
        printf("\n");
        for (j = 0; j < 3; j++)
            printf("\t %d", transposed_mat[i][j]);
    }
    return 0;
}
```
### Output 😶‍🌫️

```
 Enter the elements of the matrix 1 2 3 4 5 6 7 8 9

 The elements of the matrix are 
         1       2       3
         4       5       6
         7       8       9
 The elements of the transposed matrix are 
         1       4       7
         2       5       8
         3       6       9
```