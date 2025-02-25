---
{"dg-publish":true,"permalink":"/dstest/insertion-sort/","created":"2024-11-17T13:59:03.359+05:30","updated":"2025-02-25T11:49:33.916+05:30"}
---

### Algorithm

1) Start with second element(index 1) as the current element
2) Compare the current element with elements before it.
3) Shift elements that are larger than the current elements one position to the right.
4) Insert the current elements at the correct position
5) Repeat steps 2-3 for all elements in the array

```pseudo code
for i<-1 to length(A)-1 // (n-1) times
	key <- A[i] 
	j<- i-1
	while j>=0 and A[j] > key: // for worst case O((n-1)*n)/2) 
		A[j+1] <- A[j]
		j <- j-1
	A[j+1] <- key
```

```cpp
#include <iostream>

  
  

using namespace std;

  
  

void insertionSort(int arr[], int n)

{

    for(int i = 1; i<n; i++)

    {

        int key = arr[i];

        int j = i -1;

        while(j>=0 && arr[j]>key)

        {

            arr[j+1] = arr[j];

            j--;

        }

        arr[j+1] = key;

    }

}

  
  

void printArray(int arr[], int n)

{

    for(int i =0 ; i<n; i++)

    {

        cout << arr[i] << " ";

    }

    cout << endl;

}

  
  

int main()

{

    int arr[] = {12, 11, 13, 5, 6};

    int n = sizeof(arr) / sizeof(arr[0]);

  

    cout << "Original array";

    printArray(arr, n);

    insertionSort(arr, n);

  

    cout << "Sorted array:";

    printArray(arr, n);

    return 0;

}
```


## time complexity

https://www.youtube.com/watch?v=P18jNq3fGKA

![Pasted image 20241117143719.png](/img/user/Attachments/Pasted%20image%2020241117143719.png)

### Best case(When the array is sorted)

![Pasted image 20241117143930.png](/img/user/Attachments/Pasted%20image%2020241117143930.png)

> Time complexity is linear i.e. O(n)


### Worst case(When array is in decreasing order ) 

![Pasted image 20241117144706.png](/img/user/Attachments/Pasted%20image%2020241117144706.png)

> time is Quadratic i.e. O(n^2)


## Space complexity 

- The algorithm only uses a constant amount of extra memory (for variables like `key`, `i`, and `j`).
- O(1)