# Smart-chair-locator
"Smart Chair Locator" enhances seating in crowded venues with rapid localization, comfort, and tourist satisfaction. Hardware: Arduino, sensors, LED. Guides visitors to seats. Contribute to open-source project. Join us!
The "Smart Chair Locator" project is a cutting-edge electronic system developed to elevate the seating experience, particularly in crowded venues like stadiums, auditoriums, and other public spaces. Our innovative project aims to offer tourists and visitors an efficient solution to effortlessly locate and occupy available seats.

Project Context:
Picture yourself entering a bustling stadium or any expansive public area. You're a tourist or an event enthusiast seeking a comfortable spot to sit. The "Smart Chair Locator" simplifies this process by leveraging a network of sensors and Arduino-based electronics to detect and identify the nearest available chairs tailored to your specific preferences.

Key Features:

Chair Availability Detection: Our system employs advanced electronic sensors to meticulously scan the environment for available chairs.
User-Centric Seating: It prioritizes and recommends seats based on user preferences, whether it's proximity, comfort, or other personalized criteria.
Arduino-Powered: The project harnesses the power of Arduino microcontrollers to proficiently manage sensor data and provide real-time recommendations.
How It Works:
Upon stepping into the venue, our system's sensors go into action, actively scanning for vacant chairs. Utilizing an Arduino-based system, our software processes this data and generates real-time recommendations for the user. Users can then make an informed choice on their preferred chair based on the insights provided.

Running the C Code:
To experience the full functionality of our "Smart Chair Locator" project, we encourage you to run the C code, which serves as the backbone of the system. This code is designed to ensure the seamless operation of our electronic sensors and real-time recommendation algorithms.

Why "Smart Chair Locator"?
Our project effectively addresses a prevalent challenge in crowded public spaces, ensuring a smooth and comfortable experience for all visitors. It ingeniously combines a synergy of hardware and software components to provide data-driven chair recommendations.

Get Involved:
If this project sparks your interest or if you have valuable ideas for enhancements, we cordially invite you to explore our comprehensive code and documentation. We wholeheartedly embrace collaboration and contributions from the dynamic open-source community.

Technologies Used:

C Programming
Arduino Development
Electronic Sensors
Data Analysis and Recommendation Algorithms
Join us on this exciting journey to simplify the seating experience for tourists and event attendees. Together, we can transform public spaces into more accessible and enjoyable environments. Don't forget to explore the detaile()
d code for Arduino and its accompanying explanatory presentation.(https://github.com/hanelo/Smart-chair-locator/files/13260775/Smart.Luggage.System.8.pdf)


int dsiege1=2;
int dsiege2=3;
int p1=8;
int p2=9;
int valeurseuil=400;
void setup() {
pinMode(siege1,INPUT);
pinMode (siege2,INPUT);

pinMode(siege1,INPUT);
pinMode (siege2,INPUT);
pinMode (p1,OUTPUT);
pinMode (p2,OUTPUT);
Serial.begin(9600);}
void loop() {
//  
Serial.print(analogRead(siege1));
Serial.print("\t");
Serial.println(analogRead(siege2));
Serial.print(digitalRead(dsiege1));
   digitalWrite(p1,LOW);
    digitalWrite(p2,LOW);
if(!digitalRead(dsiege1)&&analogRead(siege1)>valeurseuil){
  digitalWrite(p1,HIGH);
    digitalWrite(p2,LOW);
  }
 if(!digitalRead(dsiege2)&&analogRead(siege2)>valeurseuil){
  digitalWrite(p2,HIGH);
  digitalWrite(p1,LOW);
  }
   
   
  if(!digitalRead(dsiege1)&&analogRead(siege1)<valeurseuil &&analogRead(siege2)>valeurseuil ){
  digitalWrite(p2,HIGH);
  digitalWrite(p1,LOW);
  }
 if(!digitalRead(dsiege2)&&analogRead(siege2)<valeurseuil &&analogRead(siege1)>valeurseuil ){
  digitalWrite(p1,HIGH);
  digitalWrite(p2,LOW);
  }
}
ing ProgramC.ino…]()
