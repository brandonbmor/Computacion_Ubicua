# LABORATORIO 1 #
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/7b35d68d-b300-446d-94e4-ec2e64ca6340" />



void setup() {


  pinMode(2, INPUT); 
  pinMode(3, OUTPUT); 

}


void loop(){
  if (digitalRead(2) == HIGH){  
    digitalWrite(3, HIGH);    
  }
  else {
    digitalWrite(3, LOW); 
  }
}










