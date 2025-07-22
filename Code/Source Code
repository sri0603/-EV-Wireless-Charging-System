#include <Wire.h>
#include <LiquidCrystal_I2C.h>

// Pin configuration
const int hallPin = 4;         // Hall effect sensor pin
const int relayPin = 3;        // Relay control pin

LiquidCrystal_I2C lcd(0x27, 16, 2);

void setup() {
  pinMode(hallPin, INPUT);
  pinMode(relayPin, OUTPUT);

  lcd.init();
  lcd.backlight();
  lcd.setCursor(0, 0);
  lcd.print("EV Charging Sys");
  lcd.setCursor(0, 1);
  lcd.print("Booting up...");
  delay(3000);
  lcd.clear();
}

void loop() {
  // Step 1: Power ON transmitter briefly
  digitalWrite(relayPin, HIGH); // ON (active low)
  lcd.setCursor(0, 0);
  lcd.print("Power: ON        ");
  lcd.setCursor(0, 1);
  lcd.print("Detecting field...");
  delay(20000);  // Give time for magnetic field to build

  // Step 2: Read Hall sensor
  int fieldDetected = digitalRead(hallPin);  // HIGH = magnetic field present

  if (fieldDetected == HIGH) {
    // Proper alignment
    lcd.setCursor(0, 0);
    lcd.print("Field: YES        ");
    lcd.setCursor(0, 1);
    lcd.print("Charging ON       ");
    delay(5000); // Maintain charging for longer
  } else {
    // Misalignment detected
    digitalWrite(relayPin, LOW); // Turn OFF relay
    lcd.setCursor(0, 0);
    lcd.print("Field: NO         ");
    lcd.setCursor(0, 1);
    lcd.print("Charging OFF      ");
    delay(6000); // Wait longer before retrying
  }

  lcd.clear();
}
