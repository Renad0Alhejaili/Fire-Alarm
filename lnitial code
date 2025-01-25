const int ledpin_flame = 13; // LED for flame detection
const int flamepin = A2;    // Flame sensor pin
const int ledpin_smoke = 12; // LED for smoke detection
const int smokepin = A1;    // Smoke sensor pin
const int buzpin = 11;      // Buzzer pin
const int threshold_flame = 200; // Threshold value for flame sensor
const int threshold_smoke = 300; // Threshold value for smoke sensor
const int sample_count = 10;     // Number of samples for averaging
int flamesensvalue = 0;      // Initialize flame sensor reading
int smokesensvalue = 0;      // Initialize smoke sensor reading

void setup() {
  pinMode(ledpin_flame, OUTPUT);
  pinMode(flamepin, INPUT);
  pinMode(ledpin_smoke, OUTPUT);
  pinMode(smokepin, INPUT);
  pinMode(buzpin, OUTPUT);
}

int getAverageReading(int pin) {
  long sum = 0;
  for (int i = 0; i < sample_count; i++) {
    sum += analogRead(pin);
    delay(10); // Short delay between samples
  }
  return sum / sample_count;
}

void loop() {
  // Read sensor values with averaging
  flamesensvalue = getAverageReading(flamepin); // Reads averaged data from flame sensor
  smokesensvalue = getAverageReading(smokepin); // Reads averaged data from smoke sensor

  // Check flame sensor
  if (flamesensvalue <= threshold_flame) { // If flame is detected
    digitalWrite(ledpin_flame, HIGH); // Turn on flame LED
    tone(buzpin, 100);                // Turn on buzzer
  } else {
    digitalWrite(ledpin_flame, LOW); // Turn off flame LED
  }

  // Check smoke sensor
  if (smokesensvalue >= threshold_smoke) { // If smoke is detected
    digitalWrite(ledpin_smoke, HIGH); // Turn on smoke LED
    tone(buzpin, 50);                // Turn on buzzer
  } else {
    digitalWrite(ledpin_smoke, LOW); // Turn off smoke LED
  }

  // Turn off buzzer if no detection
  if (flamesensvalue > threshold_flame && smokesensvalue < threshold_smoke) {
    noTone(buzpin);
  }

  delay(100); // Short delay for stability
}
