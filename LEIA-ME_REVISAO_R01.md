# MULTIFUNCTION SHIELD V1 — Revisão R01 (organização) — 2026-11-12
Zat Electronic · KiCad 10.0 · mesmo padrão do ZATINO PTH/SMD V2

## O que mudou
- Esquema plano -> capa A2 + 3 folhas: 02 ARDUINO (A4), 03 ENTRADAS (A4), 04 SAIDAS (A4).
- Projeto renomeado sem espaços: MULTIFUNCTION_SHIELD_V1.kicad_pro / .kicad_sch / .kicad_pcb.
- Reanotação (ordem do KiCad, 1º livre após 0; chaves desenhadas em linha para seguir D6-D9):
  L1..L4 -> LED1..LED4 · POT1 -> RV1 · LDR1 -> R2 · R10 -> R1 · R5..R8 -> R3..R6 · R1..R4 -> R7..R10 · R9 -> R11
  (A1, BZ1, J1, J2, SW1-SW4 sem mudança)
- Values normalizados (10k, 220R, LED_5mm_<COR>...), Descrição PT, Stock Code, Package Group, title block Zat.
- A1: ZAT_Board_Arduino:ARDUINO_UNO_R3_Headers (símbolo/footprint globais, fora da simulação).
- LDR: Device:R_Photo (o filtro do A9013 não aceitava o footprint de 5 mm).
- J1: ZAT_Connector:Screw_Terminal_01x03 (cópia do KiCad com filtro que aceita ZAT_TerminalBlock).
- POT: símbolo atualizado da biblioteca (lib_symbol_mismatch).
- PWR_FLAG em +5V e GND (vêm do Arduino). Pinos livres do A1 com No Connect. Nenhuma severidade em "ignore".

## PCB (nenhum componente, trilha ou zona movida)
- Contorno da placa (Edge.Cuts) estava dentro do footprint do A1 e foi para a placa (mesmas 27 linhas).
- A1 sem o courtyard do tamanho da placa: acabaram os 23 courtyards_overlap e 58 pth_inside_courtyard.
- Footprints KiCad 10 / ZAT com 3D da pasta 3dmodels:
  LEDs ZAT_LED azul/vermelho/verde/amarelo · resistores ZAT_Resistor_THT 220R/10K ·
  RV1 ZAT_Potentiometer_THT:..._10K_EdgeMount (Rez10K.stp; serigrafia termina 0,2 mm antes da borda) ·
  J1 ZAT_TerminalBlock:..._DG306 (DG306-5.0-03P) · chaves, buzzer, LDR e J2 com 3D padrão do KiCad 10.
- Logos ZAT/KiCad/OSHW: courtyard real e "Not in schematic"; OSHW virou arte da placa.
- Referências visíveis em F.SilkS 1,0 mm, fora do corpo, sem sobrepor nada.
- Arte: blocos GND refeitos sem cobrir os pads GND_1/GND_2/GND_3 nem os textos; "GND" do topo 0,8 mm;
  "AREF" 0,8 mm na vertical sob o pino (igual a SCL/SDA, fora do círculo do buzzer); linha sob ANALOG IN encurtada.
- .kicad_dru só com "(version 1)".

## Biblioteca global (já gravada no PC)
- symbols/ZAT_Connector: + Screw_Terminal_01x03
- footprints/ZAT_LED: + LED_D5.0mm_Green, LED_D5.0mm_Yellow
- footprints/ZAT_Potentiometer_THT (nova): Potentiometer_Piher_T-16H_Single_Horizontal_10K_EdgeMount
- footprints/ZAT_TerminalBlock (nova): TerminalBlock_MaiXu_MX126-5.0-03P_1x03_P5.00mm_DG306
- fp-lib-table global: + ZAT_Potentiometer_THT, ZAT_TerminalBlock

## Pontos de projeto
- IMPORTANTE: os botões têm PULL-UP (10k para +5V, botão para GND): pressionado = LOW.
  O README dizia pull-down e o exemplo testava HIGH — README corrigido.
- ATENÇÃO: buzzer direto no D10 por 220R (~23 mA): usar buzzer ATIVO ou tone() com passivo; magnético precisa de transistor.
- ATENÇÃO: borne J1 (D11/D12) sem proteção: 0-5 V, máx. 20 mA por pino.
- MELHORIA: I2C sem pull-ups na placa (depende do módulo). GND_3 (ao lado do AREF) não ligado (o UNO já liga ao GND).

## Após abrir no KiCad
1. Reiniciar o KiCad (bibliotecas novas).
2. ERC no esquema.
3. PCB: B (preencher zonas) -> F8 (Update PCB from Schematic: deve vir sem alterações) -> DRC.
