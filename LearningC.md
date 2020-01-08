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
