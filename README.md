Explanation of Simple Calculator using Stack Logic

This program is a simple calculator that solves expressions step by step using BODMAS rule.

How it works:

1. It has two lists (stacks):
   - nums → stores numbers
   - ops → stores operators (+, -, *, /, %, ^)

2. Functions:
   - precedence(op): decides which operator has higher priority. For example, * and / have higher priority than + and -.
   - apply(a, b, op): applies the operator on two numbers. Example: apply(2,3,'*') = 6.
   - evaluate(exp): main function that reads the expression character by character and solves it.

3. Inside evaluate():
   - If a number is found → it is stored in nums.
   - If '(' is found → it is stored in ops.
   - If ')' is found → keep solving until '(' is found.
   - If an operator is found → solve higher priority operators first, then store the current one.
   - At the end, solve all remaining operators.

Example:
Expression: 1+2*3*(4-5/4)-(3/5)+2^3

Step by step:
- 5/4 = 1.25
- 4 - 1.25 = 2.75
- 2*3 = 6
- 6*2.75 = 16.5
- 1 + 16.5 = 17.5
- 3/5 = 0.6
- 17.5 - 0.6 = 16.9
- 2^3 = 8
- 16.9 + 8 = 24.9

Final Answer = 24.9

Summary:
- This calculator follows BODMAS rule.
- Handles brackets, power, multiplication, division etc.
- Final answer is the last number in nums.

