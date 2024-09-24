# sistema de alarme com sensor de movimento
# Componentes Necessários
Arduino Uno: Controlador principal que processa os sinais do sensor PIR e aciona os dispositivos de alerta (buzina e LEDs).
Sensor de Movimento PIR (Passive Infrared Sensor): Detecta a presença de pessoas ou animais no ambiente, baseando-se na radiação infravermelha emitida por esses corpos.
Buzina: Dispositivo de alerta sonoro que será acionado quando o sensor PIR detectar movimento.
LEDs: Indicadores visuais que acendem quando o sistema detecta movimento. Podem ser usados múltiplos LEDs para maior visibilidade.
Resistores: Utilizados para limitar a corrente que passa pelos LEDs, evitando danos ao circuito.
# Descrição do Funcionamento
Detecção de Movimento: O sensor PIR é posicionado em uma área onde a detecção de movimento é desejada.Este sensor é capaz de detectar variações na radiação infravermelha que indicam a presença de um corpo em movimento.

Processamento no Arduino: Quando o sensor PIR detecta movimento, ele envia um sinal digital para o Arduino Uno. O Arduino, por sua vez, processa esse sinal.Ativação dos Dispositivos de Alerta:

Buzina: O Arduino aciona a buzina, emitindo um som alto para alertar sobre a presença de um intruso.
LEDs: Simultaneamente, os LEDs são acesos para proporcionar um alerta visual adicional.
Envio de Notificação: Se o sistema estiver equipado com um módulo Wi-Fi, o Arduino pode enviar uma mensagem para uma URL ou MQTT broker, informando que um movimento foi detectado.

# Circuito Eletrônico:
Sensor PIR: O pino de saída do sensor PIR é conectado a um dos pinos digitais do Arduino.
Buzina: Um dos pinos digitais do Arduino é conectado ao terminal positivo da buzina, enquanto o terminal negativo é conectado ao GND.
LEDs: Os LEDs são conectados a outros pinos digitais do Arduino, com resistores em série para limitar a corrente.
