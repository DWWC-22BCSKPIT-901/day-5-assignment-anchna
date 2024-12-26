#include <iostream>
#include <vector>
using namespace std;

bool isPresent(const vector<int>& arr, int k) {
    int left = 0, right = arr.size() - 1;
    while (left <= right) {
        int mid = left + (right - left) / 2; 
        if (arr[mid] == k) {
            return true; 
        } else if (arr[mid] < k) {
            left = mid + 1; 
        } else {
            right = mid - 1;
        }
    }
    return false; 
}
int main() {
    vector<int> arr1 = {1, 2, 3, 4, 6};
    int k1 = 6;
    cout << (isPresent(arr1, k1) ? "true" : "false") << endl; 

    vector<int> arr2 = {1, 2, 4, 5, 6};
    int k2 = 3;
    cout << (isPresent(arr2, k2) ? "true" : "false") << endl; 
    vector<int> arr3 = {1, 2, 4, 5, 6};
    int k3 = 6;
    cout << (isPresent(arr3, k3) ? "true" : "false") << endl; 

    return 0;
}
