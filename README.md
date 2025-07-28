# Smart-Irrigation-System
###### This Smart Irrigation System, built using Tinkercad and Arduino UNO, automates plant watering by monitoring soil moisture and controlling a sprinkler with real-time LCD feedback.
---
## Here is the references...

Circuit Connections in TINKERCAD :-

<img src=https://github.com/lingeshkumarkamaraj/Smart-Irrigation-System/blob/main/1.png> 
<img src=https://github.com/lingeshkumarkamaraj/Smart-Irrigation-System/blob/main/2.png> 

Working :- 

[<img width="300" height="300" src="https://img.icons8.com/color/96/start.png" alt="video"/>](https://youtu.be/FChY_B5z7uw)


---
Code :-
```

#include<LiquidCrystal.h>
LiquidCrystal lcd(7,6,2,3,4,5);

void setup()
{
  lcd.begin(16,2);
  pinMode(A3, INPUT);
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(11, OUTPUT);
}

void loop()
{
  int a;
  a = analogRead(A3);
  if(a<700)
  {
    lcd.setCursor(0,0);
    lcd.print(" ");
    lcd.print("Soil is Wet");
    lcd.setCursor(0,1);
    lcd.print(" ");
    lcd.print("Sprinkler OFF");
    digitalWrite(13,LOW);
    digitalWrite(12,LOW);    
    digitalWrite(11,LOW);
    lcd.print(" ");
  }
  else
  {
    lcd.setCursor(0,0);
    lcd.print(" ");
    lcd.print("Soil is dry");
    lcd.setCursor(0,1);
    lcd.print(" ");
    lcd.print("Sprinkler ON");
    digitalWrite(13,HIGH);
    digitalWrite(12,HIGH);
    digitalWrite(11,HIGH);
    lcd.print(" ");
  }
}

```
---
[TINKERCAD LINK](https://www.tinkercad.com/things/99NJweZUUkV-tremendous-snicket)
---
