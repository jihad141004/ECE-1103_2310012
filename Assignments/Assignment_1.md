
## Assignment Name : Create a simple banking system in C using a switch statement to manage these menu options
1.Deposit: Ask for an amount and add it to the balance.

2.Withdraw: Ask for an amount and deduct it if funds are sufficient; otherwise, show an
error.

3.Balance Inquiry: Display the current balance.

4.Exit: End the program.

Validate inputs to prevent negative deposits or withdrawals and handle insufficient funds.

## **Submission Date : November 7, 2024**

---
## **Code :**
~~~
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

In this assignment we created a  Banking Menu system where users can choose different options according to their needs. We also handled incorrect inputs to prevent errors.
</div>

## Assignment Name :
Guess the Secret Number with Limited Attempts
Create a number guessing game where the program selects a random secret number
between 1 and 50. The user has to guess the number, and they get unlimited attempts until
they guess correctly. However, if they exceed 10 attempts, the game stops, and a message
indicates that they’ve run out of attempts.
Use a while loop to keep asking the user for guesses, and use break when:
1.The user guesses correctly.
2.The attempt limit (10 guesses) is reached.
---
## **Code :**
~~~
#include<stdio.h>
#include<stdlib.h>
#include<time.h>

void solve(){
    srand(time(NULL));
    int secret_num = (rand()%49)+1;
    int choice, count = 0;
    while(1){
        printf("Enter a number between (1-50):  ");
        scanf("%d", &choice);
        if(choice==secret_num){
            printf("\nCongratulation You Guessed Correctly! \n");
            return;
        }
        if(choice>secret_num && count<9 ){
            printf("Guess smaller\n");
        }else if(choice<secret_num && count<9 ){
            printf("Guess Bigger\n");
        }
        count++;
        if(count==10){
            break;
        }
    }
    printf("\nSorry YOu lost !\n");
}
int main(){
    solve();
}
~~~
## **Output :**
Successfull guess:
<p align="center">
<img  alt="2310012 Secret random number" src="https://github.com/user-attachments/assets/793c5b55-af73-4645-b886-4006a8d7d155">
</p>
Unsuccessfull guess:
<p align="center">
<img  alt="2310012 Secret random number" src="https://github.com/user-attachments/assets/6fef54e2-db8f-46a1-86a0-c8da8a567c10">
</p>

## **Discussion :**
<div align="justify">

In this assignment, we developed a program in which the computer randomly generates a number, and the objective is for the user to guess that number. If the user successfully guesses the number within 10 attempts or fewer, a winning message is displayed; otherwise, a losing message is shown.
</div>
