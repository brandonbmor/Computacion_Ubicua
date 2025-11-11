# LABORATORIO 7 #
<img src="https://github.com/user-attachments/assets/89031310-d4bc-4a4c-a1c3-c486f06364bd" width="500" height="500"> 

```
int TRIG = 10;
int ECO = 9;
int LED = 3;
int DURACION; 
int DISTANCIA;

void setup(){
  pinMode(TRIG, OUTPUT);
  pinMode(ECO, INPUT);
  pinMode(LED, OUTPUT);
  Serial.begin(9600);
}

void loop(){
  digitalWrite(TRIG, HIGH);
  delay(1);
  digitalWrite(TRIG, LOW);

  DURACION = pulseIn(ECO, HIGH);
  DISTANCIA = DURACION / 58.2;

  Serial.println(DISTANCIA);
  delay(200);

  if(DISTANCIA <= 20 && DISTANCIA >= 0){
    digitalWrite(LED, HIGH);
    delay(DISTANCIA*10);  
    digitalWrite(LED, LOW);
  }
}
```

