# Scenario:
```
You run an online education platform.
Students submit assignments with scores. You are given data in the form of a list of (student_name, score) pairs.
You must find:

· The student with the highest total score (if tie, any student).

Explanation:

· Store student names and accumulate scores using a dictionary.
. After all inputs, find the student with the maximum score.

Input Format:

. First line: an integer n (number of entries)
. Next n lines: space-separated student_name score

Output Format:

. Print the name of the student with the highest total score.

Constraints:

. 1≤n ≤ 500
. 0≤score ≤ 100

Sample Input:

5

Alice 85
Bob 90
Alice 10
Bob 5
Charlie 80

Sample Output:

Alice

Explanation of Output:

. Alice: 85 + 10 = 95
. Bob: 90 + 5 = 95
. Charlie: 80
. Alice and Bob tie, but Alice appeared first (acceptable by tie rule).
```
```python
n=int(input())
scores={}
i=0
while i<n:
  name, score=input().split()
  scores[name]=scores.get(name,0)+int(score)
  i+=1
max_score=max(scores.values())


for student in scores:
  if scores[student]==max_score:
    print(student)
    break
```
