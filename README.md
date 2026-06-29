<div align="center">

<img src="imagem_1.png" alt="MULTIFUNCTION SHIELD V1 — Vista Superior" width="800"/>

# MULTIFUNCTION SHIELD V1

**Shield multifuncional para Arduino Uno com LEDs, botões, buzzer, potenciômetro, LDR, conector I2C e borne de terminais — tudo em uma única placa de expansão**

[![KiCad](https://img.shields.io/badge/KiCad-10-blue?logo=kicad&logoColor=white)](https://www.kicad.org/)
[![Compatível](https://img.shields.io/badge/Compat%C3%ADvel-Arduino%20Uno%20R3-teal)](.)
[![Versão](https://img.shields.io/badge/Vers%C3%A3o-V1%202025-orange)](.)
[![Montagem](https://img.shields.io/badge/Montagem-PTH-blueviolet)](.)
[![ZAT ELECTRONIC](https://img.shields.io/badge/Feito%20por-ZAT%20ELECTRONIC-black)](.)
[![Made in Brazil](https://img.shields.io/badge/Made%20in-Brazil%20%F0%9F%87%A7%F0%9F%87%B7-009c3b)](.)

</div>

---

## 📋 Índice

- [MULTIFUNCTION SHIELD V1](#multifunction-shield-v1)
  - [📋 Índice](#-índice)
  - [Visão Geral](#visão-geral)
  - [Renders 3D](#renders-3d)
  - [Funcionalidades](#funcionalidades)
  - [Mapa de Pinos](#mapa-de-pinos)
  - [Especificações Técnicas](#especificações-técnicas)
  - [Lista de Materiais](#lista-de-materiais)
  - [Aplicações](#aplicações)
  - [Estrutura do Repositório](#estrutura-do-repositório)
  - [Como Usar](#como-usar)
    - [Instalação](#instalação)
    - [Exemplo — Piscar os 4 LEDs em sequência](#exemplo--piscar-os-4-leds-em-sequência)
    - [Exemplo — Leitura do potenciômetro e LDR](#exemplo--leitura-do-potenciômetro-e-ldr)
    - [Exemplo — Botões com pull-down](#exemplo--botões-com-pull-down)
  - [Sobre](#sobre)

---

## Visão Geral

**MULTIFUNCTION SHIELD V1** é uma placa de expansão (shield) para **Arduino Uno R3**, projetada pela **ZAT ELECTRONIC** utilizando **KiCad 10**. O shield encaixa diretamente nos conectores do Arduino e disponibiliza um conjunto completo de periféricos prontos para uso imediato em projetos de aprendizado, prototipagem e experimentos com eletrônica e programação.

Em uma única placa são integrados: **4 LEDs coloridos**, **4 botões tácteis**, **1 buzzer**, **1 potenciômetro**, **1 sensor LDR**, **1 conector I2C** (GND / VCC / SDA / SCL) e **1 borne de terminais** — cobrindo as principais necessidades de entrada e saída para projetos com Arduino.

> 💡 Ideal para aulas, workshops, laboratórios maker e iniciantes em eletrônica e programação com Arduino.

---

## Renders 3D

<div align="center">

<img src="imagem_1.png" alt="Vista Superior" width="700"/>

*Vista superior — LEDs coloridos, botões tácteis, buzzer, potenciômetro e LDR*

<br/>

<img src="imagem_2.png" alt="Vista Isométrica Frontal" width="700"/>

*Vista isométrica frontal — pinout Arduino Uno R3 e conector I2C*

<br/>

<img src="imagem_3.png" alt="Vista Isométrica Traseira" width="700"/>

*Vista isométrica traseira — borne de terminais, pinos analógicos e digitais*

</div>

---

## Funcionalidades

- ✅ **4 LEDs 5mm PTH** — azul (L1), vermelho (L2), verde (L3) e amarelo (L4)
- ✅ **4 botões tácteis** (SW1–SW4) — 6×6×5mm PTH, com resistores pull-down 10KΩ
- ✅ **1 buzzer PTH** (BZ1) — sinalização sonora ativa
- ✅ **1 potenciômetro 10KΩ** (POT1) — entrada analógica ajustável
- ✅ **1 sensor LDR** (LDR1) — leitura de luminosidade ambiente
- ✅ **1 conector I2C** (J2 — 4 pinos: GND / VCC / SDA / SCL) — expansão para displays, sensores e módulos I2C
- ✅ **1 borne de terminais KRE 3 pinos** (J1 — D11 / D12 / GND) — conexão externa por parafuso
- ✅ **Resistores de proteção 220Ω** (R1–R4, R9) — para os LEDs e buzzer
- ✅ **Resistores pull-down 10KΩ** (R5–R8, R10) — para botões e LDR
- ✅ **Encaixe direto** no Arduino Uno R3 — sem soldagem adicional no Arduino
- ✅ **Todos os componentes PTH** — montagem manual simples
- ✅ **Made in Brazil** — serigrafia na PCB

---

## Mapa de Pinos

| Periférico | Pino Arduino | Descrição |
|------------|-------------|-----------|
| **L1** — LED Azul | D2 | Saída digital |
| **L2** — LED Vermelho | D3 | Saída digital (PWM) |
| **L3** — LED Verde | D4 | Saída digital |
| **L4** — LED Amarelo | D5 | Saída digital (PWM) |
| **SW1** — Botão 1 | D6 | Entrada digital |
| **SW2** — Botão 2 | D7 | Entrada digital |
| **SW3** — Botão 3 | D8 | Entrada digital |
| **SW4** — Botão 4 | D9 | Entrada digital |
| **BZ1** — Buzzer | D10 | Saída digital (PWM) |
| **POT1** — Potenciômetro | A0 | Entrada analógica |
| **LDR1** — Sensor de luz | A1 | Entrada analógica |
| **J2 SDA** — I2C Dados | A4 (SDA) | Comunicação I2C |
| **J2 SCL** — I2C Clock | A5 (SCL) | Comunicação I2C |
| **J1** — Borne | D11 / D12 / GND | Terminal externo |

---

## Especificações Técnicas

| Parâmetro | Valor |
|-----------|-------|
| **Compatibilidade** | Arduino Uno R3 (encaixe direto) |
| **LEDs** | 4x 5mm PTH — azul, vermelho, verde, amarelo |
| **Botões** | 4x tácteis 6×6×5mm PTH |
| **Buzzer** | 1x PTH ativo |
| **Potenciômetro** | 1x 10KΩ PTH |
| **Sensor de Luz** | 1x LDR PTH |
| **Conector I2C** | 1x header 4 pinos 2,54mm (GND / VCC / SDA / SCL) |
| **Borne de Terminais** | 1x KRE 3 pinos, passo 5,0mm (D11 / D12 / GND) |
| **Resistores LEDs/Buzzer** | 220Ω — R1, R2, R3, R4, R9 |
| **Resistores Pull-down** | 10KΩ — R5, R6, R7, R8, R10 |
| **Tensão de operação** | 5V (alimentado pelo Arduino) |
| **Tipo de montagem** | PTH — Através-furo |
| **Ferramenta de Projeto** | KiCad 10 |
| **Versão** | V1 — 2025 |

---

## Lista de Materiais

| Ref | Componente | Valor / Cor | Encapsulamento |
|-----|-----------|------------|----------------|
| A1 | Arduino Uno R3 | — | Shield (encaixe) |
| L1 | LED 5mm | Azul | PTH 5mm |
| L2 | LED 5mm | Vermelho | PTH 5mm |
| L3 | LED 5mm | Verde | PTH 5mm |
| L4 | LED 5mm | Amarelo | PTH 5mm |
| SW1–SW4 | Botão Táctil | 6×6×5mm | PTH |
| BZ1 | Buzzer | Ativo | PTH |
| POT1 | Potenciômetro | 10KΩ | PTH |
| LDR1 | Sensor de Luz | LDR | PTH Vertical |
| J1 | Borne de Terminais | D11 / D12 / GND | KRE 3 pinos 5,0mm |
| J2 | Conector I2C | GND / VCC / SDA / SCL | Header 4 pinos 2,54mm |
| R1, R2, R3, R4, R9 | Resistor de proteção | 220Ω | Axial 0,5W PTH |
| R5, R6, R7, R8, R10 | Resistor pull-down | 10KΩ | Axial 0,5W PTH |

---

## Aplicações

- 🎓 **Ensino de eletrônica e programação** — plataforma completa para aprender Arduino do zero
- 🔬 **Prototipagem rápida** — periféricos prontos sem necessidade de protoboard
- 🏫 **Laboratórios maker e escolas técnicas** — kit de experimentos em uma única placa
- 🎮 **Projetos interativos** — jogos, quizzes e desafios com LEDs e botões
- 📡 **Integração com módulos I2C** — displays OLED, sensores de temperatura, RTC, etc.
- 🔊 **Projetos sonoros** — alarmes, melodias e sinalizações com buzzer
- 🌅 **Automação com luz** — controle baseado em luminosidade via LDR

---

## Estrutura do Repositório

```
MULTIFUNCTION_SHIELD_V1_2025/
├── MULTIFUNCTION_SHIELD_V1_2025.kicad_pro   # Arquivo de projeto KiCad
├── MULTIFUNCTION_SHIELD_V1_2025.kicad_sch   # Esquemático (KiCad 10)
├── MULTIFUNCTION_SHIELD_V1_2025.kicad_pcb   # Layout da PCB (KiCad 10)
├── MULTIFUNCTION_SHIELD_V1_2025.kicad_prl   # Configurações locais
├── packages3D/                              # Modelos 3D arquivados
│   ├── LED 5mm Blue.step
│   ├── LED 5mm Red.step
│   ├── LED 5mm Green.step
│   ├── LED 5mm Yellow.step
│   ├── SW_PUSH_6mm_H5mm.wrl
│   ├── Buzzer_12x9.5RM7.6.wrl
│   ├── Rez10K.stp
│   ├── R_LDR_5.1x4.3mm_P3.4mm_Vertical.wrl
│   ├── DG306-5.0-03P-12-00AH.STEP
│   ├── PinHeader_1x04_P2.54mm_Vertical.wrl
│   ├── SIL_Socket06_.stp
│   ├── SIL_Socket08_.stp
│   ├── SIL_Socket10_.stp
│   └── Resistor Axial 0.5W *.STEP
├── fp-info-cache                            # Cache de footprints
├── imagem_1.png                             # Render 3D superior
├── imagem_2.png                             # Render 3D isométrico frontal
├── imagem_3.png                             # Render 3D isométrico traseiro
└── README.md
```

---

## Como Usar

### Instalação

1. Encaixe o **MULTIFUNCTION SHIELD V1** diretamente nos conectores do Arduino Uno R3
2. Conecte o Arduino ao computador via USB
3. Abra a **Arduino IDE** ou **PlatformIO** e selecione a placa **Arduino Uno**
4. Carregue seu sketch e comece a experimentar

### Exemplo — Piscar os 4 LEDs em sequência

```cpp
#define LED_AZUL    2
#define LED_VERMELHO 3
#define LED_VERDE   4
#define LED_AMARELO 5

void setup() {
  pinMode(LED_AZUL,     OUTPUT);
  pinMode(LED_VERMELHO, OUTPUT);
  pinMode(LED_VERDE,    OUTPUT);
  pinMode(LED_AMARELO,  OUTPUT);
}

void loop() {
  digitalWrite(LED_AZUL, HIGH);    delay(300);
  digitalWrite(LED_AZUL, LOW);
  digitalWrite(LED_VERMELHO, HIGH); delay(300);
  digitalWrite(LED_VERMELHO, LOW);
  digitalWrite(LED_VERDE, HIGH);   delay(300);
  digitalWrite(LED_VERDE, LOW);
  digitalWrite(LED_AMARELO, HIGH); delay(300);
  digitalWrite(LED_AMARELO, LOW);
}
```

### Exemplo — Leitura do potenciômetro e LDR

```cpp
void setup() {
  Serial.begin(9600);
}

void loop() {
  int pot = analogRead(A0); // potenciômetro
  int ldr = analogRead(A1); // sensor de luz
  Serial.print("POT: "); Serial.print(pot);
  Serial.print(" | LDR: "); Serial.println(ldr);
  delay(500);
}
```

### Exemplo — Botões com pull-down

```cpp
#define BTN1 6
#define BTN2 7
#define BTN3 8
#define BTN4 9
#define BUZZER 10

void setup() {
  pinMode(BTN1, INPUT);
  pinMode(BTN2, INPUT);
  pinMode(BTN3, INPUT);
  pinMode(BTN4, INPUT);
  pinMode(BUZZER, OUTPUT);
}

void loop() {
  if (digitalRead(BTN1) == HIGH) {
    tone(BUZZER, 1000, 200); // aciona buzzer ao pressionar SW1
  }
}
```

## Sobre

<div align="center">

Projetado por **ZAT ELECTRONIC**

*MULTIFUNCTION SHIELD V1 — 2025 — Made in Brazil 🇧🇷*

[![KiCad](https://img.shields.io/badge/Projetado%20com-KiCad%2010-blue)](https://www.kicad.org/)
[![Open Source Hardware](https://img.shields.io/badge/Open%20Source-Hardware-brightgreen)](https://www.oshwa.org/)

</div>