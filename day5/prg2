#include <iostream>
#include <vector>
#include <algorithm>
#include <climits>

using namespace std;
long long countLessEqual(const vector<int>& nums1, const vector<int>& nums2, long long x) {
    long long count = 0;
    for (int i = 0; i < nums1.size(); ++i) {
        if (nums1[i] >= 0) {
            count += upper_bound(nums2.begin(), nums2.end(), x / nums1[i]) - nums2.begin();
        } else {
            count += nums2.end() - lower_bound(nums2.begin(), nums2.end(), (x + 1) / nums1[i]);
        }
    }
    return count;
}

int kthSmallestProduct(vector<int>& nums1, vector<int>& nums2, int k) {
    long long left = LLONG_MIN, right = LLONG_MAX;

    while (left < right) {
        long long mid = left + (right - left) / 2;
        if (countLessEqual(nums1, nums2, mid) < k) {
            left = mid + 1;
        } else {
            right = mid;
        }
    }

    return left;
}

int main() {
    vector<int> nums1 = {2, 5};
    vector<int> nums2 = {3, 4};
    int k1 = 2;
    cout << kthSmallestProduct(nums1, nums2, k1) << endl; 
    vector<int> nums3 = {-4, -2, 0, 3};
    vector<int> nums4 = {2, 4};
    int k2 = 6;
    cout << kthSmallestProduct(nums3, nums4, k2) << endl;
    vector<int> nums5 = {-2, -1, 0, 1, 2};
    vector<int> nums6 = {-3, -1, 2, 4, 5};
    int k3 = 3;
    cout << kthSmallestProduct(nums5, nums6, k3) << endl;

    return 0;
}
