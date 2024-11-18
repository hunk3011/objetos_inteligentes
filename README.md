# Edifícios Inteligentes para Economia de Energia

Este repositório contém o código e a documentação do projeto de um sistema de automação inteligente desenvolvido com a plataforma Arduino, que tem como objetivo integrar eficiência energética e segurança contra incêndios. O sistema é projetado para ser implementado em ambientes comerciais e residenciais, criando soluções que não apenas aumentam a sustentabilidade do edifício, mas também melhoram a segurança dos ocupantes.

A principal funcionalidade do sistema é a detecção precoce de incêndios utilizando sensores especializados, como o Sensor de Chama/Fogo KY-026, que detecta a radiação infravermelha emitida pelas chamas. Quando um incêndio é detectado, o sistema aciona alertas visuais e sonoros, além de enviar notificações via Internet das Coisas (IoT), possibilitando o monitoramento remoto e respostas rápidas. Isso proporciona maior segurança para os moradores e trabalhadores no ambiente, reduzindo riscos e danos em caso de emergência.

Além disso, o sistema também é projetado para otimizar o consumo de energia, ajustando automaticamente as condições de iluminação, climatização e outros recursos elétricos com base nas condições do ambiente. Utilizando a conectividade Wi-Fi da placa ESP8266 NodeMCU V3, o projeto é capaz de integrar todos os sensores e atuadores em uma rede inteligente, permitindo que os dispositivos se comuniquem entre si e com os usuários de forma centralizada. Isso contribui diretamente para a redução de custos com energia elétrica e a sustentabilidade ambiental, tornando o projeto uma solução moderna e eficaz para edifícios inteligentes.

A combinação de tecnologias de IoT com automação residencial e comercial é um avanço significativo para a criação de ambientes mais sustentáveis, seguros e conectados. Através da integração com plataformas de gerenciamento e aplicativos móveis, o sistema oferece um controle remoto eficiente e prático, podendo ser adaptado para diferentes cenários e necessidades. Assim, o projeto não só visa aprimorar a eficiência no uso de energia, mas também a segurança e o conforto dos ocupantes, tornando os espaços mais inteligentes e preparados para responder a emergências de forma rápida e eficaz.

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


