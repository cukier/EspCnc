# EspCnc - hardware

Projeto de placa em [KiCad](https://www.kicad.org/) (v9) para a interface
entre um modulo ESP32 e a eletronica da CNC 3035: drivers de motor de passo
(ex. A4988/DRV8825/TMC2208), fins-de-curso, controle de spindle/laser e
alimentacao.

Usado como referencia/ponto de partida o esquematico da buildlog.net,
disponivel em [`doc/esp32_test_schem_v1.pdf`](../doc/esp32_test_schem_v1.pdf):
https://www.buildlog.net/blog/wp-content/uploads/2018/07/esp32_test_schem_v1.pdf

## Arquivos

```
hardware/
├── EspCnc.kicad_pro   # projeto KiCad
├── EspCnc.kicad_sch   # esquematico (folha raiz, ainda vazio)
└── EspCnc.kicad_pcb   # placa (ainda vazia)
```

## Como abrir

Abra `EspCnc.kicad_pro` no KiCad 9 (ou superior).

## Status

Esqueleto inicial do projeto. Proximos passos: desenhar o esquematico com
base na referencia da buildlog.net, definir o mapeamento de pinos do ESP32
usado pelo firmware em `firmware/`, e projetar a PCB.
