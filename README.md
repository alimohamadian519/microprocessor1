# راه اندازی LED چشمک زن با استفاده از آردوینو
## گزارش کار 

برد آردوینو UNO رو آماده کرده و به کامپیوتر وصل می‌کنیم. سپس یک برنامه برای چشمک زدن LED می‌نویسیم. برای این منظور، LED و مقاومت رو به بردبرد متصل می‌کنیم و پایه منفی LED رو به GND آردوینو و پایه مثبت رو به یکی از خروجی‌های دیجیتال (مثلاً پایه 8) وصل می‌کنیم. در نهایت، آردوینو رو با کابل USB به کامپیوتر وصل کرده 

---

### کد برنامه :
این کد یک LED رو به‌صورت متناوب روشن و خاموش می‌کنه. 

1. در خط اول، متغیر led تعریف می‌شه که شماره پایه LED رو مشخص می‌کنه (پایه ۸).
2. در فانکشن setup، پایه LED به عنوان خروجی تنظیم می‌شه.
3. فانکشن loop که مدام تکرار می‌شه، اول پایه LED رو روشن می‌کنه (ولتاژ ۵ ولت)، بعد از یک ثانیه (۱۰۰۰ میلی‌ثانیه) خاموشش می‌کنه (ولتاژ صفر). این فرایند همواره تکرار می‌شه.

اینجوری LED هر ثانیه روشن و خاموش می‌شه.

```cpp
int led = 8;   

void setup() {  
  pinMode(led, OUTPUT); 
}

void loop() {   
  digitalWrite(led,HIGH);   
  delay(1000);  
  digitalWrite(led ,LOW);   
  delay(1000);
}
---

### عکس مدار 

![micro and circuit](/images/microprocessor_1.jpg)
