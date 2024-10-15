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
# Código

``````````````````````````
// Código exemplo Sensor PIR de Moviemnto
// Projeto de Alarme / Automação Residencial
 
#define pinoPIR 8 // Define o pino 8 como "pinoPIR"
#define pino5V 9 // Define o pino 9 como "pino5V"
#define pinoRele 10 // Define o pino 10 como "pinoRele"
 
void setup() {
 
Serial.begin(9600); // Declara o BaundRate em 9600
Serial.println("www.usinainfo.com.br"); // Imprime a frase no monitor serial
pinMode(pinoPIR, INPUT); // Declara o pinoPIR como Entrada
pinMode(pino5V, OUTPUT); // Declara o pino5V como Saída
pinMode(pinoRele, OUTPUT); // Declara o pinoRele como Saída
digitalWrite(pino5V, HIGH); // Põem o pino5V em estado alto = 5V
}
 
void loop() {
 
if (digitalRead(pinoPIR) == LOW) { // Se o Sensor PIR Estiver em nível baixo
digitalWrite (pinoRele, LOW); // Módulo Relé permanece desligado
}
 
if (digitalRead(pinoPIR) == HIGH) { // Se o Sensor PIR estiver em nível Alto
digitalWrite (pinoRele, HIGH); // Liga o Relé
Serial.println("Alarme Acionado"); // Imprime a mensagem no monitor serial
delay (10000); // Aguarda 10 segundo
}
}

``````````````````````````
# esquema
![image](https://github.com/user-attachments/assets/1abf08e6-2874-4ef6-9183-8d170ab4b96d)
