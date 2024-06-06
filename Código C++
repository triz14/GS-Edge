// Inclusão das bibliotecas
#include <Adafruit_LiquidCrystal.h>

// Declaração do lcd
Adafruit_LiquidCrystal lcd(0);

// Declaração dos leds
int led_verm = 4;
int led_verde = 5;
int led_turb = 6;

// Declaração ph
int ph;

// Declaração sensor ultrassonico
int trigger = 8;
int echo = 7;

// Declaração centimetros
int cm = 0;

void setup(){
  // Iniciação do lcd
  lcd.begin(16,2);
  lcd.setBacklight(1);

  // Leds configurados como saída de informação
  pinMode(led_verm, OUTPUT);
  pinMode(led_verde, OUTPUT);
  pinMode(led_turb, OUTPUT); 
  
  // Sensor ultrassonico
  pinMode(trigger, OUTPUT);
  pinMode(echo, INPUT);
}

// Função ph
void val_ph(){
  // Declaração sensor ph
  int sensor_ph = analogRead (A0); 
  
  // Dividimos o valor lido pelo pot que é 1023 
  // por 14 (valores do ph)
  ph = (14 * sensor_ph / 1023);
  
  // Ph baixo
  if (ph < 7){
    digitalWrite(led_verm, HIGH);
    digitalWrite(led_verde, LOW);
    lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("PH ");
    lcd.print("Baixo");
    lcd.setCursor(0, 1);
    lcd.print("PH = ");
    lcd.print(ph);
    delay(500); 
  }
  // Ph ideal
  else if(ph >= 7 && ph <= 8.5){
    digitalWrite(led_verde, HIGH);
    digitalWrite(led_verm, LOW);
    lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("PH ");
    lcd.print("Ideal");
    lcd.setCursor(0, 1);
    lcd.print("PH = ");
    lcd.print(ph);
    delay(500);
  }
  // Ph alto
  else{
  	digitalWrite(led_verm, HIGH);
    digitalWrite(led_verde, LOW);
    lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("PH ");
    lcd.print("Alto");
    lcd.setCursor(0, 1);
    lcd.print("PH = ");
    lcd.print(ph);
    delay(500);
  }
  delay(2000);
}

// Função temperatura
void temp(){
  // Faz a leitura da tensao no Sensor de Temperatura
  int sensor_temp = analogRead(A1);
  
  // Converte a tensao lida
  float tensao = sensor_temp*5;
  tensao/=1024;

  // Converte a tensao lida em Graus Celsius
  float temp_c = (tensao-0.5)*100;
  
  //Temp baixa
  if(temp_c < 24){
  	lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("Temp. ");
    lcd.print("Baixa");
    lcd.setCursor(0, 1);
    lcd.print("Temp = ");
    lcd.print(temp_c);
    delay(500);
  }
  //Temp ideal
  else if(temp_c >= 24 && temp_c <= 27){
  	lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("Temp. ");
    lcd.print("Ideal");
    lcd.setCursor(0, 1);
    lcd.print("Temp = ");
    lcd.print(temp_c);
    delay(500);
  }
  //Temp Alta
  else{
  	lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("Temp. ");
    lcd.print("Alta");
    lcd.setCursor(0, 1);
    lcd.print("Temp = ");
    lcd.print(temp_c);
    delay(500);
  }
  delay(2000);
}

void turb(){
  // Declaração ldr
  int ldr = analogRead(A2);
  
  // Turbidez muito alta
  if(ldr <= 200){
  	lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("Turb ");
    lcd.print("Muito alta");
    lcd.setCursor(0, 1);
    lcd.print("Turb = ");
    lcd.print(ldr);
    delay(500);
  }
  // Turbidez alta
  else if(ldr > 300 && ldr <= 400){
  	lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("Turb ");
    lcd.print("Alta");
    lcd.setCursor(0, 1);
    lcd.print("Turb = ");
    lcd.print(ldr);
    delay(500);
  }
  // Turbidez ideal
  else{
  	lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("Turbidez ");
    lcd.print("Ideal");
    lcd.setCursor(0, 1);
    lcd.print("Turb = ");
    lcd.print(ldr);
    delay(500);
  }
  delay(2000);
}

void sensor_mov(){
  // Iniciação sensor ultrassonico
  digitalWrite(trigger, LOW);
  delayMicroseconds(5);
  digitalWrite(trigger, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigger, LOW);
  
  // Cenimetros pega o valor que é lido pela echo
  cm = pulseIn(echo, HIGH);
  
  // Converte o valor lido em centimetros
  cm = cm/58;
  
  // Movimento detectado
  if(cm <= 100){
  	lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("Mov. ");
    lcd.print("Detectado");
    lcd.setCursor(0, 1);
    lcd.print("Dist = ");
    lcd.print(cm);
    delay(500);
  }
  // Nenhum movimento
  else{
  	lcd.clear();
    lcd.setCursor(0, 0);
    lcd.print("Nenhum ");
    lcd.print("Movimento");
    delay(500);
  }
  delay(2000);
}

void loop(){
  // Led turbidez
  digitalWrite(led_turb, HIGH);
  
  //Chamando as funções
  val_ph();
  temp();
  turb();
  sensor_mov();
  
}
