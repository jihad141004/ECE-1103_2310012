## Assignment 3:
## **Submission Date : November 28, 2024**

## Assignment Name :Find the index of given element in an Array

---
## **Code :**
~~~C
#include <stdio.h>

void solve()
{
  int arr[] = {10, 20, 30, 100, 40, 23, 12, 45, 32, 90};
  int n = sizeof(arr)/sizeof(arr[0]);
  int key;
  printf("Enter the value you want to find: ");
  scanf("%d", &key);
  for (int i = 0; i < n; i++)
  {
    if (arr[i] == key)
    {
      printf("%d  found at index : %d", key, i);
      return;
    }
  }
  printf("Value Not found\n");
}

int main()
{
  solve();
}

~~~
## **Output :**
<p align="center">
<img  alt="2310012 index" src="https://github.com/user-attachments/assets/68cb7415-5ead-42be-97ac-42601815cd2a">
</p>

## **Discussion :**
<div align="justify">

In this assignment, We developed a program that will give out the index of given element.If element not found a message will be shown </div>
