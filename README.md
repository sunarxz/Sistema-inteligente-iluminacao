# 💡 Sistema Inteligente de Iluminação Residencial

Sistema embarcado desenvolvido com Arduino para controle automático de iluminação baseado em sensor de luminosidade (LDR), utilizando lógica condicional e conceitos introdutórios de inteligência artificial.

---

## 📌 Visão Geral

Este projeto tem como objetivo simular um sistema de automação residencial inteligente capaz de acionar automaticamente uma lâmpada (LED) de acordo com a luminosidade do ambiente.

- 🌑 Ambiente escuro → LED liga automaticamente  
- ☀️ Ambiente claro → LED desliga automaticamente  

---

## 📜 Artigo Acadêmico
[Artigo acadêmico.pdf](https://github.com/user-attachments/files/28240935/Artigo.academico.pdf)

---

## 🎯 Objetivo

Desenvolver um sistema embarcado utilizando Arduino que:

- Leia dados de sensores (LDR)
- Tome decisões automáticas
- Controle atuadores (LED)
- Simule conceitos de inteligência artificial baseada em regras

---

## ⚙️ Componentes totais utilizados

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

```cpp
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
```


## 🔌 Diagrama do Circuito

# Sistema ativo (noturno)
<img width="1012" height="688" alt="Sistema ativo (noturno)" src="https://github.com/user-attachments/assets/6fad88b2-190a-403e-9ede-332180088e65" />

# Sistema inativo (dia)
<img width="1048" height="660" alt="Sistema inativo (dia)" src="https://github.com/user-attachments/assets/02d9e8f3-8f6d-46b9-b22d-529363654eeb" />

# LED ligado (zoom)
<img width="965" height="632" alt="LED aceso (zoom)" src="https://github.com/user-attachments/assets/3c5c24cb-092f-45d8-909c-be6784bb948c" />

# LED desligado (zoom)
<img width="986" height="628" alt="LED desligado (zoom)" src="https://github.com/user-attachments/assets/dfcb0d38-3e88-4861-8bd6-19668dea93ff" />

# Componentes
<img width="1013" height="352" alt="Componentes" src="https://github.com/user-attachments/assets/9f9a8127-c25a-4b69-9b0b-61f65fbcca99" />

# Imagem Código
<img width="610" height="712" alt="Codigo" src="https://github.com/user-attachments/assets/4a2e6a5d-75b4-458d-87b5-f59e4269bdf9" />


---

## 🧠 Conceitos aplicados
Sistemas embarcados
Microcontroladores (Arduino)
Sensores e atuadores
Programação em C/C++
Lógica de decisão (if/else)
Inteligência artificial baseada em regras
Simulação conceitual de arquitetura ARM

---

## 🏗️ Arquitetura ARM (conceitual)

Embora o projeto utilize Arduino (arquitetura AVR), o sistema foi analisado sob o ponto de vista de execução em arquitetura ARM Cortex-M.

O fluxo de execução pode ser interpretado como:

Entrada via ADC (sensor LDR)
Processamento em registradores
Execução de instruções condicionais
Controle de saída digital (LED)

---

## 🚀 Como executar
Abrir o código no Arduino IDE
Montar o circuito no Tinkercad ou protoboard
Compilar e enviar o código
Observar o funcionamento automático do LED

---

## 👨‍💻 Autor

Suriel Ormond Franqueline

---

## 📚 Referências
https://www.arduino.cc

Stallings, W. Arquitetura e Organização de Computadores

Material de aula – Microprocessadores e Microcontroladores





