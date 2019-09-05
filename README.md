 int sensorPin0 = A0;
const int ProxSensor=2;
 

int sensorVal0 = 0; 
int inputVal1 = 0;
void setup() 
{
  pinMode(13, OUTPUT);            
  pinMode(ProxSensor,INPUT);  
  Serial.begin(9600); 
}
void loop() 
{
sensorVal0 = analogRead(sensorPin0);
Serial.print("LDR = ");
Serial.print(sensorVal0); 

delay(1000);

if(digitalRead(ProxSensor)==HIGH)      
  {
    digitalWrite(13, HIGH);   
  }
  else
  {
    digitalWrite(13, LOW);  
  }
inputVal1 = digitalRead(ProxSensor);
Serial.print("  Infrared = ");
Serial.println(inputVal1);

delay(1000);

}
