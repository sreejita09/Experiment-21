# Experiment 21
# Aim
# Apparatus 
VS code 
# Theory 

# Codes 
~~~
#include <iostream>
using namespace std;

int binarySearch(int arr[], int size, int target) {
    int low = 0, high = size - 1;
    
    while (low <= high) {
        int mid = low + (high - low) / 2; 
        if (arr[mid] == target)
            return mid;
        if (arr[mid] < target)
            low = mid + 1;
        else
            high = mid - 1;
    }
    return -1;
}
int main() {
    int arr[] = {2, 3, 4, 10, 40}; 
    int size = sizeof(arr) / sizeof(arr[0]);
    int target = 10;
    int result = binarySearch(arr, size, target);
    if (result != -1)
        cout << "Element found at index " << result << endl;
    else
        cout << "Element not found in array" << endl;
        
    return 0;
}
~~~
output: 
![image](https://github.com/user-attachments/assets/ee3a00ab-f2ad-4c6e-bbe7-7451b770ded2)


code 2 
~~~
#include <iostream>
using namespace std;

// Function for linear search
int linearSearch(int arr[], int size, int target) {
    for (int i = 0; i < size; i++) {
        if (arr[i] == target) {
            return i;  // Return the index if target is found
        }
    }
    return -1;  // Return -1 if the target is not found
}

int main() {
    int arr[] = {2, 3, 4, 10, 40};  // Unsorted or sorted array
    int size = sizeof(arr) / sizeof(arr[0]);
    int target = 10;
    
    int result = linearSearch(arr, size, target);
    
    if (result != -1)
        cout << "Element found at index " << result << endl;
    else
        cout << "Element not found in array" << endl;
        
    return 0;
}
~~~
![image](https://github.com/user-attachments/assets/10850572-89d2-4139-aa58-e1eaacfccd2b)
