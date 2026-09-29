# Build e Flash

## Pré-requisitos

- cross-toolchain ARM
- make/cmake
- serial console
- ferramenta de flash específica do hardware

## Estrutura de build

```text
build/
  firmware.bin
  kernel.bin
  bootloader.bin
```

## Comandos sugeridos

```bash
mkdir -p build
cmake -S . -B build
cmake --build build
```

## Flash

```bash
# exemplo genérico
./tools/flash.sh /dev/ttyUSB0
```

## Observações

A ferramenta exata de flash depende do chip e do carregador do fabricante. Esse documento deve ser ajustado quando a plataforma de gravação for confirmada.
