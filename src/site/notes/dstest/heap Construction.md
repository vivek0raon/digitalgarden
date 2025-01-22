---
{"dg-publish":true,"permalink":"/dstest/heap-construction/","created":"2024-11-17T14:53:49.912+05:30","updated":"2025-01-23T00:15:29.633+05:30"}
---

A heap a specialized [[dstest/Binary Tree new\|tree]]- based data structure that satisfies the heap property:
1) Max-Heap Property: For every node i, the value of i is greater than or equal to the values of its children
2) Min-Heap Property: For every node i, the value of i is less than or equal to the values of its children

## Usage

Used in priority Queues, heap sort, and graph algorithm like  Dijkstra's Prism's

### How to implement heap

#### Relation and formula

> if we go level by level representation of tree
> then these relationship will be formed
> ![Pasted image 20241117152613.png](/img/user/Attachments/Pasted%20image%2020241117152613.png)
> left child is at 2\*i
> Right child is at 2\*i+1
> and parent is at floor of (i/2)


> [!important] Title
> Heap is a [[dstest/Binary Tree new\|Complete Binary tree]]
> duplicates are allowed


#### Heap insertion

![Pasted image 20241117153628.png](/img/user/Attachments/Pasted%20image%2020241117153628.png)
> - number 60 will climb up the hierarchy it will take O(log n ) i.e. height of a complete binary tree
> - if it was 6 then it will take O(1) 


### Basic code for insertion
```cpp
void InsertA(int A[], int n){

    int i = n;

    int temp = A[n];

    while (i > 0 && temp > A[i % 2 == 0 ? (i/2)-1 : i/2]){

        A[i] = A[i % 2 == 0 ? (i/2)-1 : i/2];

        i = i % 2 == 0 ? (i/2)-1 : i/2;

    }

    A[i] = temp;

}
```



### for creating heap different ways is given in this code 

```cpp
#include <iostream>

#include <vector>

  

using namespace std;

// Lecture based

void InsertA(int A[], int n){

    int i = n;

    int temp = A[n];

    while (i > 0 && temp > A[i % 2 == 0 ? (i/2)-1 : i/2]){

        A[i] = A[i % 2 == 0 ? (i/2)-1 : i/2];

        i = i % 2 == 0 ? (i/2)-1 : i/2;

    }

    A[i] = temp;

}

// STL vector based

void Insert(vector<int>& vec, int key){

    // Insert key at the end

    auto i = vec.size();

    vec.emplace_back(key);

    // Rearrange elements: Indices are not DRY :-(

    while (i > 0 && key > vec[i % 2 == 0 ? (i/2)-1 : i/2]){

        vec[i] = vec[i % 2 == 0 ? (i/2)-1 : i/2];

        i = i % 2 == 0 ? (i/2)-1 : i/2;

    }

    vec[i] = key;

}

  

void InsertInplace(int A[], int n){

    int i = n;

    int temp = A[n];

    while (i > 0 && temp > A[i % 2 == 0 ? (i/2)-1 : i/2]){

        A[i] = A[i % 2 == 0 ? (i/2)-1 : i/2];

        i = i % 2 == 0 ? (i/2)-1 : i/2;

    }

    A[i] = temp;

}

  

void CreateHeap(vector<int>& vec, int A[], int n){

    // O(n log n)

    for (int i=0; i<n; i++){

        Insert(vec, A[i]);

    }

}

void createHeap(int A[], int n){

    for (int i=0; i<n; i++){

        InsertInplace(A, i);

    }

}

  
  

template <class T>

void Print(T& vec, int n){

    cout << "Max Heap: [" << flush;

    for (int i=0; i<n; i++){

        cout << vec[i] << flush;

        if (i < n-1){

            cout << ", " << flush;

        }

    }

    cout << "]" << endl;

}

  

template <class T>

void Print(T& vec, int n, char c){

    cout << c << ": [" << flush;

    for (int i=0; i<n; i++){

        cout << vec[i] << flush;

        if (i < n-1){

            cout << ", " << flush;

        }

    }

    cout << "]" << endl;

}

int main() {

    int a[] = {45, 35, 15, 30, 10, 12, 6, 5, 20, 50};

    InsertA(a, 9);

    Print(a, sizeof(a)/sizeof(a[0]));

    cout << endl;

    // STL based

    vector<int> v = {45, 35, 15, 30, 10, 12, 6, 5, 20};

    Print(v, v.size());

    v.reserve(15);  // Reserve space for 15 elements

    Insert(v, 50);

    Print(v, v.size());

    cout << "Create Heap" << endl;

    int b[] = {10, 20, 30, 25, 5, 40, 35};

    Print(b, sizeof(b)/sizeof(b[0]), 'b');

    vector<int> u;

    CreateHeap(u, b, sizeof(b)/sizeof(b[0]));

    Print(u, u.size(), 'u');

    cout << "Inplace Insert" << endl;

    createHeap(b, sizeof(b)/sizeof(b[0]));

    Print(b, sizeof(b)/sizeof(b[0]), 'b');

    return 0;

}
```
#### Delete Operation in maxheap


