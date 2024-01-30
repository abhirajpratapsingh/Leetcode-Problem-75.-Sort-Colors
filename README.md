

# Intuition
<!-- Describe your first thoughts on how to solve this problem. -->
- The approach involves counting the occurrences of each color (0, 1, and 2) in the array.



# Approach
<!-- Describe your approach to solving the problem. -->
- Initialize counters for red, white, and blue.
- Traverse the array to count the occurrences of each color.
- Update the original array based on the counts, placing 0s first, then 1s, and finally 2s.

---

# Complexity

- **Time complexity: O(n)** (as we traverse the array twice)
- **Space complexity: O(1)** (as we use a constant amount of space for counters)

---
# Code
```
class Solution {
public:
    void sortColors(vector<int>& nums) 
    {
        int red=0;int white=0;int blue=0;
        for(int i=0;i<nums.size();i++)
        {
            if(nums[i]==0)
                red++;
            else if(nums[i]==1)
                white++;
            else if(nums[i]==2)
                blue++;
        }
        for(int i=0;i<nums.size();i++)
        {
            if(red)
            {
                nums[i]=0;
                red--;
            }
            else if(white)
            {
                nums[i]=1;
                white--;
            }
            else
               nums[i]=2;
        }
    }
};
```
---
