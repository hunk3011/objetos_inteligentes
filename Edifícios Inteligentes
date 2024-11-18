#include <ESP8266WiFi.h>
#include <Adafruit_MQTT.h>
#include <Adafruit_MQTT_Client.h>

const int FIRE_SENSOR_PIN = D2;
const int LED_PIN = D7; // Define o pino da LED

const char* WIFI_SSID = "HUNK-2G";
const char* WIFI_PASS = "piauilino1958";

const char* AIO_SERVER = "io.adafruit.com";
const uint16_t AIO_SERVERPORT = 1883;
const char* AIO_USERNAME = "Maria99";
const char* AIO_KEY = "aio_LAAE79PIrCzxgA6zfz0lEw7n9xtJ";

WiFiClient wifiClient;
Adafruit_MQTT_Client mqttClient(&wifiClient, AIO_SERVER, AIO_SERVERPORT, AIO_USERNAME, AIO_KEY);

Adafruit_MQTT_Publish fireStatusFeed = Adafruit_MQTT_Publish(&mqttClient, "Maria99/feeds/firestatus");

unsigned long previousNormalPublish = 0;
unsigned long previousAlarmPublish = 0;
const unsigned long NORMAL_INTERVAL = 5000; 
const unsigned long ALARM_INTERVAL = 2000;  

void connectWiFi() {
  Serial.print("Conectando ao Wi-Fi...");
  WiFi.begin(WIFI_SSID, WIFI_PASS);
  while (WiFi.status() != WL_CONNECTED) {
    delay(500);
    Serial.print(".");
  }
  Serial.println("\nWi-Fi conectado!");
  Serial.print("Endereço IP: ");
  Serial.println(WiFi.localIP());
}

void connectMQTT() {
  while (!mqttClient.connected()) {
    Serial.println("Conectando ao MQTT...");
    int8_t ret = mqttClient.connect();
    if (ret == 0) {
      Serial.println("Conectado ao Adafruit IO!");
    } else {
      Serial.print("Falha ao conectar (erro: ");
      Serial.print(mqttClient.connectErrorString(ret));
      Serial.println("). Tentando novamente em 5 segundos...");
      delay(5000);
    }
  }
}

void checkFireSensor() {
  int fireStatus = digitalRead(FIRE_SENSOR_PIN);
  unsigned long currentMillis = millis();
  
  if (fireStatus == LOW && currentMillis - previousAlarmPublish >= ALARM_INTERVAL) {
    Serial.println("Incêndio Detectado!");
    fireStatusFeed.publish("Incêndio Detectado!");
    digitalWrite(LED_PIN, HIGH); // Acende a LED quando o incêndio é detectado
    previousAlarmPublish = currentMillis;
  } else if (fireStatus == HIGH && currentMillis - previousNormalPublish >= NORMAL_INTERVAL) {
    Serial.println("Nenhum alerta.");
    fireStatusFeed.publish("Nenhum alerta.");
    digitalWrite(LED_PIN, LOW); // Apaga a LED quando não há alerta
    previousNormalPublish = currentMillis;
  }
}

void setup() {
  Serial.begin(9600);
  pinMode(FIRE_SENSOR_PIN, INPUT);
  pinMode(LED_PIN, OUTPUT); // Configura o pino da LED como saída
  digitalWrite(LED_PIN, LOW); // Garante que a LED começa desligada
  
  connectWiFi();
  connectMQTT();
}

void loop() {
  if (!mqttClient.connected()) {
    connectMQTT();
  }
  
  mqttClient.ping();
  checkFireSensor();
}
