# Código do Arduino/ESP
#include <Wire.h>
#include <LiquidCrystal_I2C.h>
//biblioteca, baixada extraida na pasta documentos arduino https://github.com/johnrickman/LiquidCrystal_I2C/releases/tag/1.1.3 (quando extrair tem que tirar - 1.1.3 do nome da blibloteca para funcionar

// Configuração do LCD I2C (endereço comum: 0x27, 16 colunas, 2 linhas)
LiquidCrystal_I2C lcd(0x27, 16, 2);

const int led1 = 13;
const int led2 = 12;
const int led3 = 14;
const int led4 = 27;

const int trig1 = 26;
const int trig2 = 33;
const int trig3 = 35;
const int trig4 = 23;

const int echo1 = 25;
const int echo2 = 32;
const int echo3 = 34;
const int echo4 = 22;

const float distanciaLimite = 50.0;

void setup() {
  Serial.begin(115200);

  Wire.begin(21, 5);       // SDA 21 SCL 5
  lcd.init();        
  lcd.backlight();        


  pinMode(led1, OUTPUT); digitalWrite(led1, LOW);
  pinMode(trig1, OUTPUT); pinMode(echo1, INPUT);

  pinMode(led2, OUTPUT); digitalWrite(led2, LOW);
  pinMode(trig2, OUTPUT); pinMode(echo2, INPUT);

  pinMode(led3, OUTPUT); digitalWrite(led3, LOW);
  pinMode(trig3, OUTPUT); pinMode(echo3, INPUT);

  pinMode(led4, OUTPUT); digitalWrite(led4, LOW);
  pinMode(trig4, OUTPUT); pinMode(echo4, INPUT);
}

float medirDistancia(int trigPin, int echoPin) {
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);

//calculo da distancia 
  long duracao = pulseIn(echoPin, HIGH, 30000);
  if (duracao == 0) return -1.0;
  float distancia = duracao * 0.034 / 2;
  return distancia;
}

void loop() {
  int sensoresAtivados = 0;
  int sensoresDesativados = 0;

// Se for identificado alguma coisa no raio do ultrassonico o led é acendido
  float distancia1 = medirDistancia(trig1, echo1);
  if (distancia1 > 0 && distancia1 < distanciaLimite) {
    digitalWrite(led1, HIGH);
    sensoresAtivados++;
  } else {
    digitalWrite(led1, LOW);
    sensoresDesativados++;
  }
// Se for identificado alguma coisa no raio do ultrassonico o led é acendido
  float distancia2 = medirDistancia(trig2, echo2);
  if (distancia2 > 0 && distancia2 < distanciaLimite) {
    digitalWrite(led2, HIGH);
    sensoresAtivados++;
  } else {
    digitalWrite(led2, LOW);
    sensoresDesativados++;
  }
// Se for identificado alguma coisa no raio do ultrassonico o led é acendido
  float distancia3 = medirDistancia(trig3, echo3);
  if (distancia3 > 0 && distancia3 < distanciaLimite) {
    digitalWrite(led3, HIGH);
    sensoresAtivados++;
  } else {
    digitalWrite(led3, LOW);
    sensoresDesativados++;
  }
// Se for identificado alguma coisa no raio do ultrassonico o led é acendido
  float distancia4 = medirDistancia(trig4, echo4);
  if (distancia4 > 0 && distancia4 < distanciaLimite) {
    digitalWrite(led4, HIGH);
    sensoresAtivados++;
  } else {
    digitalWrite(led4, LOW);
    sensoresDesativados++;
  }

  
  Serial.print("Total Livres: ");
  Serial.println(sensoresDesativados);
  Serial.print("Total Ocupados: ");
  Serial.println(sensoresAtivados);
  Serial.println("------------------------");

  // Display mostrando vagas livres e vagas ocupadas
  lcd.clear();
  lcd.setCursor(0, 0);
  lcd.print("Livres: ");
  lcd.print(sensoresDesativados);
  lcd.setCursor(0, 1);
  lcd.print("Ocupadas: ");
  lcd.print(sensoresAtivados);

  delay(2000);
}
