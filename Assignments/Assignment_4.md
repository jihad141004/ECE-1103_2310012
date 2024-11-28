
## Assignment 4:
## **Submission Date : November 28, 2024**

## Assignment Name :Our next program prints a table showing the value of $100 invested at different rates of interest over a period of years. The user will enter an interest rate and the number of years the money will be invested. The table will show the value of the money at one-year intervals-at that interest rate and the next four higher rates- assuming that interest is compounded once a year. Here's what a session with the program will look like:

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

In this assignment, We developed a program that will give out the index of given element.If element not found a message will be shown </div>
