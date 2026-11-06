# EMDR2 Controle

App web para controlar a barra de luz EMDR2 (Arduino Uno + fita WS2812B) por Bluetooth (HC-05/HC-06) ou USB.

**Abrir:** https://pesouza.github.io/emdr2/ no Chrome do Android (versão 138 ou mais nova) ou no Chrome do computador.

## Como usar
1. Pareie o HC-05 nas configurações de Bluetooth do Android (senha 1234 ou 0000).
2. Abra o app e toque em **Conectar Bluetooth**; escolha o HC-05.
3. Escolha um preset (Dessens, Recurso, Calma, Foco) ou ajuste padrão, velocidade, série, cor e brilho, e toque em **Iniciar**.

Sem placa, o botão **Simulador** mostra o funcionamento só na tela.

O registro das séries fica apenas no navegador do aparelho; nada é enviado para servidor.

## Protocolo
Comandos de texto a 9600 baud, um por linha: `INICIA`, `PARA`, `PAUSA`, `SEGUE`, `MODO <nome>`, `PRESET <nome>`, `VEL <ms>`, `SERIE <n>`, `COR <nome>|r g b`, `BRILHO <0..255>`, `TAM <1..10>`, `DEMO [s]`, `STATUS`, `AJUDA`.
