# Hardware

## Resumo

O Colmi P71 é um smartwatch com SoC RTL8763EWE, memória RAM de 270 KB, armazenamento interno de 128 MB e tela IPS de 1.9" com resolução 240x286.

## Chipset

- SoC: RTL8763EWE
- Arquitetura: ARM Cortex-M / MCU de baixo consumo
- Características esperadas:
  - Bluetooth LE
  - Wi-Fi opcional (dependendo da variante)
  - Controle de display TFT
  - I/O para sensores, touchscreen, bateria e memória

## Memória e armazenamento

- RAM: 270 KB
- Flash/Storage: 128 MB
- Implicações:
  - Sistema deve ser minimalista
  - Sem suporte para runtime pesado
  - Necessidade de compressão de recursos e imagens pequenas

## Display

- Tamanho: 1.9"
- Resolução: 240x286 px
- Tipo: IPS LCD
- Interface: provavelmente SPI ou RGB paralelo, conforme variante do painel
- Necessidade de driver específico para framebuffer e backlight

## Touch

- Tipo: touchscreen capacitivo ou resistivo
- Driver: dependente do painel e do controlador integrado
- Necessidade de calibragem em firmware

## Sensores e periféricos

- Bateria
- Motor de vibração
- LED/Backlight
- Botões físicos
- Bluetooth
- Possível aceleração e monitor de atividade

## Limitações de design

Este hardware é muito limitado para um sistema tradicional do tipo Android ou Wear OS completo. Portanto, a solução mais plausível é:

- kernel minimalista
- runtime customizado em C/C++
- UI leve com framebuffer direto
- gerência de tarefas e eventos simples
- processador dedicado ao display e sensores

## Observações

Este documento servirá como referência para o desenvolvimento do firmware e do sistema operacional customizado.
