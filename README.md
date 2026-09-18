# EspCnc

Controlador ESP32 para uma fresadora CNC 3018/3020/3030-3035, baseado no
firmware [grbl_esp32](https://github.com/bdring/grbl_esp32) (Bart Dring) e no
[esquematico de referencia da buildlog.net](https://www.buildlog.net/blog/wp-content/uploads/2018/07/esp32_test_schem_v1.pdf).

O objetivo e substituir a controladora original da CNC 3035 (tipicamente
baseada em GRBL sobre Arduino/Atmega) por uma placa com ESP32, aproveitando
mais pinos, maior clock, Wi-Fi/Bluetooth e a arquitetura de I/O configuravel
que o grbl_esp32 introduziu.

Este repositorio contem dois projetos independentes:

- [`firmware/`](firmware/) - firmware para o ESP32, em **ESP-IDF** (nao
  Arduino/PlatformIO), inspirado na logica de interpretacao G-code e no
  planejador de movimento do grbl_esp32.
- [`hardware/`](hardware/) - projeto de placa em **KiCad**, com o
  esquematico e PCB da interface entre o ESP32 e os drivers de motor de
  passo, fins-de-curso, spindle/laser e demais perifericos da CNC 3035,
  usando o esquematico da buildlog.net como ponto de partida.
- [`doc/`](doc/) - documentacao de referencia, incluindo o esquematico da
  buildlog.net usado como base do projeto.

## Estrutura

```
EspCnc/
├── firmware/   # Projeto ESP-IDF
├── hardware/   # Projeto KiCad
└── doc/        # Documentacao de referencia (esquematico, etc.)
```

## Firmware (ESP-IDF)

Ver [firmware/README.md](firmware/README.md).

## Hardware (KiCad)

Ver [hardware/README.md](hardware/README.md).

## Referencias

- grbl_esp32 (Bart Dring): https://github.com/bdring/grbl_esp32
- Esquematico ESP32 CNC (buildlog.net): https://www.buildlog.net/blog/wp-content/uploads/2018/07/esp32_test_schem_v1.pdf
- GRBL original: https://github.com/gnea/grbl

## Licenca

Distribuido sob a licenca MIT. Veja [LICENSE](LICENSE).
