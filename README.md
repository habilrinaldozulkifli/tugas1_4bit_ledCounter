// tugas1_4bit_ledCounter
int Reset = 7;

void setup()  
 {  
  pinMode(2,OUTPUT);   // declare LED pins as output pins  
  pinMode(3,OUTPUT);  
  pinMode(4,OUTPUT);  
  pinMode(5,OUTPUT);
  digitalWrite(Reset, HIGH);
  delay(1000);
  pinMode(Reset,OUTPUT);
  delay(1000);
 }  
 
 void loop()  
 {  
  for(int i=0;i<16;i++)  // increment automatically from 0 to 15 
  {  
   int a=i%2;      // calculate LSB   
   int b=i/2 %2;     
   int c=i/4 %2;        
   int d=i/8 %2;  //hitung MSB
   digitalWrite(5,a);   //write MSB
   digitalWrite(4,b);   
   digitalWrite(3,c);    
   digitalWrite(2,d);  // write LSB  
   delay(1000);     // wait for d second 

   digitalWrite(Reset, LOW);
  }  
 }  
