Code Practice
---

## For loops

### Greetings loop
```.c
void setup()
{
	Serial.begin(9600);
}

void loop() {
  for (int i = 0; i<1000; i++) {
 	Serial.print("\n Hello!");
  	delay(1000);
  }
}
```

### Year loop
```.c
void setup()
{
	Serial.begin(9600);
}

void loop()
{
  for (int i = 1000; i < 2019; i++ ) {
  		Serial.print("\n Year ");
  		Serial.print(i);
  }
}
```

### Addition loop
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

### Odd loop
```.c
void setup()
{
  Serial.begin(9600);
}

void loop()
{
  for (int i = 1002; i > 0; i--){
    if (i % 2 != 0){
      Serial.print("\n");
      Serial.print(i);
    }
  }
}
```

### Sequence loop
```.c
void setup()
{
  Serial.begin(9600);
  int n = -1;
  for (int i = 0; i < 1000; i++){
    n = n + 1;
    if (n == 7){
      n = 0;
    }
  Serial.print(n);
  }
}

void loop()
{
  
}
```

### Factors of Seven loop
```.c
void setup()
{
  Serial.begin(9600);
  for ( int i = 1; i < 101; i++ ){
    int factor = i * 7;
  	Serial.print(factor);
    Serial.print("\n");
  }
}

void loop()
{
}
```

### Ordinal loop
```.c
void setup()
{
  Serial.begin(9600);
  for (int i = 0; i < 100; i++){
    if (i % 10 == 1 && i != 11){
      Serial.print(i);
      Serial.print("st");
      Serial.print("\n");
    }
    else if (i % 10 == 2 && i != 12){
      Serial.print(i);
      Serial.print("nd");
      Serial.print("\n");
    }
    else if (i % 10 == 3 && i != 13){
      Serial.print(i);
      Serial.print("rd");
      Serial.print("\n");
    }
    else {
      Serial.print(i);
      Serial.print("th");
      Serial.print("\n");
    }
  }
}
  
void loop()
{
}
```

### Four Letters loop
```.c
void setup()
{
  Serial.begin(9600);
  for (int i = 0; i < 100; i++){
    int prime = 1;
    for (int n = 2; n < i; n++){
      int remainder = i % n;
      if (remainder == 0){
        prime=0;
        break;
      }
    }
  	if (prime == 1){
    	Serial.print(i);
      	Serial.print("\n");
	}
  }
}

void loop()
{
}
```

### Random Letter loop
```.c
void setup()
{
  Serial.begin(9600);
  long num;
  char letters[] = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
  for (int i = 0; i < 100; i++){
    num = random(26);
    Serial.print(letters[num]);
    Serial.print("\n");
  }
}

void loop()
{
}
```

## Circuit Practice

### Traffic Light
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

### Binary Counter
```.c
int five = 13;
int four = 12;
int three = 11;
int two = 10;
int one = 9;

void setup(){
  pinMode(five, OUTPUT);
  pinMode(four, OUTPUT);
  pinMode(three, OUTPUT);
  pinMode(two, OUTPUT);
  pinMode(one, OUTPUT);
  Serial.begin(9600);
}

void loop(){
  for (unsigned char i = 0; i < 32; i++){
    lights(i);
  }
}

void on(int port){
  digitalWrite(port, HIGH);
}

void off(int port){
  digitalWrite(port, LOW);
}

void lights(unsigned char n){
  if (n % 2 != 0){
    on(one);
  }
  else {
    off(one);
  }
  if (n % 4 > 1){
    on(two);
  }
  else {
    off(two);
  }
  if (n % 8 > 3){
    on(three);
  }
  else {
    off(three);
  }
  if (n % 16 > 5){
    on(four);
  }
  else {
    off(four);
  }
  if (n % 32 > 15){
    on(five);
  }
  else {
    off(five);
  }
  delay(1000);
}
```

## Button Practice

### Table 1
```.c
int butA = 13;
int butB = 12;
int led1 = 3;
int led2 = 4;
int a = 0;
int b = 0;
bool statusA = false;
bool statusB = false;

void setup()
{
  pinMode(butA, OUTPUT);
  pinMode(butB, OUTPUT);
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
}

void loop()
{
  if(digitalRead(butA) == HIGH){
    a = a++;
  }
  if(digitalRead(butB) == HIGH){
    b = b++;
  }
  if(a % 2 == 1){
    statusA = true;
  }
  else{
    statusA = false;
  }
  if(b % 2 == 1){
    statusB = true;
  }
  else{
    statusB = false;
  }
  if(statusA == false && statusB == false){
    digitalWrite(led1, LOW);
    digitalWrite(led2, HIGH);
  }
  if(statusA == false && statusB == true){
    digitalWrite(led1, HIGH);
    digitalWrite(led2, LOW);
  }
  if(statusA == true && statusB == false){
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
  }
  if(statusA == true && statusB == true){
    digitalWrite(led1, LOW);
    digitalWrite(led2, LOW);
  }
}
```

### Table 2
```.c
int butA = 13;
int butB = 12;
int led1 = 3;
int led2 = 4;

void setup()
{
  pinMode(butA, OUTPUT);
  pinMode(butB, OUTPUT);
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
}

void loop()
{
  if(digitalRead(butA) == LOW && digitalRead(butB) == LOW){
    digitalWrite(led1, HIGH);
    digitalWrite(led2, LOW);
  }
  if(digitalRead(butA) == LOW && digitalRead(butB) == HIGH){
    digitalWrite(led1, LOW);
    digitalWrite(led2, HIGH);
  }
  if(digitalRead(butA) == HIGH && digitalRead(butB) == LOW){
    digitalWrite(led1, LOW);
    digitalWrite(led2, HIGH);
  }
  if(digitalRead(butA) == HIGH && digitalRead(butB) == HIGH){
    digitalWrite(led1, HIGH);
    digitalWrite(led2, HIGH);
  }
}
```

### Table 3
```.
int butA = 13;
int butB = 12;
int butC = 11;
int led1 = 3;
int led2 = 4;

void setup()
{
  pinMode(butA, OUTPUT);
  pinMode(butB, OUTPUT);
  pinMode(butC, OUTPUT);
  pinMode(led1, OUTPUT);
  pinMode(led2, OUTPUT);
}

void loop()
{
  bool a = digitalRead(butA);
  bool b = digitalRead(butB);
  bool c = digitalRead(butC);
  digitalWrite(led1, ~a | (a & b) | (a & ~b & c));
  digitalWrite(led2, a | (~a & ~b));
}
```

## LED Number Display
```.c

```
