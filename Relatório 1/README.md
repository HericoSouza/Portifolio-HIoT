# Introdução

Este projeto apresenta o desenvolvimento de uma aplicação embarcada utilizando um microcontrolador ESP32, com o objetivo de aplicar conceitos fundamentais de programação e montagem de circuitos para Internet das Coisas. A aplicação utiliza um potenciômetro, um sensor LDR e um botão como entradas, além de dois LEDs como elementos de saída.

O sistema possui dois modos de funcionamento: manual e automático. No modo manual, selecionado inicialmente pelo microcontrolador, o valor de um potenciômetro é obtido por meio do conversor analógico-digital (ADC). Já no modo automático, o valor utilizado é proveniente de um LDR, permitindo que o comportamento do circuito seja influenciado pela intensidade luminosa do ambiente. A alternância entre os modos é realizada por meio de um botão.

Os valores obtidos pelas entradas analógicas são utilizados para controlar o funcionamento dos LEDs. O primeiro LED tem sua intensidade luminosa ajustada por modulação por largura de pulso (PWM), enquanto o segundo LED pisca em intervalos que variam entre 100 ms e 1000 ms, de acordo com o valor lido pelo ADC. Para isso, é necessário realizar a conversão dos valores obtidos pelo microcontrolador para as faixas adequadas de operação das saídas.

## Diagrama de montagem

A montagem utiliza um ESP32, um potenciômetro, um LDR, um botão e dois LEDs. As entradas analógicas são conectadas aos pinos GPIO 34 e GPIO 32, enquanto os LEDs são controlados pelos pinos GPIO 16 e GPIO 17.

```mermaid
flowchart LR
    ESP32[ESP32]

    POT[Potenciômetro]
    LDR[LDR + resistor de 10 kΩ]
    BOT[Botão]
    R1[Resistor do LED 1]
    R2[Resistor do LED 2]
    LED1[LED 1]
    LED2[LED 2]

    POT -->|Saída analógica| GPIO34[GPIO 34 - ADC]
    LDR -->|Saída analógica| GPIO32[GPIO 32 - ADC]
    BOT -->|Entrada digital| GPIO26[GPIO 26 - INPUT\_PULLUP]

    GPIO34 --> ESP32
    GPIO32 --> ESP32
    GPIO26 --> ESP32

    ESP32 -->|PWM| GPIO16[GPIO 16]
    ESP32 -->|PWM| GPIO17[GPIO 17]

    GPIO16 --> R1 --> LED1
    GPIO17 --> R2 --> LED2

    ESP32 --> VCC[3,3 V]
    ESP32 --> GND[GND]

    VCC --> POT
    VCC --> LDR
    GND --> POT
    GND --> LDR
    GND --> BOT
```
> **Observação:** diagrama gerado por I.A

## Modo manual

Potenciômetro no máximo, LED no brilho máximo!

![Circuito no modo manual](assets/manual.jpeg)

## Modo automático

Muita luz, LED no brilho mínimo!

![Circuito no modo automático](assets/auto.jpeg)

> **Observação:** o código executado na montagem foi ligeiramente diferente do código presente neste repositório. Na versão utilizada na montagem, considerava-se que, quanto maior a luminosidade do ambiente, menor deveria ser o brilho do LED. Já na versão “corrigida” disponível neste repositório, esse comportamento foi invertido: quanto maior a luminosidade do ambiente, maior será o brilho do LED.
