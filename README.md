پروژه ساخت ماشین حساب ساده
float num1 , num2;
char x;
void setup() {
  // put your setup code here, to run once:
Serial.begin(9600);
}

void loop() {
  // put your main code here, to run repeatedly:
if(Serial.available() > 0){
  num1 = Serial.parseFloat();
  x = Serial.read();
  num2 = Serial.parseFloat();
  Serial.print(num1);
  Serial.print(x);
  Serial.print(num2);
  Serial.print('=');
  switch(x)
  {
    case '+' : Serial.println(num1 + num2);break;
    case '-' : Serial.println(num1 - num2);break;
    case '*' : Serial.println(num1 * num2);break;
    case '/' :
    if(num2 == 0){
      Serial.println("Error");}
      else (Serial.println(num1 / num2));break;
  }
}
}
در این پروژه میتوانم چهار عملیات جمع ، منها ، ضرب و تقسیم را بر روی دو عدد ورودی دلخواه به انتخواب خود انجام دهیم
این اعداد میتوانند عشاری نیز باشند
اگر عدد ورودی دوم صفر باشد در تقسیم به ارور بر میخوریم
