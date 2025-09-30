# LABORATORIO 5 #
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/6a7be99d-dd1f-48c4-a158-ba8d1d0d2100" />

  
  
  ```
#include <DHT.h>
#include <DHT_U.h>

int SENSOR = 2;
int TEMPERATURA;
int HUMEDAD;   

DHT dht(SENSOR, DHT22);

void setup(){
  Serial.begin(9600);
  dht.begin();
}

void loop(){
  float TEMPERATURA = dht.readTemperature();
  float HUMEDAD = dht.readHumidity();

  Serial.print("Temperatura: ");
  Serial.print(TEMPERATURA);
  Serial.print("  Humedad: ");
  Serial.println(HUMEDAD);

  delay(500);
}
 ```
