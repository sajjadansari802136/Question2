# Question 2

## Explanation of development environment
I have used Visual Studio Code to write the code for Question 2 because VS Code is a good choice for development or debugging.

In the first line, the header file #include<stdio.h> contains the valid C sources statements that can be compiled as part of a program. The system will find the file named "stdio.h" and read its entire contents in, replacing this statement.

In Method 1, recursion has been used to find F(n). If n is less than or equal to 2 then we return n else the function will recursively call itself and will return F(n-3) + F(n-2) which is same as F(n).

In Method 2, Dynamic Programming has been used to find F(n). In this, we created an array and stored the results using previous calculated values by running a for loop from i=3 to i=n. At i=n, we get the value of F(n) and come out of loop and finally we return F(n).

In Method 3, Space Optimization has been used to find F(n). In this, we used variables a0, a1, a2 and a3. Initially, a0, a1 and a2 are equal to F[0], F[1] and F[2] respectively. If n is 0, we return a0 and if n is 1 we return a1 else we run a for loop updating a0, a1 and a2 after each iteration. When i=n then a2 becomes F(n) and we come out of loop and return a2 which is equal to F(n). 

## Running and compiling the code
First open the Terminal and run the command ‘gcc -v’ to check if you have a compiler installed. If not, you need to download a gcc compiler and install it.

Then we compile the program. To do this we need to use the command gcc followed by the name of the program we are going to execute. In our case, we will use gcc Question2.c

After this, an executable file will be created in the directory where our c file exists in. Eg: Question2.exe

After that we run the program. This is done by simply giving the name of the executable file without any extension. In our case we write Question2 and we will get the output of the code.

## Advantages and Disadvantages
Method 1(Recursion) -> This method is simple to code and it is a naïve approach but it has Exponential time complexity because every function calls two other functions. Also if we consider the function call stack size then it takes O(n) extra space otherwise it takes O(1) extra space. 

Method 2(Dynamic programming) -> This method is better than the first method because it avoids the repeated calls to the function by storing the result using previous calculated results. This helps in reducing the time complexity from exponential to linear i.e time complexity becomes O(n). But the Auxiliary space used is O(n) as we have created the array to store the values.

Method 3 (Space Optimization) -> This method is the most optimized method as compared to other two methods. This is similar to method 2 but instead of storing all the values, we are just storing three values to find the next value because we just need (n-2)th and (n-3)th values to find the nth value. Thus the time complexity remains same i.e O(n) but takes O(1) space. 
