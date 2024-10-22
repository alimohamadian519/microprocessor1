# راه اندازی LED چشمک زن با استفاده از آردوینو 
## گزارش کار 

راه اندازی اولیه برد آردوینو UNO به کامپیوتروصل میکنیم و برنامه LED  اجرا میکنیم که حالت چشمک زن بدهد.  
اول LED و مقاومت را به برد وصل و بعد با استفاده از سیم های جامپر پایه منفی LED را به خروجی GND آردوینو و پایه مثبت را به یکی از خروجی های دیجیتال آردوینو وصل می کنیم. برد آردوینو را به کامپیوتر وصل میکنیم.

---

### کد برنامه 

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
```

---

### عکس مدار 

![micro and circuit](/images/microprocessor_1.jpg)
