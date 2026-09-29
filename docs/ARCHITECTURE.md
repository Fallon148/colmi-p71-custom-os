# Arquitetura do Sistema

## Visão geral

O sistema objetivo para o Colmi P71 deve ser leve, previsível e eficiente em energia. Por conta das limitações do hardware, a arquitetura deve priorizar:

- baixo consumo
- UI responsiva em 240x286
- gerenciamento leve de memória
- drivers mínimos para hardware relevante
- atualização local e diagnósticos simples

## Camadas

### 1. Bootloader
- inicializa CPU
- configura clocks
- ativa memória e periféricos essenciais
- detecta dispositivo e inicia kernel

### 2. Kernel
- scheduler leve
- multitarefa cooperativa ou preemptiva mínima
- gerenciamento de IRQs
- drivers essenciais

### 3. Drivers
- display
- touchscreen
- bateria
- vibração
- GPIO
- bluetooth
- sensores

### 4. Runtime / Framework
- gerenciamento de janelas
- inputs
- renderização em framebuffer
- serviços de notificação
- armazenamento de configurações

### 5. Apps / Serviços
- relógio
- calendário
- saúde
- notificações
- ajustes

## Estrutura de software

```
core/
  kernel/
  runtime/
  services/
ui/
  framebuffer/
  events/
  widgets/
  styles/
platform/
  drivers/
  low_level/
apps/
  watch/
  settings/
  health/
```

## Estratégia de desenvolvimento

- Primeiro, implementar bootloader e base de hardware
- Em seguida, driver de display e touch
- Depois, renderização e interface
- Por fim, apps e integração com Bluetooth

## Observações

Este projeto é um firmware customizado, não um port de Android completo. A arquitetura foi construída para viabilizar um smartwatch funcional em hardware muito limitado.
