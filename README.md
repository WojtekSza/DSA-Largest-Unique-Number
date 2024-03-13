# DSA-Largest-Unique-Number
Given an integer array nums, return the largest integer that only occurs once. If no integer occurs once, return -1.
```
Input: nums = [5,7,3,9,4,9,8,3,1]
Output: 8
Explanation: The maximum integer in the array is 9 but it is repeated. The number 8 occurs only once, so it is the answer.
```
```
from collections import defaultdict
class Solution:
    def largestUniqueNumber(self, nums: List[int]) -> int:
        counts=defaultdict(int)
        ans=-1
        #time cost of loop O(n)
        for num in nums:
            #space cost of loop O(n)
            counts[num]+=1
        #time cost of loop O(n)    
        for i,j in counts.items():
            if j==1:
                #space cost chech O(1)
                ans=max(ans,i)
        return ans
        '''
        Total time cost O(n) + O(n) = 2O(n)= O(n)
        Total space cost O(n) + O(1) = O(n)
        '''
```
