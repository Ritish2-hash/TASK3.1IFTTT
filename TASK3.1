#include "thingProperties.h"

const int ledPin = LED_BUILTIN;

const int dotDuration = 200;
const int dashDuration = 3 * dotDuration;
const int elementSpace = dotDuration;
const int letterSpace = 3 * dotDuration;

void setup() {
  Serial.begin(9600);
  pinMode(2,INPUT_PULLUP);
  pinMode(ledPin, OUTPUT);

  delay(1800);

  initProperties();

  ArduinoCloud.begin(ArduinoIoTPreferredConnection);
  
  setDebugMessageLevel(2);
  ArduinoCloud.printDebugInfo();
}

void loop() {
  ArduinoCloud.update();

  int Switchpin = digitalRead(2);
  Serial.print("LED Value: ");
  Serial.println(led);

  if (!Switchpin) {
    blinkR();
    blinkI();
    blinkT();
    blinkI();
    blinkS();
    blinkH();
  }
}

void onLedChange() {
  Serial.println("LED state changed from IoT Cloud");
}

void blinkDot() {
  digitalWrite(ledPin, HIGH);
  delay(dotDuration);
  digitalWrite(ledPin, LOW);
  delay(elementSpace);
}

void blinkDash() {
  digitalWrite(ledPin, HIGH);
  delay(dashDuration);
  digitalWrite(ledPin, LOW);
  delay(elementSpace);
}

void blinkR() {
  blinkDot();
  blinkDash();
  delay(letterSpace);
}

void blinkI() {
  blinkDash();
  blinkDot();
  blinkDash();
  delay(letterSpace);
}

void blinkT() {
  blinkDot();
  blinkDot();
  blinkDot();
  delay(letterSpace);
}

void blinkI() {
  blinkDot();
  blinkDot();
  blinkDot();
  blinkDot();
  delay(letterSpace);
}

void blinkS() {
  blinkDot();
  blinkDot();
  delay(letterSpace);
}

void blinkH() {
  blinkDash();
  delay(letterSpace);
}
