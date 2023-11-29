# arduino-assignment
int sensorvalue=0;
void setup()
{
  Serial.begin(9600);
  pinMode(A1,INPUT);
}
void loop()
{
  sensorvalue=analogRead(A1);
  Serial.print("SENSOR VALUE");
  Serial.println(sensorvalue);
  int voltage=sensorvalue*(5000/1024.0);
  int temperature=(voltage-500)/10;
  Serial.print("TEMPERATURE");
  Serial.print(temperature);
}
