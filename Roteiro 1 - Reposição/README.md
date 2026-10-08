# 🔬 Estudo de Plataformas IoT - Roteiro 1: Configuração e Conectividade Inicial

<p align="center">
  <img src="https://github.com/HericoSouza/Estudo-plataformas-IOT/raw/Roteiro1/assets/banner-roteiro1.png" alt="Capa Roteiro 1" width="700px">
</p>

> Documentação prática e passo a passo referente ao **Roteiro 1** do estudo de plataformas de Internet das Coisas (IoT). Este roteiro cobre a configuração inicial do ambiente, conexão do hardware e testes de envio de telemetria básica.

---

## 🎯 Objetivos do Roteiro 1

* Configurar o ambiente de desenvolvimento (IDE, bibliotecas e dependências).
* Estabelecer a comunicação inicial do microcontrolador/dispositivo com a rede.
* Publicar os primeiros dados de sensores utilizando o protocolo MQTT ou HTTP.
* Validar a recepção dos dados na plataforma IoT escolhida.

---

## 🛠️ Materiais e Pré-requisitos

1. **Hardware Utilizado:**
   * ESP8266 / ESP32 (ou dispositivo equivalente)
   * Cabo USB para programação
   * Sensores básicos (ex: DHT11 / DHT22 / LED indicador)

2. **Software e Bibliotecas:**
   * Arduino IDE / VS Code com PlatformIO
   * Bibliotecas de conexão Wi-Fi e Cliente MQTT (ex: `PubSubClient`)

---

## 📸 Evidências e Passos Práticos

| Montagem do Circuito | Monitor Serial (Logs) |
| :---: | :---: |
| <img src="https://github.com/HericoSouza/Estudo-plataformas-IOT/raw/Roteiro1/assets/circuito-roteiro1.png" width="350px"> | <img src="https://github.com/HericoSouza/Estudo-plataformas-IOT/raw/Roteiro1/assets/serial-monitor.png" width="350px"> |
| *Esquemático das ligações físicas* | *Saída de logs indicando conexão com sucesso* |

---

## 🚀 Passo a Passo de Execução

1. **Clone e altere para o branch do roteiro:**
   ```bash
   git clone [https://github.com/HericoSouza/Estudo-plataformas-IOT.git](https://github.com/HericoSouza/Estudo-plataformas-IOT.git)
   cd Estudo-plataformas-IOT
   git checkout Roteiro1
