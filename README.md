# non-recursive-linear-search
#include<iostream>
using namespace std;
//function to perform non recursive linear search
int nonRecursiveLinearSearch(int arr[], int n, int key) {
    for (int i = 0; i < n; i++) {
        if (arr[i] == key) {
            return i; // Return the index if the key is found
        }
    }
    return -1; // Return -1 if the key is not found
}
int main(){
    int arr []={10,20,30,40,50};
    int n = sizeof(arr) / sizeof(arr[0]);
    //First test case
    int key=30;
    int result = nonRecursiveLinearSearch(arr, n, key);
    if (result != -1) {
        cout << "Element "<< key <<"found at index " << result << endl;
    } else {
        cout << "Element " << key <<"not found in the array." << endl;
    }
    //Second test case
    key= 60;//correct assignment
    result = nonRecursiveLinearSearch(arr, n, key);
    if (result != -1) {
        cout << "Element " << key <<"found at index" << result << endl;
    } else {
       cout << "Element " <<key <<"not found in the array." << endl;
    }
    return 0;
}
