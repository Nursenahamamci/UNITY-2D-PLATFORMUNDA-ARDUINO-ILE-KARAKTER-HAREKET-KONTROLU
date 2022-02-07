# UNITY-2D-PLATFORMUNDA-ARDUINO-ILE-KARAKTER-HAREKET-KONTROLU


int gelenVeri = 0;    
char gelenKarakter;

void setup() {
   
 Serial.begin(9600);
 pinMode(2,OUTPUT);
 pinMode(3,OUTPUT);
 pinMode(4,OUTPUT);
 pinMode(5,OUTPUT);
}

void loop() {
  
 if (Serial.available() > 0) {
                // gelen veriyi oku
                gelenVeri = Serial.read();
                /*gelenKarakter = gelenVeri;
                Serial.print("Gelen Veri: ");
                Serial.println(gelenVeri);
                Serial.print("Gelen Karakter: ");
                Serial.println(gelenKarakter);*/
        }

if(gelenVeri==49){
  digitalWrite(2, HIGH);
  delay(1000); 
  digitalWrite(2, LOW);
  delay(1000); 
  }
  if(gelenVeri==50){
  digitalWrite(3, HIGH);
  delay(1000); 
  digitalWrite(3, LOW);
  delay(1000); 
  }
  if(gelenVeri==51){
  digitalWrite(4, HIGH);
  delay(1000); 
  digitalWrite(4, LOW);delay(1000); 
  }
  if(gelenVeri==52){
  digitalWrite(5, HIGH);
  delay(1000); 
  digitalWrite(5, LOW);delay(1000); 
  }
  gelenVeri=0;
}
