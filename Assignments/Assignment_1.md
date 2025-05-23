## Assignment 1:
## **Submission Date : November 8, 2024**

## Assignment Name :Create a simple banking system in C using a switch statement
Create a simple banking system in C using a switch statement to manage these menu options:

1.Deposit: Ask for an amount and add it to the balance.

2.Withdraw: Ask for an amount and deduct it if funds are sufficient; otherwise, show an
error.

3.Balance Inquiry: Display the current balance.

4.Exit: End the program.
Validate inputs to prevent negative deposits or withdrawals and handle insufficient funds.



---
## **Code :**
~~~C
#include <stdio.h>
void display()
{
  printf("\n------Banking System MENU -------\n");
  printf("   1 : Deposit\n ");
  printf("   2 : Withdraw\n ");
  printf("   3 : Balance Inquiry\n ");
  printf("   4 : Exit\n\n ");
}

void solve()
{
  double balance = 0.0, amount;
  int choice;

  while (1)
  {
    display();
    printf("Enter you choice: ");
    scanf("%d", &choice);
    if (choice == 4)
    {
      break;
    }
    else
    {
      switch (choice)
      {
      case 1:

        printf("Enter amount to deposit: ");
        scanf("%lf", &amount);
        if (amount < 0)
        {
          printf("\nEnter valid amount\n");
        }
        else
        {
          balance += amount;
        }
        break;
      case 2:
        printf("Enter amount to Withdraw: ");
        scanf("%lf", &amount);
        if (amount > balance || amount < 0)
        {
          printf("\nEnter valid amount\n");
        }
        else
        {
          balance -= amount;
        }
        break;
      case 3:
        printf("Your current Balance :  %.2lf\n", balance);
        break;
      default:
        printf("Enter a valid option\n");
        break;
      }
    }
  }
}

int main()
{
  solve();
}


~~~
## **Output :**
<p align="center">
<img  alt="2310012 Banking system" src="https://github.com/user-attachments/assets/60330ed7-8c28-40c4-bb1b-72423ee4a947">
</p>

## **Discussion :**
<div align="justify">

In this assignment, we developed a banking menu system that allows users to select various options based on their needs. Additionally, we implemented input validation to handle incorrect entries, ensuring a smooth and error-free user experience.</div>

