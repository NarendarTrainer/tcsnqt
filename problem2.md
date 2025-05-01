# Scenario:
```
In a text processing engine, each character needs to be categorized into:

· Alphabets (lowercase/uppercase)
. Digits
. Special Characters

You are given a string and must return a dictionary where each key ( 'alphabets','digits' , 'special' ) maps to the count of characters in that category.

Explanation:

. Read the string character by character.
. Classify each character.
. Count them using dictionary keys.

Input Format:

· A single line string containing letters, digits, and symbols.

Output Format:

. Three lines:
o alphabets: count
o digits: count
o special: count
Constraints:

. 1≤ string length ≤ 104

Sample Input:

Hello123!@#

Sample Output:

alphabets: 5
digits: 3
special: 3

Explanation of Output:

. Alphabets: H, e, I, I, o-> 5
. Digits: 1,2,3-> 3
. Special: !, @,#->3
````


