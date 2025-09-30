# LABORATORIO 2 #
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/374dbf5f-321c-4212-bcad-996ac14c6b1a" />


```
int LED = 3;        // LED en pin 3
int BRILLO;
int POT = 0;        // potenciometro en pin A0

void setup(){
  pinMode(LED, OUTPUT);   // pin 3 como salida
  // las entradas analogicas no requieren inicializacion
}

void loop(){
  BRILLO = analogRead(POT) / 4; // valor leido de entrada analogica divido por 4
  analogWrite(LED, BRILLO); // brillo del LED proporcional al giro del potenciometro
}
```