> [!NOTE] Title
> - top most node is removed
> - last node node takes its place
> - preserve complete binary tree after deletion
> - For preserving the complete binary tree the nodes left and right child is compared 
> - the largest child replaces the root node if child node is larger  
> - Deletion takes O(log n ) times

![Pasted image 20241117154830.png](/img/user/Attachments/Pasted%20image%2020241117154830.png)

![Pasted image 20241117162721.png](/img/user/Attachments/Pasted%20image%2020241117162721.png)


> [!important] Title
> if you delete the element largest number get deleted
> if we keep the deleted element in the empty space after deleting all the element in heap we will get the sorted array
> ![Pasted image 20241117155149.png](/img/user/Attachments/Pasted%20image%2020241117155149.png)


#### Basic code for deletion

```cpp
nt Delete(int A[], int n){
    int x = A[0];  // Max element
    A[0] = A[n-1];
 
    int i = 0;
    int j = 2 * i + 1;
 
    while (j < n-1){
        // Compare left and right children
        if (A[j] < A[j+1]){
            j = j+1;
        }
 
        // Compare parent and largest child
        if (A[i] < A[j]){
            swap(A, i, j);
            i = j;
            j = 2 * i + 1;
        } else {
            break;
        }
    }
    return x;
}
```

# Heap Sorting

![Pasted image 20241117155748.png](/img/user/Attachments/Pasted%20image%2020241117155748.png)

> elements of array is inserted in the heap then deleted 
> see above how to insertion and deletion works

#### Time complexity of heap sorting is 
> n.logn for creating the heap and n.logn for deleting the heap
> Therefore time complexity is 2\*n.log(n) = O(nlog(n))

## Heapify

> We look from Right and look if that's node subtree is heap or not if not then adjust to adjust look its child subtree then adjust the parent node with largest then again adjust the adjust node if it is still not a heap


![Pasted image 20241117160248.png](/img/user/Attachments/Pasted%20image%2020241117160248.png)

![Pasted image 20241117160409.png](/img/user/Attachments/Pasted%20image%2020241117160409.png)
> adjust 25 

> Time complexity of heapify is O(n). this is faster


#### Code

```cpp
#include <iostream>

using namespace std;
 
void swap(int A[], int i, int j){
    int temp = A[i];
    A[i] = A[j];
    A[j] = temp;
}
 
int Delete(int A[], int n){
    int x = A[0];  // Max element
    A[0] = A[n-1];
 
    int i = 0;
    int j = 2 * i + 1;
 
    while (j < n-1){
        // Compare left and right children
        if (A[j] < A[j+1]){
            j = j+1;
        }
 
        // Compare parent and largest child
        if (A[i] < A[j]){
            swap(A, i, j);
            i = j;
            j = 2 * i + 1;
        } else {
            break;
        }
    }
    return x;
}
 
void Heapify(int A[], int n){
    // # of leaf elements: (n+1)/2, index of last leaf element's parent = (n/2)-1
    for (int i=(n/2)-1; i>=0; i--){
 
        int j = 2 * i + 1;  // Left child for current i
 
        while(j < n-1){
            // Compare left and right children of current i
            if (A[j] < A[j+1]){
                j = j+1;
            }
 
            // Compare parent and largest child
            if (A[i] < A[j]){
                swap(A, i, j);
                i = j;
                j = 2 * i + 1;
            } else {
                break;
            }
        }
    }
}
 
template <class T>
void Print(T& vec, int n, string s){
    cout << s << ": [" << flush;
    for (int i=0; i<n; i++){
        cout << vec[i] << flush;
        if (i < n-1){
            cout << ", " << flush;
        }
    }
    cout << "]" << endl;
}
 
int main() {
 
    int A[] = {5, 10, 30, 20, 35, 40, 15};
    Print(A, sizeof(A)/sizeof(A[0]), "A");
 
    Heapify(A, sizeof(A)/sizeof(A[0]));
    Print(A, sizeof(A)/sizeof(A[0]), "Heapified A");
    cout << endl;
 
    int B[] = {5, 10, 30, 20};
    Print(B, sizeof(B)/sizeof(B[0]), "B");
 
    Heapify(B, sizeof(B)/sizeof(B[0]));
    Print(B, sizeof(B)/sizeof(B[0]), "Heapified B");
 
    return 0;
}
```

### Time Complexity

1. **Heapify**: O(log⁡n) per node (due to the tree height).
2. **Build-Heap**: O(n) because the number of nodes decreases exponentially at deeper levels of the tree.

**Overall Time Complexity**: O(n) // O(log n) + O(n).


### Space Complexity

- **Auxiliary Space**: O(1), as heap construction is done in-place.
- **Overall Space Complexity**: O(1).


## Priority Queue



> [!NOTE] Title
> we implement smaller Higher priority we use min heap and for large number higher priority use max heap

![Pasted image 20241117161137.png](/img/user/Attachments/Pasted%20image%2020241117161137.png)
