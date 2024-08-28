#include <Wire.h>
#include <BH1750.h>
#include <WiFiNINA.h>
#include <ArduinoHttpClient.h>

// WiFi Credentials
char ssid[] = "AkshitMittal";      // Your WiFi SSID
char pass[] = "akshitmittal";  // Your WiFi Password

// IFTTT Credentials
const char* host = "maker.ifttt.com";
const int port = 80;
const String eventName = "sunlight_detected";
const String iftttKey = "lGuPBie3kqV2rXfEGy8hHucSXRl9dKFenulo2rUH--p";

// Light Sensor Threshold
const float lightThreshold = 500.0; // Adjust as needed

// BH1750 Sensor Object
BH1750 lightMeter;

// WiFi Client and HTTP Client Objects
WiFiClient wifi; //This object manages the WiFi connection
HttpClient client = HttpClient(wifi, host, port); //This object is used to send HTTP requests to the IFTTT server using the WiFi connection

// State Variables
bool sunlightDetected = false;

void setup() {
  Serial.begin(9600);
  
  // Start I2C communication
  Wire.begin();
  
  // Initialize the light sensor
  lightMeter.begin();
  
  // Connect to WiFi
  connectWiFi();
}

void loop() {
  // Read light level from BH1750 sensor
  float lux = lightMeter.readLightLevel();
  Serial.print("Light: ");
  Serial.print(lux);
  Serial.println(" lx");

  // Check if light level exceeds threshold
  if (lux > lightThreshold) {
    if (!sunlightDetected) {
      sendIFTTTEvent("Sunlight Started", lux); // Send notification for sunlight started
      sunlightDetected = true;
    }
  } else {
    if (sunlightDetected) {
      sendIFTTTEvent("Sunlight Stopped", lux); // Send notification for sunlight stopped
      sunlightDetected = false;
    }
  }

  // Delay before the next reading
  delay(60000);  // Check every minute
}

void connectWiFi() {
  Serial.print("Connecting to WiFi...");
  while (WiFi.begin(ssid, pass) != WL_CONNECTED) {
    delay(1000);
    Serial.print(".");
  }
  Serial.println("Connected!");
}

void sendIFTTTEvent(String value, float lux) {
  // Prepare URL and data to be sent to IFTTT
  String url = "/trigger/" + eventName + "/with/key/" + iftttKey;
  String postData = "{\"value1\":\"" + value + "\", \"value2\":\"" + String(lux) + "\"}";

  // Send HTTP POST request to IFTTT
  client.beginRequest();
  client.post(url);
  client.sendHeader("Content-Type", "application/json");
  client.sendHeader("Content-Length", postData.length());
  client.beginBody();
  client.print(postData);
  client.endRequest();
  
  // Get the response from IFTTT
  int statusCode = client.responseStatusCode();
  String response = client.responseBody();
  
  // Print response for debugging
  Serial.print("Status: ");
  Serial.println(statusCode);
  Serial.print("Response: ");
  Serial.println(response);
}
