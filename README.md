# C-Program-to-Reverse-a-Given-Number

Program to Reverse a Number in C
In this post we will learn how to reverse a number in c. For example, if a user will enter 4567 as input then 7654 will be printed as output. This C program accepts an integer and reverse it.
c program to reverse a number
While loop in C
Working:-
For a user input num

Initialize reverse = 0, rem
Extract the last digit of num (rem = num % 10)
Multiply reverse with 10 & add remainder (reverse = reverse * 10 + rem)
Reduce the original number (num = num/10)
Keep doing this until original number becomes 0
Reverse a given number in C
C program:-
Run

#include<stdio.h>

//main program
int main ()
{
  //variables initialization
  int num, reverse = 0, rem;
  num=1234;
  printf("The number is: %d\n",num);
  
 
  //loop to find reverse number
    while(num != 0)
    {
      rem = num % 10;
      reverse = reverse * 10 + rem;
      num /= 10;
    };
 
  //output
  printf("Reverse: %d\n",reverse);
  
  return 0;
}
// Time complexity O(N)
// Space complexity : O(1)
Output:-
The number is: 1234
Reverse: 4321
While loop in C
Related Pages
Program to print Prime Number in range

Program to find Sum of digits of number

Program to check palindrome or not

Program to check armstrong number

Armstrong number in a given range

Prime Course Trailer

Related Banners
Get PrepInsta Prime & get Access to all 200+ courses offered by PrepInsta in One Subscription

Get Prime
Method 2
This method uses a recursive approach.

Code
Run

#include<stdio.h>

int getReverse(int num, int rev){
if(num == 0)
return rev;

int rem = num % 10;
rev = rev * 10 + rem;

return getReverse(num / 10, rev);
}

//main program
int main ()
{
int num, rev = 0;
num=1234;
printf("The number is: %d\n",num);

printf("Reverse: %d", getReverse(num, rev));
}
Output
The number is: 1234
Reverse: 4321
