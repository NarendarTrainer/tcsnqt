# Scenario:
```
You are managing a data analysis tool that tracks the behavior of numbers over time.
You are given a list of integers representing measurements recorded sequentially.
You need to determine the length of the longest continuous subsequence where the numbers keep increasing.

This helps identify periods of consistent growth.

Explanation:

. Traverse the list.
. For each number, check if it is greater than the previous number.
. Count consecutive increases.
. Whenever the sequence breaks, reset the counter.
· Return the maximum length found.

Input Format:

· A single line containing space-separated integers.

Output Format:

· A single integer representing the length of the longest continuous increasing subsequence.

Constraints:
. 1 ≤ list length ≤ 1000
· -104 ≤ list element ≤ 104

Sample Input:

12245623

Sample Output:

3

Explanation of Output:

. Increasing sequence: 2->4->5->6-> Length = 3
· Other sequences are shorter.
· Hence, longest increasing subsequence has length 3.
```
```python
nums=list(map(int,input().split()))
max_len=1
current_len=1
i=1
while i<len(nums):
  if nums[i]>nums[i-1]:
    current_len+=1
    if current_len>max_len:
      max_len=current_len
  else:
    current_len=1
  i+=1
print(max_len-1)
```
