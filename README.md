From Earth to Mars
====

Language conversion with Arduino IDE and Modern C
2
Contents
----
  1. [Planning](#planning)
  2. [Solution Overview](#solution)
  3. [Development](#development)
  4. [Evaluation](#evaluation)
  
  
Planning
---
## Definition of the problem
The year is 2050. NASA has planned a Mars expedition, and needs our help developing a communication system between the Earth and Mars. Since the two planets are so far away, they will have to transmit their communications through the moon. However, due to the lack of infrastructure in space, the following conditions apply:
* Communications between the Earth and the Moon must be done in Morse Code
* Communications between the Moon and Mars must be done in binary
* The people communicating do not know morse code or binary
* The keyboard input is limited to two button inputs

## Rationale for proposed solution
For this program, we will use the Arduino hardware and Modern C language. Before presenting our solution to NASA, we will simulate the situation by being in three different buildings and communicating with a lightbulb. This involves dividing into three teams: Earth, the Moon, and Mars. I am on the Earth team, which means I need to be able to send and recieve messages in morse code and translate them to and from English. 

The user's needs will be met with two buttons and an LCD display being built with the arduino. Then, we will program code to translate from binary and morse code to English, and vice-versa. The keyboard input system will be handled by using alternating keys to change and select options, and having the letters being presented in a matrix that allows for the most efficient system.

The feasibility of this solution is as follows:

*Technical feasibility* - This project can be completed using the arduino hardware.
*Economic feasibility* - Since we are first modelling this software with a lightbulb at our location, developping the software will be very cheap.
*Legal feasibility* - We are working closely with NASA to make ensure that we are complying with all of their legal requirements
*Operational feasibility* - By splitting up into three teams, the project will be completed quickly. Some minor problems could be anticipated through lack of communication, so this will need to be a priority.
*Schedule feasibility* - From learning the arduino to completing the project, this should take no more than two months to complete.

## Success criteria
For the Earth team to be succcessful, it needs to meet the following criteria:
USING TWO BUTTONS...
* A message can be typed in English
* An error within the message can be deleted
* The message can be translated into morse code and shown back to the client
* The message can have the option "SEND"
* A message can be typed in English
* The message can be translated to English and shown back to the client

Solution Overview
---
## Test plan

## System diagram

## Flow diagrams

Development
----

What is Usability?

According to [1](#references), usability is "the extent to which a product can be used by specified users to achieve specified goals with effectiveness, efficiency, and satisfaction in a specified context of use."

Therefore, usability extends beyond the meeting of the success criteria. It is wholly dependent on the user's ability to use the product and feel confident in its functioning.

## Existing tools

The following skills must be developed in order to succcessfully complete the project:
* Learn to use arduino (Language and Hardware)
* Learn how to use & convert numbers to and from Binary
* Understand boolean operators 

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
*Fig. 1* - Addition loop in bash

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
*Fig. 2* - Addition loop in Modern C

These two codes show the differences in functions, variable declarations, commands, and arithmetic operations in the two languages.

**Arduino**

In order to learn Arduino, we experimented with TinkerCad and the Arduino kits to build circuits. Below is a photo of a traffic light model we built, along with a section of the code used for it.

![Arduino Circuit](IMG_5886.PNG)
*Fig. 3* - Traffic light

This photo shows the traffic light circuit, one of the first circuits we built to learn about the use of arduino.

```.c
void red()
{
  digitalWrite(13, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(13, LOW);
}
```
*Fig. 4* - Traffic light code

The code shown in Fig. 4 demonstrates how to control LEDs in arduino.

![Button](button_circuit.png)
*Fig. 5* - Button circuit

This shows a circuit created to use a button, a component of the arduino essential for our solution


*Fig. 6* - LCD Circuit

This shows the standard LCD circuit provided by arduino, which we replicated in real life and added two buttons to.

```
String keyboard[3][13]{
  {"e", "a", "r", "i", "o", "t", "n", "s", "l", "c", "u", "d", "p"};
  {"m", "h", "g", "b", "f", "y", "w", "k", "v", "x", "z", "j", "q"};
  {" ", "SEND", "DEL", "0", "1", "2", "3", "4", "5", "6", "7", "8", "9"};
}


void setup()
{
  Serial.begin(9600);
  attachInterrupt(0, buttonA, RISING);//button A in port 2
  attachInterrupt(1, buttonB, RISING);//button B in port 3
}
```

*Fig. 7* - English input system

This segment of code shows two important skills developed in the first draft of the English Input System:
* Matrix use
* Interruptions

### Binary

![BNotes](Binary_notes.JPG)
*Fig. 7* - Binary notes

These notes show essential tables for binary and hexadeximal numbers, as well as briefly outlining the process for converting between the two, and from binary to decimal.

![BConversion](Binary_conversion.png)
*Fig. 8* - Binary conversion.

This table from [2](#references) shows the conversion process from decimal to binary.

### Boolean Operators

![Boolean Notes](IMG_6146.JPG)

*Fig. 9* - Boolean Notes

These notes show the process to create logic diagrams and equations with a set of conditions.

```.c
  digitalWrite(s, b | (a && ~b && c) | (~a && ~b && ~c) );
  digitalWrite(d, ~a | (a && b && c) | (~a && ~b && ~c) );
  digitalWrite(f, a | (~a && ~b && ~c) | (~a && c) );
  digitalWrite(g, (~a && ~b && ~c) | (~a && b && c) );
  digitalWrite(h, (~a && ~c) | (a && b && ~c) );
  digitalWrite(j, (a && ~b) | (a && ~c) | (~a && ~b && ~c) );
  digitalWrite(k, (~a && b) | (a && b && ~c) | (a && ~b) );
```
*Fig. 10* - Binary Counter Code

This is a portion of the code for an attempted binary counter. It shows the logic equations in action.

## References

(1) ISO. (n.d.). Usability of consumer products and products for public use. Retrieved from https://www.iso.org/obp/ui/#iso:std:iso:ts:20282:-2:ed-2:v1:en.
(2) Electronics Tutorials. (n.d.) Binary to Decimal and How to Convert Binary to Decimal. Retrieved from https://www.electronics-tutorials.ws/binary/bin_2.html

Evaluation
----
