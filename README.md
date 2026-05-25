# 💡 Sistema Inteligente de Iluminação Residencial

Sistema embarcado desenvolvido com Arduino para controle automático de iluminação baseado em sensor de luminosidade (LDR), utilizando lógica condicional e conceitos introdutórios de inteligência artificial.

---

## 📌 Visão Geral

Este projeto tem como objetivo simular um sistema de automação residencial inteligente capaz de acionar automaticamente uma lâmpada (LED) de acordo com a luminosidade do ambiente.

- 🌑 Ambiente escuro → LED liga automaticamente  
- ☀️ Ambiente claro → LED desliga automaticamente  

---

## 🎯 Objetivo

Desenvolver um sistema embarcado utilizando Arduino que:

- Leia dados de sensores (LDR)
- Tome decisões automáticas
- Controle atuadores (LED)
- Simule conceitos de inteligência artificial baseada em regras

---

## ⚙️ Componentes utilizados

- Arduino UNO  
- Sensor LDR (Light Dependent Resistor)  
- LED  
- Resistor (220Ω)  
- Protoboard  
- Jumpers  

---

## 🧠 Funcionamento do Sistema

O sistema realiza a leitura contínua da luminosidade do ambiente através do LDR.

Em seguida, o valor é comparado com um limite pré-definido:

- Se o valor > limite → ambiente escuro → LED ON  
- Se o valor ≤ limite → ambiente claro → LED OFF  

Esse comportamento representa um sistema de decisão automatizada baseado em regras.

---

## 💻 Código-fonte

```cpp
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

```

## 📊 Diagrama do Sistema
🔄 Fluxo lógico
[LDR Sensor]
     ↓
[Leitura Analógica]
     ↓
[Processamento Arduino]
     ↓
[Decisão (if/else)]
   ↓            ↓
LED ON       LED OFF
## 🔌 Diagrama do Circuito



## 🧠 Conceitos aplicados
Sistemas embarcados
Microcontroladores (Arduino)
Sensores e atuadores
Programação em C/C++
Lógica de decisão (if/else)
Inteligência artificial baseada em regras
Simulação conceitual de arquitetura ARM

## 🏗️ Arquitetura ARM (conceitual)

Embora o projeto utilize Arduino (arquitetura AVR), o sistema foi analisado sob o ponto de vista de execução em arquitetura ARM Cortex-M.

O fluxo de execução pode ser interpretado como:

Entrada via ADC (sensor LDR)
Processamento em registradores
Execução de instruções condicionais
Controle de saída digital (LED)

## 🚀 Como executar
Abrir o código no Arduino IDE
Montar o circuito no Tinkercad ou protoboard
Compilar e enviar o código
Observar o funcionamento automático do LED

## 👨‍💻 Autor

Suriel Ormond Franqueline

## 📚 Referências
https://www.arduino.cc

Stallings, W. Arquitetura e Organização de Computadores

Material de aula – Microprocessadores e Microcontroladores





