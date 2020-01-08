Homework for January 8th
-----

### #1: Make a program that checks if two integers are the same

```.c
#include <stdio.h>

int main(void) {
  int one;
  int two;
  printf("Enter integer #1\n");
  scanf("%i",&one);
  printf("Enter integer #2\n");
  scanf("%i",&two);
  if (one==two) {
    printf("Integers are the same");
  }
  else {
    printf("Integers are not the same");
  }
}
```

### #2: Make a program that checks if a year is a leap year

```.c
#include <stdio.h>

int main(void) {
  int year;
  printf("Enter a year\n");
  scanf("%i",&year);
  if (year % 4 == 0) {
    printf("Year is a leap year");
  }
  else {
    printf("Year is not a leap year");
  }
}
```


January 8th Worksheet
===

### #1
```.c
#include <stdio.h>

int main(void) {
  int number;
  printf("This program tests whether a number is even or odd\n");
  printf("Please enter a number\n");
  scanf("%d",&number);
  if(number % 2 == 0){
    printf("%d is even\n", number);
  }
  else {
    printf("%d is odd\n", number);
  }
}
```

### #2
```.c
#include <stdio.h>

int main(void) {
  int number;
  printf("This program tests whether a number is positive or negative\n");
  printf("Please enter a number\n");
  scanf("%d",&number);
  if(number < 0){
    printf("%d is a negative number\n", number);
  }
  else if(number > 0){
    printf("%d is a positive number\n", number);
  }
  else {
    printf("%d is zero\n", number);
  }
}
```

### #3
```.c
#include <stdio.h>

int main(void) {
  int age;
  printf("This program tests whether or not you are eligible to vote\n");
  printf("Please enter your age\n");
  scanf("%d",&age);
  if(age < 18){
    printf("Sorry, you are not eligible to vote.");
  }
  else {
    printf("Congratulations! You are eligible to vote");
  }
}
```

### #4

### #5
```.c
#include <stdio.h>

int main(void) {
  int x, y;
  printf("This program determines what quadrant a point lies in\n");
  printf("Enter the value for x\n");
  scanf("%d", &x);
  printf("Enter the value for y\n");
  scanf("%d", &y);
  if(x < 0 && y < 0){
    printf("%d,%d is in Quadrant 4\n", x,y);
  }
  else if(x < 0 && y > 0){
    printf("%d,%d is in Quadrant 2\n", x,y);
  }
  else if(x > 0 && y < 0){
    printf("%d,%d is in Quadrant 3\n", x,y);
  }
  else if(x > 0 && y > 0){
    printf("%d,%d is in Quadrant 1\n", x,y);
  }
  else{
    printf("%d,%d is on an axis", x,y);
  }
}
```

### #6
