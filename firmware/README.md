# EspCnc - firmware

Firmware do controlador de CNC baseado em ESP32, escrito com o
[ESP-IDF](https://github.com/espressif/esp-idf) (framework nativo da
Espressif, sem Arduino/PlatformIO).

Serve de base para portar/reimplementar a logica do
[grbl_esp32](https://github.com/bdring/grbl_esp32): interpretador G-code,
planejador de movimento (planner), geracao de pulsos de step/dir por timer e
mapeamento de pinos configuravel.

## Requisitos

- [ESP-IDF](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/index.html)
  (v5.x recomendado)
- Placa com ESP32 (ex.: a interface descrita em `hardware/`)

## Build e flash

```sh
cd firmware
. $IDF_PATH/export.sh   # carrega o ambiente do ESP-IDF
idf.py set-target esp32
idf.py build
idf.py -p /dev/ttyUSB0 flash monitor
```

## Estrutura

```
firmware/
├── CMakeLists.txt        # projeto ESP-IDF
├── sdkconfig.defaults    # configuracoes padrao (flash, etc.)
└── main/
    ├── CMakeLists.txt
    └── main.c            # ponto de entrada (app_main)
```

## Status

Esqueleto inicial do projeto. Ainda faltam: mapeamento de pinos de acordo
com o esquematico em `hardware/`, geracao de step/dir via timer/RMT,
interpretador G-code e maquina de estados do GRBL.
