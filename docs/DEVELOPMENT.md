# Desenvolvimento

## Requisitos iniciais

- GCC para ARM/MCU
- CMake ou Make
- ferramenta de depuração serial
- conhecimento de drivers de display e GPIO
- ferramenta de flasheio da plataforma

## Fluxo recomendado

1. Mapear hardware e periféricos
2. Implementar bootloader mínimo
3. Validar framebuffer e display
4. Ativar entradas do touch
5. Implementar relógio e widgets básicos
6. Criar camada de serviços e persistência
7. Expandir para notificações, saúde e Bluetooth

## Organização do código

```text
src/
  boot/
  kernel/
  drivers/
  ui/
  services/
  apps/
```

## Testes recomendados

- boot e validação de RAM
- renderização inicial do display
- calibração do touch
- consumo de bateria
- estabilidade do loop principal

## Padrões

- código em C/C++ com estilo mínimo
- evitar alocação dinâmica em tempo de execução
- priorizar controle explícito de memória
- logs simples via UART

## Objetivo

Construir um firmware funcional e enxuto, com base em hardware de smartwatch de baixa potência.
