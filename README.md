# Meroitic-reference-3LED
// كود تشغيل إشارة مرور بسيطة باستخدام Arduino

int redLed = 8;     // لمبة حمراء
int yellowLed = 9;  // لمبة صفراء
int greenLed = 10;  // لمبة خضراء

void setup() {
  // تعريف الأرجل كمخارج
  pinMode(redLed, OUTPUT);
  pinMode(yellowLed, OUTPUT);
  pinMode(greenLed, OUTPUT);
}

void loop() {
  // 1- تشغيل الأحمر
  digitalWrite(redLed, HIGH);
  delay(5000); // 5 ثواني
  digitalWrite(redLed, LOW);

  // 2- تشغيل الأخضر
  digitalWrite(greenLed, HIGH);
  delay(5000); // 5 ثواني
  digitalWrite(greenLed, LOW);

  // 3- تشغيل الأصفر (تنبيه للتبديل)
  digitalWrite(yellowLed, HIGH);
  delay(2000); // ثانيتين
  digitalWrite(yellowLed, LOW);
}
