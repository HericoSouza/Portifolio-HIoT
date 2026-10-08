<div align="center">

# 🌐 Portfólio HIoT

**Internet das Coisas • Sistemas embarcados • Experimentação prática**

Repositório acadêmico com relatórios, códigos, diagramas e materiais de atividades relacionados a projetos de hardware e Internet das Coisas.

</div>

---

## 📖 Sobre o repositório

Este portfólio reúne atividades práticas desenvolvidas no contexto de **HIoT**, documentando experiências com microcontroladores, sensores, circuitos eletrônicos e programação embarcada. A organização dos materiais busca facilitar a consulta aos experimentos, às montagens e aos códigos utilizados.

## 📂 Conteúdo

### Relatório 1 — Entradas analógicas e controle de LEDs

Aplicação com **ESP32** que combina um potenciômetro, um sensor de luminosidade (LDR), um botão e dois LEDs.

O experimento contempla:
- Alternância entre modo manual, controlado pelo potenciômetro, e modo automático, baseado na luminosidade lida pelo LDR.
- Leitura analógica com o ADC do ESP32.
- Controle de brilho dos LEDs por PWM.
- Piscar de um LED com intervalo variável conforme a leitura analógica.
- Código-fonte, diagrama de montagem e imagens do circuito.

**Arquivos:** [`Relatório 1/`](Relat%C3%B3rio%201/)

### Relatório 2 — Medição de distância com sensor ultrassônico

Experimento com **ESP32** e sensor ultrassônico **HC-SR04** para medir a distância de um objeto e exibir os resultados pela comunicação serial.

O material aborda:
- Disparo e leitura do sinal do sensor por meio dos pinos TRIG e ECHO.
- Cálculo da distância a partir do tempo de retorno do eco.
- Configuração de um limite máximo de distância.
- Montagem do circuito, código-fonte e registro da saída serial.

**Arquivos:** [`Relatório 2/`](Relat%C3%B3rio%202/)

> **Atenção:** ao reproduzir a montagem do HC-SR04, confira as ligações e utilize um divisor de tensão no sinal ECHO quando necessário para adequar o nível de 5 V à entrada de 3,3 V do ESP32.

### Roteiros e atividades de reposição

A pasta [`Roteiro 1 - Reposição/`](Roteiro%201%20-%20Reposi%C3%A7%C3%A3o/) contém documentos e links para simulações de circuitos. A pasta [`Roteiro 2 - Reposição/`](Roteiro%202%20-%20Reposi%C3%A7%C3%A3o/) reúne o material correspondente ao segundo roteiro.

### Projeto final

A pasta [`Projeto Final/`](Projeto%20Final/) está reservada ao material relacionado ao projeto final.

## 🧰 Tecnologias e ferramentas

- **ESP32** — microcontrolador utilizado nos experimentos.
- **Arduino / C++** — programação embarcada.
- **Sensores e componentes eletrônicos** — potenciômetro, LDR, botão, LEDs e sensor ultrassônico HC-SR04.
- **Arduino IDE / Monitor Serial** — compilação, gravação e observação das leituras.
- **Wokwi e Falstad** — recursos de simulação e representação de circuitos presentes nos materiais.

A utilização de cada ferramenta depende da atividade; consulte o relatório correspondente para ver os detalhes.

## 🚀 Como acessar os materiais

Clone o repositório:

```bash
git clone https://github.com/HericoSouza/Portifolio-HIoT.git
```

Entre na pasta do projeto:

```bash
cd Portifolio-HIoT
```

Abra os arquivos Markdown para ler os relatórios, os arquivos `.ino` para consultar os códigos e os documentos incluídos nas pastas de roteiros para acessar as demais atividades.

Para executar os experimentos físicos, será necessário o hardware indicado em cada relatório e um ambiente compatível com a programação do ESP32.

## 👥 Integrantes

- Hérico Souza
- Francisco Cirino
- Dieguito Maradona
- Ivyson Lucas
- Matheus Vidal

## 🎯 Objetivo acadêmico

Registrar o desenvolvimento dos experimentos, documentar as soluções implementadas e reunir os materiais de apoio em um único repositório, favorecendo a consulta, a colaboração e o acompanhamento do aprendizado.

---

<div align="center">

**Portfólio HIoT — projetos e experimentos de Internet das Coisas**

</div>
