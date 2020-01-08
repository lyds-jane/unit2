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
