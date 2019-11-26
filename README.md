Feedback Nov 26 (you can delete this section later it will remain in the history)

|No.|How to improve        |
|-|------------- |
|①| Under the development section, you are including all the source code for the programs. It is better if you include only small parts of the code that are new to you or that show an important algorithm. This is because the source code is anyway in the repo so no need to repeat. 

**For example:** The code below shows how to read the status of a button connected to port 13 in the Arduino:
```.c
bool A = digitalRead(13);
```
Note that the variable A was created of type Bool since the input is binary data.|

|No.|How to improve        |
|-|------------- |
|②| Add figure caption to your figures and then explain what you see in them. Figures are quite ambiguous by themselves.| 

**For example:**

<img src="IMG_6146.JPG" width="50%" height="50%">

Fig. 1. My beautiful notes about boolean gates

As shown in Fig. 1, I can take really neat notes in class. The titles are highligthed and easy to read, .... etc.

|No.|How to improve        |
|-|------------- |
|③| Start wotking on the Definition of the problem, proposed solution and success criteria| 

-----

From Earth to Mars
====

Language conversion with Arduino IDE and Modern C

Contents
----
  1. [Planning](#planning)
  2. [Solution Overview](#solution_overview)
  3. [Development](#development)
  4. [Evaluation](#evaluation)
  
  
Planning
---
## Definition of the problem

## Rationale for proposed solution

## Success criteria

Solution_Overview
---
## Test plan

## System diagram

## Flow diagrams

Development
----

What is Usability?

According to [1](#1), usability is "the extent to which a product can be used by specified users to achieve specified goals with effectiveness, efficiency, and satisfaction in a specified context of use."

## Existing tools

### Learning to use Arduino

Arduino has two main components that need to be learned in order to master its use:
1. Language (Modern C)
2. Hardware (Arduino)

**Modern C**

In order to learn Modern C, we took for loops that had already been completed in bash, and translated them into Modern C. An example is shown below. Both programs have the same outputs.

*Addition Loop - Bash*
```.sh
even=0
odd=0
for (( i=1; i<1001; i++ ))
do
        (( remainder= $i % 2 ))
        if [ $remainder == 0 ]; then
                (( even=$even + $i ))
        else
                (( odd=$odd + $i ))
        fi
done

echo "The sum of the odd numbers from 1 to 1000 is $odd"
echo "The sum of the even numbers from 1 to 1000 is $even"
```

*Addition Loop - Modern C*
```.c
void setup()
{
   Serial.begin(9600);
}

unsigned int even = 0;
unsigned int odd = 0;

void loop()
{
  for (int i = 0; i < 1001; i++){
    if (i % 2 == 0){
      (even + i);
    }
    if (i % 2 != 0){
      (odd + i);
    }
  }
}

void print()
{
  Serial.print(even);
  Serial.print("\n");
  Serial.print(odd);
}
```

**Arduino**

In order to learn Arduino, we experimented with TinkerCad and the Arduino kits to build circuits. Below is a photo of a traffic light model we built, along with the code used for it.

![Arduino Circuit](IMG_5886.PNG)

```.c
void setup()
{
  pinMode(13, OUTPUT);
  pinMode(11, OUTPUT);
  pinMode(8, OUTPUT);
}

void loop()
{
  red();
  green();
  yellow();
}

void red()
{
  digitalWrite(13, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(13, LOW);
}
  
void yellow()  
{
  digitalWrite(11, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(11, LOW);  
}

void green()
{
  digitalWrite(8, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(8, LOW);
}
```
### Boolean Operators

![Boolean Notes](IMG_6146.JPG)

*Learning to form logic diagrams and equations with binary charts


## References

(1) ISO. (n.d.). Usability of consumer products and products for public use. Retrieved from https://www.iso.org/obp/ui/#iso:std:iso:ts:20282:-2:ed-2:v1:en.

Evaluation
----
