#include <LiquidCrystal.h>
int button=8;
int val;
int count=0;
int press; int Y;
const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);

void setup() {
  lcd.begin(16, 2);
  pinMode(button,INPUT);
}

void loop() {
  val=digitalRead(button);
  if(val==HIGH){
    press=count++;
    Y=1*press+1; //y=mx+b
    delay(250);
  }
 
  lcd.setCursor(0, 0);
  lcd.print("Clicks");
  lcd.setCursor(0, 1);
  lcd.print(Y);
  
 

     
   if (count == 10){
      lcd.clear();
      lcd.setCursor(2, 0);
      lcd.print("Cool");
      delay(10);
    }
     else if(count == 20){
      lcd.clear();
      lcd.setCursor(2, 0);
      lcd.print("Gud");
      delay(1000);
    }
     else if(count == 30){
      lcd.clear();
      lcd.setCursor(2, 0);
      lcd.print("WoW");
      delay(1000);
    }
     else if(count == 40){
      lcd.clear();
      lcd.setCursor(2, 0);
      lcd.print("yo!");
      delay(1000);
    }
     else if(count == 50){
      lcd.clear();
      lcd.setCursor(2, 0);
      lcd.print(":)");
      delay(1000); 
     }
}

<!--
**ianyhgg/ianyhgg** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
