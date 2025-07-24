# Leetcode-2520.-Count-the-Digits-That-Divide-a-Number

# Description

Given an integer num, return the number of digits in num that divide num.

An integer val divides nums if nums % val == 0.
# Solution
In the  problem we have been given an integer number num .

Our aim is to find out how many number of digits in the integer number are divisible by the number itself.

Lets say the num = 1248

To prove that each digit in the number will be divisible to the number , we have to find the remainder by dividing the number with 10 using a while loop .

1248 % 10=8

1248 is divisible by 8 as well

Hence increment the counter by 1 .

Now , let's check for the other digit : 1248/10 =124 

# Algorithm

1. Create a variable named count to count the number of digits which are divisible by the number.
2. Create another variable named original , which stores the value of num for computation purposes.
3. Use a while loop which loops through each number in the integer number until it is 0.
4. Next in order to find the digit , find out the remainder of the number.
5. divide the digit with the number.
6. If the number is divisible then increment the count by 1.
7. Mpvoe on to the next digit by dividing the number with 10.

# Code
class Solution:

    def countDigits(self, num: int) -> int:
        original=num
        count=0
        while num>0:
            digit=num%10
            if digit!=0 and original%digit==0:
                count +=1
            num//=10
        return count

# Time Complexity

The function processes each digit of the number num once.

If num has d digits, the loop runs d times.

For each digit, the operation original % digit takes O(1) time.

So, the overall time complexity is O(d), where d is the number of digits in num.
