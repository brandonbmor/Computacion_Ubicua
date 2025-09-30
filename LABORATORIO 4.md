 # LABORATORIO 4 #
 <img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/354ae631-ca34-4d8f-a7f2-663a5226a6bc" />

 ```

int SENSOR;
float TEMPERATURA;
float SUMA;

void setup() {
  Serial.begin(9600);
}

void loop() {
  SUMA = 0;
  for (int i = 0; i < 5; i++) {
    SENSOR = analogRead(A0);
    TEMPERATURA = ((SENSOR * 5000.0) / 1023) / 10;
    SUMA = TEMPERATURA + SUMA;
    delay(500);
  }
  
  Serial.println(SUMA/5.0, 1);
}
```
