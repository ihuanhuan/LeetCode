# LeetCode 1877
Some self-thinking methods for solving LeetCode questions

//To solve this question, we sort the list before counting the maximum
so that we can easily get the optimal answer

class Solution:
    def minPairSum(self, nums: List[int]) -> int:
        nums.sort()
        list_couple = []
        for i in range(int(len(nums)/2)):
            value = nums[i] + nums[-(i+1)]
            list_couple.append(value)
        return max(list_couple)
