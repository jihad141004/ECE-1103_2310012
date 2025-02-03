## Assignment 2:
## **Submission Date : November 8, 2024**
## Assignment Name :Guess the Secret Number with Limited Attempts
Create a number guessing game where the program selects a random secret number
between 1 and 50. The user has to guess the number, and they get unlimited attempts until
they guess correctly. However, if they exceed 10 attempts, the game stops, and a message
indicates that they’ve run out of attempts.
Use a while loop to keep asking the user for guesses, and use break when:
1.The user guesses correctly.
2.The attempt limit (10 guesses) is reached.

## **Code :**
~~~C
#include<stdio.h>
#include<stdlib.h>
#include<time.h>

void solve(){
    srand(time(NULL));
    int secret_num = (rand()%50)+1;
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
    printf("\nSorry You lost !\n");
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

In this assignment we created a program where computer randomly generates a number and we had to guess that number. If we successfully guess the number in less than or equal top 10 guesses then we will get winning message or else we will get losing message.
</div>
