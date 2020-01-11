Homework for January 6th
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
```.c
#include <stdio.h>

int main(void) {
  int one, two, three, biggest;
  printf("This program tests the biggest out of three numbers\n");
  printf("Enter the first number\n");
  scanf("%d", &one);
  printf("Enter the second number\n");
  scanf("%d", &two);
  printf("Enter the third number\n");
  scanf("%d", &three);
  if(one > two && one > three){
    biggest = one;
  }
  else if(two > one && two > three){
    biggest = two;
  }
  else if(three > one && three > two){
    biggest = three;
  }
  else{
    printf("Error\n");
  }
  printf("First number: %d  Second number: %d Third Number: %d", one, two, three);
  printf("%d is the biggest number\n", biggest);
}
```

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
```.c
#include <stdio.h>

int main(void) {
  int math, phy, chem, total, mp;
  printf("This program checks your eligibility for Western's Engineering Program\n");
  printf("Please enter the following:\n");
  printf("Your math mark\n");
  scanf("%i", &math);
  printf("Your physics mark\n");
  scanf("%i", &phy);
  printf("Your chemistry mark\n");
  scanf("%i", &chem);
  total = math + phy + chem;
  mp = math + phy;
  if((math >= 65 && phy >= 55 && chem >= 50 && total >= 180) || (mp >= 140)){
    printf("You are eligible for admission.");
  }
  else{
    printf("Sorry, you are not eligible for admission.");
  }
}
```

### #7
```.c
#include <stdio.h>

int main(void) {
  int temp;
  printf("This program describes the temperature\n");
  printf("Please enter a temperature in celsius\n");
  scanf("%i", &temp);
  if(temp < 0){
    printf("Freezing weather.\n");
  }
  else if(0 < temp && temp < 10){
    printf("Very Cold weather.\n");
  }
  else if(10 < temp && temp < 20){
    printf("Cold weather.\n");
  }
  else if(20 < temp && temp < 30){
    printf("Normal weather.\n");
  }
  else if(30 < temp && temp < 40){
    printf("It's Hot.\n");
  }
  else if(40 <= temp){
    printf("It's Very Hot.\n");
  }
}
```

### #8
```.c
#include <stdio.h>
void exit(int status);
int main(void) {
  int angles[3];
  int total;
  printf("This program determines a triangle's type\n");
  printf("Please enter one angle\n");
  scanf("%i", &angles[0]);
  printf("Please enter another angle\n");
  scanf("%i", &angles[1]);
  printf("Please enter the final angle\n");
  scanf("%i", &angles[2]);
  }
  for(int i=0; i<3; i++){
    if(angles[i] == 90){
      printf("This is a right angle triangle\n");
      exit(0);
    }
    else if(angles[i] > 90){
      printf("This is an obtuse triangle\n");
      exit(0);
    }
  }
  printf("This is an acute triangle\n");
}
```

### #9
```.c
#include <stdio.h>
void exit(int status);
int main(void) {
  int angles[3];
  int total;
  printf("This program determines if a tirangle is valid\n");
  printf("Please enter one angle\n");
  scanf("%i", &angles[0]);
  printf("Please enter another angle\n");
  scanf("%i", &angles[1]);
  printf("Please enter the final angle\n");
  scanf("%i", &angles[2]);
  total = angles[0] + angles[1] + angles[2];
  if((angles[0] + angles[1] + angles[2]) != 180){
    printf("This triangle is invalid.");
    exit(0);
  }
}
```

### #10
```.c
#include <stdio.h>

int main(void) {
  int id, unit, charge, surcharge;
  double rate;
  char name[20];
  printf("This program calculates your electricity bill.");
  printf("Please enter your IDNO to begin\n");
  scanf("%d", &id);
  printf("Please enter your name\n");
  scanf("%s", name);
  printf("Please enter the unit of electricity you have consumed\n");
  scanf("%d", &unit);
  if(unit <= 199){
    rate = 1.20;
    charge = unit * rate;
  }
  else if(unit >= 200 && unit < 400){
    rate = 1.50;
  }
  else if(unit >= 400 && unit < 600){
    rate = 1.80;
  }
  else if(unit >= 600){
    rate = 2;
  }
  else{
    printf("Error. Invalid entry for unit.");
  }
  charge = unit * rate;
  if(charge > 400){
    surcharge = charge * 0.15;
  }
  printf("Customer IDNO: %d\n", id);
  printf("Customer name: %s\n", name);
  printf("unit Consumed: %d\n", unit);
  printf("Amount Charged @Rs %lf per unit: %d\n", rate, charge);
  printf("Surcharge amount: %d\n", surcharge);
  printf("Net Amount Paid by the Customer: ");
  printf("%i\n", charge + surcharge);
}
```

Weekend Practice
====

### #1
```.c
#include <stdio.h>
//This program gives an average of 10 numbers inputted by the user
int main(void) {
  int total, average;
  for(int i=0; i<10; i++){
    int num = 0;
    // 1. Get input
    printf("Please enter a number\n");
    scanf("%i", &num);
    // 2. Add to total
    total = num + total;
  }
  // 3. Calculate average
  average = total / 10;
  printf("The average is %i.\n", average);
}
```

### #2
```.c
#include <stdio.h>
//This program displays the cubes of numbers up to an inputted number
int main(void) {
  int last;
  printf("Please enter the number of cubes you would like\n");
  scanf("%i", &last);
  for(int i=1; i<=last; i++){
    int cube = (i * i * i);
    printf("The number is: %i and the cube is: %i\n", i, cube);
  }
}
```

### #3
```.c
#include <stdio.h>
//This program calculates the factorial of an input
int main(void) {
  int num;
  int factorial = 1;
  printf("Please enter the number you would like the factorial of\n");
  scanf("%i", &num);
  for(int i=1; i<=num; i++){
    factorial = (i * factorial);
  }
  printf("The factorial is %i\n", factorial);
}
```

### #4
```.c

```
