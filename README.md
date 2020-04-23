# Arduino-1
Simple LED program in Arduino
#include<LiquidCrystal.h>
LiquidCrystal LCD(12,11,5,4,3,2);
void setup() {
  // put your setup code here, to run once:
  LCD.begin(16,2);
  pinMode(7,OUTPUT);
}

void loop() {
  // put your main code here, to run repeatedly:
  for(int i=0;i<10;i++)
  {
    digitalWrite(7,HIGH);
    LCD.setCursor(1,0);
    LCD.print(i+1);
    LCD.setCursor(5,0);
    LCD.print("LED IS ON");
    delay(2000);
    LCD.clear();
    delay(1000);
    digitalWrite(7,LOW);
    LCD.setCursor(5,0);
    LCD.print("LED IS OFF");
    delay(2000);
    LCD.clear();
    delay(1000);
  }
}
