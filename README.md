# Guia inicial do ESP8266

O ESP8266 é um microcontrolador com grande capacidade de processamento (80 MHz de processador com 96 KB de RAM para dados), com suporte a redes Wifi. [Seu artigo na Wikipédia](https://en.wikipedia.org/wiki/ESP8266) é um bom ponto de partida para entender melhor. Ele está disponível em vários empacotamentos, onde a versão chamada de ESP-01 pode ser utilizada como um chip para fornecer acesso Wifi para o Arduino (ironicamente possuindo muito mais capacidade de processamento que o próprio Arduino Uno R3). O ESP8266 sozinho pode ser utilizado no lugar do Arduino utilizando a mesma IDE para processamento, no entanto nosso foco aqui é utilizá-lo como um periférico no Arduino.

Pode ser necessário atualizar o Firmware no ESP-01. A versão mais atual (esp8266_nonos_sdk_v2.0.0_16_08_10) pode ser encontrada na pasta do Github ou [aqui](http://espressif.com/en/support/download/sdks-demos). Aparentemente a versão 2.1 não é compatível com a versão de 4 Mb de memória ROM. Os arquivos para atualização do Firmware eagle.flash.bin e eagle.irom0text.bin estarão no arquivo compactado na pasta bin/at/noboot. Também serão utilizados os arquivos esp_init_data_default.bin e blank.bin na pasta /bin.

Para gravar o firmware podem ser utilizados diversos softwares. Existe uma ferramenta muito rica escrita em Python chamada [esptool.py](https://github.com/espressif/esptool), no entanto usaremos o gravador oficial (flash_download_tools_v3.4.9.2_0), disponível na pasta ou em seu [site oficial](http://www.espressif.com/en/support/download/other-tools). Para o ESP entrar no modo de gravação da imagem é necessário iniciá-lo com a porta GPIO0 aterrada. Também é possível colocar o reset no terra, aterrar o GPIO0, remover o reset do terra e posteriormente o GPIO0.

O [site do Filipeflop](http://blog.filipeflop.com/wireless/upgrade-de-firmware-do-modulo-esp8266.html) demonstra a montagem do circuito necessária. As configurações do gravador de ROM podem ser as mesmas da imagem abaixo:


