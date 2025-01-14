PRINTING PATTERN:
6*6*6*6

5*5*5

4*4

3

3

4*4

5*5*5

6*6*6*6

PREREQUISITE:
Basic knowledge of C language and use of loops.

ALGORITHM:
Take the number of rows as input from the user and store it in any variable.(‘r‘ in this case).
Divide the value of ‘r’  by 2 and replace it in r. And give this value to count and increase count by 2.
Run a loop ‘r’ number of times to iterate through each of the rows. From i=0 to i<r. The loop should be structured as for( i=0 ; i<r : i++).
Run a loop from j=r to j>i. The loop should be structured as for(j=r; j>i ; j–)
Run an if statement if(j!=r). If true the print star and count else only print count.
Then in the outer if statement decrement count. Then print a newline
Outside this loop increment count and run a loop from i=0 to i<r. The loop should be structured as for( i=0 ; i<r : i++).
Run a nested loop from j=0 to j<=i . The loop should be structured as  for( j=0 ; j<=i ; j++). Inside the loop run an if statement if(j!=0) then print star and digit else print only digit.
Outside the loop increment  count and print a newline.
CODE IN C:
#include<stdio.h>
int main()
{
int i,j,r,count;//declaring integer variables i,j for loops , r for number of rows
printf("Enter the number of rows :\n");//asking user for the number of rows;
scanf("%d",&r);//taking number of rows and saving in variable r
r=r/2;
count=r+2;
for(i=0;i<r;i++) //loop for number of rows
  {
    for(j=r;j>i;j--)//loop to print digit in every column of a row
      {
        if(j!=r)
          {
            printf("*%d",count);//printing digit
          }
        else
          {
            printf("%d",count);//printing digit
          }
      }
    count--;
    printf("\n");//printing newline
  }
count++; //intialising count =3
for(i=0;i<r;i++) //loop for number of rows
  {
    for(j=0;j<=i;j++) //loop to print digit in every column of a row
      {
        if(j!=0)
          {
            printf("*%d",count);//printing digit
          }
        else
          {
            printf("%d",count);//printing digit
          }
      }
    count++; //incrementing count
    printf("\n"); //printing newline
  }
}
TAKING INPUT:DISPLAYING OUTPUT:
