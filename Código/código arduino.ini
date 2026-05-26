#define LDR A0
#define LED 7

int valor;
int limite = 500;

void setup()
{
  Serial.begin(9600);
  pinMode(LED, OUTPUT);
}

void loop()
{
  valor = analogRead(LDR);

  Serial.print("Luz: ");
  Serial.print(valor);

  if (valor > limite)
  {
    digitalWrite(LED, HIGH);
    Serial.println(" -> ESCURO | LED ON");
  }
  else
  {
    digitalWrite(LED, LOW);
    Serial.println(" -> CLARO | LED OFF");
  }

  delay(300);
}
