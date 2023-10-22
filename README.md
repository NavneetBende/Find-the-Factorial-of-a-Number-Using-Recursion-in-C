# Find-the-Factorial-of-a-Number-Using-Recursion-in-C

Factorial of a Number using Recursion in C
Here, in this page we will discuss the program to find the factorial of a number using recursion in C programming Language. We will discuss various methods to solve the given problem.

Factorial of a Number using Recursion in C
Method Discussed :
Method 1 : Using Recursion
Method 2 : Using Iteration.
Let’s discuss them one by one in brief,

Method 1:
Call function getFactorial(num)
Set base case when num== 0 return 1
Other cases return num * getFactorial(num-1);
Time and Space Complexity :
Time complexity: O(N)
Space complexity: O(1)
Auxiliary Space complexity (Function call stack): O(N)
Method 1 : Code in C
Run
#include<stdio.h>
int getFactorial(int num)
{
    if(num == 0)
        return 1;
        
    return num * getFactorial(num-1);
}
int main ()
{
    int num = 7;
    
    int fact = getFactorial(num);
    
    printf("Fact %d: %d",num, fact);
}
Output :
Fact 7: 5040
Method 2:
Initialize fact = 1
If num < 0 : Print Error as we can’t calculate factorial of a negative number
Else run a iterative loop in iteration of (i) between [1, num]
Set fact = fact * i
Print the value of fact.
Time and Space Complexity :
Time complexity: O(N)
Space complexity: O(1)
Method 2 : Code in C
Run
#include<stdio.h>
int main ()
{
    int num = 7, fact = 1;
    
    // Can't calculate factorial of a negative number
    if(num < 0)
        printf("Error");
    else
    {
        for(int i = 1; i <= num; i++)
            fact = fact * i;
    }
    
    printf("Fact %d: %d",num, fact);
}   
  
Output :
Fact 7: 5040
