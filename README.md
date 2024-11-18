# Edifícios Inteligentes para Economia de Energia

Este repositório contém o projeto de um **sistema de automação inteligente** utilizando Arduino, que combina **eficiência energética** e **segurança contra incêndios**. A implementação foca na criação de ambientes comerciais e residenciais mais sustentáveis, seguros e conectados, utilizando tecnologias de Internet das Coisas (IoT).

# **Objetivo do Projeto**

Desenvolver um sistema integrado que:
- **Otimize o consumo de energia** por meio de controle automatizado de iluminação e climatização.
- **Garanta a segurança** dos ocupantes, detectando incêndios rapidamente e alertando tanto localmente quanto remotamente.
- Contribua para a **sustentabilidade ambiental** com práticas mais eficientes no uso de energia.


**Componentes Utilizados**

- **Placa ESP8266 NodeMCU V3**: Microcontrolador com Wi-Fi integrado para comunicação IoT.
- **Sensor de Chama/Fogo KY-026**: Detecta incêndios por meio da radiação infravermelha emitida pelas chamas.
- **Protoboard e Jumpers**: Para montagem e conexão dos circuitos.
- **Atuador LED Vermelho (5mm)**: Indicador visual de emergência.
- **Cabo USB**: Alimentação do sistema.
- **Sistema de Climatização Inteligente**: Controle automatizado de temperatura, umidade e qualidade do ar.
- **Plataforma IoT (Adafruit e MQTT Dash)**: Monitoramento remoto e envio de comandos pela internet.

**Funcionamento do Sistema**

1. **Detecção de Incêndio**:
   - O sensor KY-026 monitora continuamente o ambiente.
   - Em caso de detecção de fogo, um sinal é enviado para a placa ESP8266.

2. **Respostas Automáticas**:
   - Alerta local: Acionamento de alarmes sonoros e visuais.
   - Alerta remoto: Envio de notificações para dispositivos conectados via Wi-Fi.

3. **Otimização de Energia**:
   - Ajuste automático da iluminação e climatização com base nos dados captados pelos sensores.

---

# **Resultados Esperados**

- **Economia de energia**: Redução de até 30% no consumo, com base em testes preliminares.
- **Maior segurança**: Respostas rápidas em emergências, reduzindo riscos aos ocupantes.
- **Sustentabilidade**: Promoção de práticas mais ecológicas no uso de energia.


