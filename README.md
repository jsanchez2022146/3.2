int POT1  = A0;
int POT2 = A1;
int POT3 = A2;
int Lectura1;
int Lectura2;
int Lectura3;
int LED1 = 3;
int LED2 = 5;
int LED3 = 6;

void setup()
{
  Serial.begin(9600);
 pinMode(POT1,INPUT);
   pinMode(LED1,OUTPUT);
   pinMode(POT2,INPUT);
   pinMode(LED2,OUTPUT);
   pinMode(POT3,INPUT);
   pinMode(LED3,OUTPUT);
}

void loop()
{

 Lectura1 = analogRead(POT1)/4;
  analogWrite(LED1,Lectura1);
  delay(100);
   Lectura2 = analogRead(POT2)/4;
  analogWrite(LED2,Lectura2);
  delay(100);
   Lectura3 = analogRead(POT3)/4;
  analogWrite(LED3,Lectura3);
  delay(200);
  Serial.print("codigo RGB R: ");
  Serial.print( Lectura1);
  Serial.print(" ");
  Serial.print("G:");
  Serial.print( Lectura2); 
  Serial.print(" ");
  Serial.print("B:");
  Serial.println( Lectura3);

    
}
