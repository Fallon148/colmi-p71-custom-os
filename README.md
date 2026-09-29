# Colmi P71 Custom OS

Sistema operacional customizado para Colmi P71 Ouro - Smartwatch, inspirado em Wear OS do Samsung.

## 📋 Especificações Técnicas

| Especificação | Detalhes |
|--------------|----------|
| **Marca** | Colmi |
| **Modelo** | P71 |
| **Chip** | RTL8763EWE |
| **RAM** | 270 KB |
| **Armazenamento** | 128 MB |
| **Sistema Original** | HarmonyOS |
| **Tela** | 1.9" IPS |
| **Resolução** | 240 x 286 px |
| **Entrada** | Touchscreen |

## 🏗️ Arquitetura do Projeto

```
colmi-p71-custom-os/
├── bootloader/          # Bootloader customizado
├── kernel/              # Kernel do sistema
├── drivers/             # Drivers de hardware
│   ├── display/
│   ├── touch/
│   ├── battery/
│   └── sensor/
├── framework/           # Framework do SO
│   ├── core/
│   ├── ui/
│   └── services/
├── apps/                # Aplicativos padrão
│   ├── clockface/
│   ├── settings/
│   ├── health/
│   └── notifications/
├── tools/               # Ferramentas de build
├── docs/                # Documentação
└── tests/               # Testes
```

## 🎯 Objetivos do Projeto

- [x] Criar estrutura base do repositório
- [ ] Desenvolver bootloader para RTL8763EWE
- [ ] Implementar kernel minimalista
- [ ] Criar drivers essenciais (display, touch, battery)
- [ ] Desenvolver framework de interface
- [ ] Criar aplicativos base (relógio, configurações, saúde)
- [ ] Implementar sincronização com smartphone
- [ ] Otimizar consumo de bateria
- [ ] Criar ferramentas de build e flashing
- [ ] Documentar todo o projeto

## 🛠️ Tecnologias

- **Linguagem Principal**: C/C++
- **Bootloader**: U-Boot customizado
- **Kernel**: Linux minimalista
- **Framework UI**: Qt/QML (otimizado para baixa resolução)
- **Build System**: Make/CMake
- **Versionamento**: Git

## 📱 Funcionalidades Planejadas

### Fase 1 - MVP (Mínimo Viável)
- Exibição de hora/data
- Tela tátil responsiva
- Controle de bateria
- Menu de configurações básicas

### Fase 2 - Intermediária
- Sincronização com smartphone
- Notificações
- Gerenciador de apps
- Sensores (acelerómetro, frequência cardíaca)

### Fase 3 - Avançada
- Health monitoring (passos, calorias, sono)
- Aplicativos adicionais
- Temas customizáveis
- Atualizações OTA

## 🚀 Como Começar

### Pré-requisitos
- GCC ARM cross-compiler
- Make/CMake
- Git
- Ferramentas de flashing (USB serial)

### Build
```bash
git clone https://github.com/Fallon148/colmi-p71-custom-os.git
cd colmi-p71-custom-os
make build
```

### Flashing
```bash
make flash DEVICE=/dev/ttyUSB0
```

## 📚 Documentação

- [Especificações de Hardware](docs/HARDWARE.md)
- [Guia de Desenvolvimento](docs/DEVELOPMENT.md)
- [Arquitetura do Sistema](docs/ARCHITECTURE.md)
- [Build & Flash](docs/BUILD.md)

## 👥 Contribuições

Contribuições são bem-vindas! Por favor:

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob licença MIT. Veja o arquivo [LICENSE](LICENSE) para detalhes.

## 📞 Contato & Suporte

- Issues: [GitHub Issues](https://github.com/Fallon148/colmi-p71-custom-os/issues)
- Discussões: [GitHub Discussions](https://github.com/Fallon148/colmi-p71-custom-os/discussions)

---

**Status do Projeto**: 🔨 Em Desenvolvimento

Última atualização: 2026-09-29
