# program to find indices of two number in a list that add up to the target

class Solution(object):
    def twoSum(self, nums, target):
        seen = {} 
        for index, value in enumerate(nums):
            left = target - value
            if left in seen:
                return [seen[left], index]  
            seen[value] = index 
        return []

solution = Solution()
l = [2, 4, 6, 3, 7, 5, 8]
a = solution.twoSum(l, 15)
print(a)  
