# Integrantes do Grupo:
- Felipe Megumi Nakama RM: 552821
- Micael Santos Azarias RM: 552699
- Pedro Henrique Assunção Lima RM: 552746

# Projeto de Monitoramento dos Oceanos 

## Descrição do Projeto

Este projeto visa monitorar a qualidade da água dos oceanos utilizando um sistema de sensores integrado com um Arduino. Os dados coletados incluem a temperatura da água, o nível da água e a claridade da água (em Lux). Os resultados são exibidos em um display OLED SSD1306 e no monitor serial. A intenção é fornecer essas informações valiosas sobre a saúde dos oceanos para populações costeiras, empresas e formuladores de políticas.

## Sensores Utilizados

1. **Sensor de Temperatura DS18B20**:
   - Monitora a temperatura da água, fornecendo dados críticos sobre o ambiente aquático.
2. **Sensor Ultrassônico HC-SR04**:
   - Mede o nível da água, ajudando a identificar variações anormais que podem indicar poluição ou outros problemas ambientais.
3. **Fotoresistor (LDR)**:
   - Detecta mudanças na claridade da água, que podem indicar turbidez e presença de poluentes.

## Componentes Necessários

- Arduino Uno
- Sensor de Temperatura DS18B20
- Sensor Ultrassônico HC-SR04
- Fotoresistor (LDR) com 4 pinos (A0, D0, GND, Vcc)
- Display OLED SSD1306
- Resistor de 4.7kΩ (para o DS18B20)
- Cabos de conexão

## Conexões

### DS18B20
- **GND**: GND do Arduino
- **VCC**: 5V do Arduino
- **DQ (Data)**: Pino digital 2 do Arduino
- **Resistor de pull-up de 4.7kΩ**: Conectado entre DQ (Data) e VCC (5V)

### HC-SR04
- **VCC**: 5V do Arduino
- **GND**: GND do Arduino
- **Trig**: Pino digital 8 do Arduino
- **Echo**: Pino digital 9 do Arduino

### LDR
- **GND**: GND do Arduino
- **VCC**: 5V do Arduino
- **A0**: Pino analógico A0 do Arduino
- **D0**: Não utilizado

### SSD1306 OLED Display
- **GND**: GND do Arduino
- **VCC**: 5V do Arduino
- **SCL**: Pino A5 do Arduino
- **SDA**: Pino A4 do Arduino

## Instruções de Uso

1. **Montagem do Hardware**:
   - Conecte todos os componentes conforme as conexões descritas acima.
   - Certifique-se de que todos os fios estão bem conectados e que o resistor de pull-up está instalado corretamente no DS18B20.

2. **Carregamento do Código**:
   - Abra o Arduino IDE.
   - Copie e cole o código fornecido neste github ou no link para o simulador Wokwi: https://wokwi.com/projects/399742736151854081
   - Instale as seguintes bibliotecas: - `OneWire`, `DallasTemperature`, `Wire`, `Adafruit_GFX`, `Adafruit_SSD1306`
   - Conecte o Arduino ao computador via cabo USB.
   - Selecione a porta correta em `Ferramentas` > `Porta`.
   - Clique em `Carregar` para enviar o código para o Arduino.

3. **Visualização dos Dados**:
   - Abra o monitor serial no Arduino IDE para visualizar os dados em tempo real.
   - Observe as leituras de temperatura, nível da água e claridade da água no display OLED.

## Requisitos

- **Hardware**:
  - Arduino Uno
  - Sensor de Temperatura DS18B20
  - Sensor Ultrassônico HC-SR04
  - Fotoresistor (LDR) com 4 pinos
  - Display OLED SSD1306
  - Resistor de 4.7kΩ
  - Fios de conexão

- **Software**:
  - Arduino IDE
  - Bibliotecas:
    - `OneWire`
    - `DallasTemperature`
    - `Wire`
    - `Adafruit_GFX`
    - `Adafruit_SSD1306`

### Instalação de Bibliotecas

As bibliotecas necessárias podem ser instaladas através do Gerenciador de Bibliotecas do Arduino IDE:
1. Vá para `Sketch` > `Incluir Biblioteca` > `Gerenciar Bibliotecas`.
2. Procure e instale `OneWire`, `DallasTemperature`, `Adafruit GFX Library`, e `Adafruit SSD1306`.

## Informações Relevantes

- **Calibração do LDR**:
  - A conversão de valores de LDR para Lux é um mapeamento simples e pode não ser preciso. Para medições mais precisas, uma calibração adequada e possivelmente um circuito de condicionamento de sinal seriam necessários.
  
- **Manutenção e Expansão**:
  - O sistema pode ser expandido para incluir mais sensores ou para enviar dados para a nuvem para análise remota.
  - A integração com um módulo Wi-Fi (como ESP8266 ou ESP32) pode permitir a transmissão de dados em tempo real para um servidor.

---

Segue o link para o video explicativo no youtube: 
