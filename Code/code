#include <Servo.h>

const int servo1 = 3;       // s1
const int servo2 = 10;      // s2
const int servo3 = 5;       // s3
const int servo4 = 11;      // s4
const int joyH = 2;        
const int joyV = 3;        
const int joyX = 4;       
const int joyP = 5;       

int servoVal;           // variable to read analog

Servo myservo1;  // create object
Servo myservo2;  
Servo myservo3; 
Servo myservo4;  

void setup() {

   
  myservo1.attach(servo1);
  myservo2.attach(servo2);
  myservo3.attach(servo3);
  myservo4.attach(servo4);
  Serial.begin(9600);
}


void loop(){

    
    outputJoystick();

    // analog read settings
    servoVal = analogRead(joyH);         
    servoVal = map(servoVal, 0, 1023, 0, 180);     //0-180 degree

    myservo2.write(servoVal);                     
    servoVal = analogRead(joyV);          
    servoVal = map(servoVal, 0, 1023, 70, 180);    

    myservo1.write(servoVal);                           
    delay(15);                                      

    servoVal = analogRead(joyP);          
    servoVal = map(servoVal, 0, 1023, 70, 180);     
    myservo4.write(servoVal);                           

    delay(15);                                     
    servoVal = analogRead(joyX);          
    servoVal = map(servoVal, 0, 1023, 70, 180);    
    myservo3.write(servoVal);
    delay(15);                                       
}
