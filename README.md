# NotSoBasicArduino
 The follwing files are my second foray into Arduino
 
 
## Table of Contents
* [Table of Contents](#TableOfContents)
* [LED_Fade](#LED_Fade)
* [Hello_LCD](#Hello_LCD)
* [Finite LED Blinker](#FiniteLEDBlinker)
* [Arduino Review Assignment](#ArduinoReviewAssignment)
---

## LED_Fade

### Description & Code
Description goes here

Here's how you make code look like code:

```C++
// set the brightness of pin 9:
  analogWrite(led, brightness);

  // change the brightness for next time through the loop:
  brightness = brightness + fadeAmount;

  // reverse the direction of the fading at the ends of the fade:
  if (brightness <= 0 || brightness >= 255) {
    fadeAmount = -fadeAmount;
  }
```
Talk about how the fade works, here....

### Evidence
https://create.arduino.cc/editor/helmstk1/9e044cca-43d7-4d93-885f-e6dec5b4f769/preview

### Images

### Reflection

## Hello_LCD

### Description & Code
I had to make the light fade in and out.

Here's how you make code look like code:

```C++
/*
  Fading

  This example shows how to fade an LED using the analogWrite() function.

  The circuit:
  - LED attached from digital pin 9 to ground.

  created 1 Nov 2008
  by David A. Mellis
  modified 30 Aug 2011
  by Tom Igoe

  This example code is in the public domain.

  http://www.arduino.cc/en/Tutorial/Fading
*/

int ledPin = 9;    // LED connected to digital pin 9

void setup() {
  // nothing happens in setup
}

void loop() {
  // fade in from min to max in increments of 5 points:
  for (int fadeValue = 0 ; fadeValue <= 250; fadeValue += 5) {
    // sets the value (range from 0 to 255):
    analogWrite(ledPin, fadeValue);
    // wait for 30 milliseconds to see the dimming effect
    delay(30);
  }

  // fade out from max to min in increments of 5 points:
  for (int fadeValue = 20 ; fadeValue >= 0; fadeValue -= 5) {
    // sets the value (range from 0 to 255):
    analogWrite(ledPin, fadeValue);
    // wait for 30 milliseconds to see the dimming effect
    delay(30);
  }
}

```

I set a fade value, from 0-255. 
### Evidence
https://create.arduino.cc/editor/amedina41/f430cc75-e136-444a-8cb1-7bec78b6772d

### Images
<img src="https://github.com/AnthonyMedina3654/NotSoBasicArduino-1/blob/main/LEDFade.jpg?raw=true" alt="The Fade" width="400">

### Reflection
I had to ask a for a lot of help, but I know it will be worth it. 
## Finite LED Blinker

### Description & Code
I made a light blink 5 times with a variable. 

Here's how you make code look like code:

```C++
/*
  Blink

  Turns an LED on for one second, then off for one second, repeatedly.

  Most Arduinos have an on-board LED you can control. On the UNO, MEGA and ZERO
  it is attached to digital pin 13, on MKR1000 on pin 6. LED_BUILTIN is set to
  the correct LED pin independent of which board is used.
  If you want to know what pin the on-board LED is connected to on your Arduino
  model, check the Technical Specs of your board at:
  https://www.arduino.cc/en/Main/Products

  modified 8 May 2014
  by Scott Fitzgerald
  modified 2 Sep 2016
  by Arturo Guadalupi
  modified 8 Sep 2016
  by Colby Newman

  This example code is in the public domain.

  http://www.arduino.cc/en/Tutorial/Blink
*/
int counter = 0;
int LEDpin=9;
// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LEDpin, OUTPUT);
  Serial.begin(9600);
}

// the loop function runs over and over again forever
void loop() {
  counter = counter + 1;
  Serial.print(counter);
  if (counter < 6) {
    digitalWrite(LEDpin, HIGH);   // turn the LED on (HIGH is the voltage level)
    delay(250);                       // wait for a second
    digitalWrite(LEDpin, LOW);    // turn the LED off by making the voltage LOW
    delay(250);     // wait for a second
  }
  else {
    counter = 6;
    Serial.print("\t");
    Serial.println(counter);
  }
  delay(1000);
}

```
it has a variable that keeps it from going over 5 blinks

### Evidence
https://create.arduino.cc/editor/amedina41/ce10dc33-bd60-4cbe-857a-7e5be1e36fbf

### Images
<img src="https://github.com/AnthonyMedina3654/NotSoBasicArduino-1/blob/main/LEDFiniteBlink.jpg?raw=true" alt="The Finite Blink" width="400">

### Reflection
I had to ask for alot of help to complete this, but it will definintly help me in the long run

## Arduino Review Assignment

### Description & Code
I have not finished this, I dont know what to put here.

Here's how you make code look like code:

```C++
Code goes here
```
Talk about how the code works, here....

### Evidence
link goes here

### Images
draw it yourself, take a picture, make a fritzing, whatever you want to EFFECTIVELY communicate how its put together.

### Reflection
