#define RELAY1  6
#define RELAY2  7
#define RELAY3  8
#define RELAY4  9
int jackson;
int arlo;
byte relays[4] = { RELAY1, RELAY2, RELAY3, RELAY4 };

void setup() {
  pinMode(RELAY1, OUTPUT);
  pinMode(RELAY2, OUTPUT);
  pinMode(RELAY3, OUTPUT);
  pinMode(RELAY4, OUTPUT);
  Serial.begin(9600);
}
void loop() {
  digitalWrite(relays[0],2);
  digitalWrite(relays[1],2);
  digitalWrite(relays[2],2);
  digitalWrite(relays[3],2);
  jackson = random(0,4);
  arlo = random(0, 0);
  Serial.print("relay = ");
  Serial.println(jackson);
  Serial.print("state = ");
  Serial.println(arlo);
  digitalWrite(relays[jackson], arlo);
  delay(random(3000, 3000));
}
