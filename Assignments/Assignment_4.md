
## Assignment 4:
## **Submission Date : January 17, 2025**

## Problem 1:
## A   program that prints a table showing the value of $100 invested at different rates of interest over a period of years. The user will enter an interest rate and the number of years the money will be invested. The table will show the value of the money at one-year intervals-at that interest rate and the next four higher rates- assuming that interest is compounded once a year.

---
## **Code :**
~~~C
#include <stdio.h>

void solve()
{
  int arr[5][6];
  double int_rate;
  printf("Enter the Interest rate: ");
  scanf("%lf", &int_rate);
  int tmp = int_rate;
  double p1 = 100, p2 = 100, p3 = 100, p4 = 100, p5 = 100;

  printf("Years    %d%%        %d%%          %d%%         %d%%        %d%%\n", tmp, tmp + 1, tmp + 2, tmp + 3, tmp + 4);

  for (int i = 0; i < 5; i++)
  {
    for (int j = 0; j < 6; j++)
    {
      if (j == 0)
      {
        printf(" %d ", i + 1);
      }
      else if (j == 1)
      {
        p1 += p1 * (int_rate / 100.00);
        printf("    %.2lf ", p1);
      }
      else if (j == 2)
      {
        p2 += p2 * ((int_rate + 1) / 100.00);
        printf("    %.2lf ", p2);
      }
      else if (j == 3)
      {
        p3 += p3 * ((int_rate + 2) / 100.00);
        printf("    %.2lf ", p3);
      }
      else if (j == 4)
      {
        p4 += p4 * ((int_rate + 3) / 100.00);
        printf("    %.2lf ", p4);
      }
      else if (j == 5)
      {
        p5 += p5 * ((int_rate + 4) / 100.00);
        printf("    %.2lf ", p5);
      }
    }
    printf("\n");
  }
}

int main()
{
  solve();
}


~~~
## **Output :**
<p align="center">
<img  alt="2310012 index" src="https://github.com/user-attachments/assets/c6917cb8-c03a-4a9d-8df5-c5bdb5c584ff">
</p>

## **Discussion :**
<div align="justify">

This program calculates the future value of a $100 investment over 5 years at various interest rates, starting with a user-entered rate and increasing by 1% for each subsequent column. It uses the compound interest formula to compute the value of the investment for each year. The results are displayed in a table format, showing the value for each interest rate over the years. The program demonstrates how interest rates impact investment growth when compounded annually. </div>

## Problem 2:
## Exploring Pass by Value and Pass by Reference: Swap Function Implementation in C
---
## **Code :**
~~~C
#include <stdio.h>

void swap_pass_by_reference(int *a, int *b)
{
  *a = *a ^ *b;
  *b = *a ^ *b;
  *a = *a ^ *b;
}
void swap_pass_by_value(int a, int b)
{
  a = a ^ b;
  b = a ^ b;
  a = a ^ b;
}
int main()
{
  int a, b;
  printf("Enter Num1:   ");
  scanf("%d", &a);
  printf("Enter Num2:   ");
  scanf("%d", &b);
  swap_pass_by_value(a, b);
  printf("Swap Result with pass by value      :  a = %d     b = %d \n", a, b);
  swap_pass_by_reference(&a, &b);
  printf("Swap Result with pass by reference  :  a = %d     b = %d ", a, b);
}

~~~
## **Output :**
<p align="center">
<img  alt="2310012 index" src="https://github.com/user-attachments/assets/3fc20b5f-5b7d-40ce-82af-1f2030ef9b48">
</p>

## **Discussion :**
<div align="justify">
This assignment focuses on implementing and comparing two methods of parameter passing in C: pass by value and pass by reference. A swap function is created to interchange the values of two variables, demonstrating the differences between the two approaches. The pass-by-value method works with copies of the variables, while the pass-by-reference method directly modifies the original variables. The assignment highlights the advantages and limitations of each method. It provides practical insight into how parameter passing influences function behavior and data manipulation. </div>
