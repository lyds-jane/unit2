04/11/2019
----

### Outline of Unit
* Converting a phrase from English, to morse code, to English, to Binary, to English, using two buttons
* Relaying messages in morse code and binary using a lightbulb
* Language: Modern C
* Hardware: Arduino IDE

### What I'm looking forward to
* Learning a new programming language
* Using Arduino

### What I'm worried about
* Working in groups
* Using only two buttons to convert from morse code to English to binary

### Tasks/To do
* Traffic light project with tinkercad
* Finish syllabus reflection for Unit 1


10/11/2019
----

### Difference between Arduino and Bash programming
There are many differences between Arduino and Bash.

First, the overall syntax has different requirements. In Arduino, all code must take place within a function. When a line of code is not declaring or closing a function, the line of code must end with a semicolon. There are also different types of variables in arduino, such as int, char, long, and many more.

Furthermore, specific commands are different. For example, all of the commands start with "Serial". There is no "echo" command, instead we use "Serial.print()". This command is also excecuted very differently, as text and variables have to be printed seperately, and "\n" must be used to move an output to the next line. The eqality statement syntax is also different in arduino, using == for everything, instead of a combination of == and -eq.

Finally, small syntax specifics are different. For example, the use of spaces. What would be `( i=0; i<100; i++ )` in bash is `(int i = 0; i < 100; i++)` in arduino.

Ultimately, bash and arduino are very different programming languages, but they use the same logic, making it very easy to convert programs from one to another.

For this assignment, resouces in the Arduino Reference pages were used. Specifically:
* Increment
* &&
* break
* array
* random()
* for
* if
* else
* !=
* functions
