# HOME-AUTOMATION-WITH-BLUETOOTH

**company** = CODTECH IT SOLUTIONS

**NAME** = SAYALI SANTOSH NIRDHAR 

**INTERN ID** = CT08JED

**DOMAIN** = Embedded Systems 

**BATCH DURATION** = January 20th, 2025 to February 20th, 2025 

**MENTOR NAME** = Neela Santhosh 

#include <SoftwareSerial.h>

SoftwareSerial BT(10, 11);

const int relayPin = 8;  
char receivedChar;     

void setup() {
    pinMode(relayPin, OUTPUT);
    digitalWrite(relayPin, LOW);
    BT.begin(9600);  
    Serial.begin(9600); 
}
void loop() {
    if (BT.available()) {  
        receivedChar = BT.read(); 
        if (receivedChar == '1') {  
            digitalWrite(relayPin, HIGH);
            Serial.println("Device ON");
        } 
        else if (receivedChar == '0') {  
            digitalWrite(relayPin, LOW);
            Serial.println("Device OFF");
        }
    }
}

# output of task 2
![Image](https://github.com/user-attachments/assets/1c4a028a-a76f-4760-a97e-41e203df5444)

![Image](https://github.com/user-attachments/assets/2d36ed3e-7c8e-42ac-af1b-668c6d82bdb4)
