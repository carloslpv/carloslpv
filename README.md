<div align="center">

# Oi, eu sou o Carlos

**Engenheiro de Computação · Desenvolvedor de software · Professor**

Joaçaba, Santa Catarina

[![Site](https://img.shields.io/badge/carlosvieira.eng.br-0D1B2A?style=flat-square&logo=googlechrome&logoColor=F59E0B)](https://carlosvieira.eng.br)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square)](https://www.linkedin.com/in/carloslpv/)
[![E-mail](https://img.shields.io/badge/carloscelpv@outlook.com-0078D4?style=flat-square&logo=minutemailer&logoColor=white)](mailto:carloscelpv@outlook.com)

</div>

---

Sou engenheiro de computação e trabalho há quase três anos com desenvolvimento backend em Java. Hoje faço parte do time que mantém o sistema acadêmico da Unoesc, aquele que cuida de matrícula, financeiro, diplomas e de toda a integração com outros sistemas. Boa parte do meu trabalho recente tem sido tirar pedaços de um sistema antigo e transformá-los em serviços menores com Spring Boot, além de revisar código e ajudar quem está chegando no time.

Antes de programar em tempo integral, passei pelo lado físico da tecnologia: redes, data center e equipamentos industriais em uma indústria de alimentos. Na faculdade, o que mais me prendeu foi a parte de baixo nível: microcontroladores, firmware em C e CLPs. Esse interesse continua, e os projetos de que mais gosto são aqueles em que o dado nasce num sensor e termina num sistema que alguém usa de verdade.

Também dou aula de Comunicação de Dados e Aplicações Distribuídas no curso de Engenharia de Computação da Unoesc.

## No que estou trabalhando

### [machine-telemetry](https://github.com/carloslpv/machine-telemetry)

Telemetria de máquinas industriais, do CLP ao OEE. Um gateway de borda lê o CLP que a máquina já tem, por OPC UA ou S7, e envia por MQTT ou, onde não há rede, por LoRaWAN. A plataforma guarda o histórico de estados e mostra quanto tempo a máquina parou e por quê, quanto produziu e qual o OEE. É a continuação do meu TCC, que testou essa arquitetura com um S7-1200, um Raspberry Pi e uma TV Box.

<p align="center">
  <img src="https://raw.githubusercontent.com/carloslpv/machine-telemetry/main/docs/img/dashboard.png" alt="Painel do machine-telemetry no Grafana com estado da máquina, OEE, linha do tempo de estados, produção por hora e paradas por causa" width="720">
</p>

| Parte | O que tem lá |
| --- | --- |
| [gateway](https://github.com/carloslpv/machine-telemetry/tree/main/gateway) | Gateway de borda em Java 25: OPC UA, cliente S7, fila local em SQLite, MQTT e modem LoRaWAN por comandos AT |
| [platform](https://github.com/carloslpv/machine-telemetry/tree/main/platform) | Spring Boot 4 e PostgreSQL: ingestão MQTT e The Things Network, paradas e OEE |
| [plc-sim](https://github.com/carloslpv/machine-telemetry/tree/main/plc-sim) | S7-1200 simulado em Python, para rodar a demonstração sem hardware |
| [comissionamento](https://github.com/carloslpv/machine-telemetry/blob/main/docs/comissionamento.md) | Passo a passo para ligar numa máquina de verdade, do TIA Portal à TTN |

### [cold-monitor](https://github.com/carloslpv/cold-monitor-infra)

Monitoramento de temperatura para geladeiras, freezers e câmaras frias. Os sensores enviam leituras, um painel mostra tudo ao vivo e o sistema avisa no Telegram quando a temperatura sai da faixa ou quando um sensor para de responder. As leituras podem vir de um simulador ou de um ESP32 com sondas DS18B20, que envia por MQTT sem perder dados quando o Wi-Fi cai.

<p align="center">
  <img src="https://raw.githubusercontent.com/carloslpv/cold-monitor-infra/main/docs/screenshots/dashboard-live.gif" alt="Painel do cold-monitor recebendo leituras ao vivo" width="720">
</p>

| Repositório | O que tem lá |
| --- | --- |
| [cold-monitor-infra](https://github.com/carloslpv/cold-monitor-infra) | Por onde começar: arquitetura, decisões técnicas e o Docker Compose que sobe tudo |
| [cold-monitor-backend](https://github.com/carloslpv/cold-monitor-backend) | API em Java 25 e Spring Boot 4, PostgreSQL, atualização em tempo real (SSE) e alertas |
| [cold-monitor-dashboard](https://github.com/carloslpv/cold-monitor-dashboard) | Painel em React e TypeScript com gráficos ao vivo |
| [cold-monitor-simulator](https://github.com/carloslpv/cold-monitor-simulator) | Simulador de sensores, com uma virtual thread por equipamento |
| [cold-monitor-edge](https://github.com/carloslpv/cold-monitor-edge) | Firmware do ESP32 em C (ESP-IDF), MQTT e a ponte para o backend |

Os READMEs estão em português e inglês e explicam o porquê de cada escolha.

## Com o que eu trabalho

**No dia a dia**

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![Hibernate](https://img.shields.io/badge/Hibernate%20%2F%20JPA-59666C?style=flat-square&logo=hibernate&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab_CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)

**Em projetos próprios**

![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![nginx](https://img.shields.io/badge/nginx-009639?style=flat-square&logo=nginx&logoColor=white)

**Embarcados e automação**

![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![ESP32](https://img.shields.io/badge/ESP32-E7352C?style=flat-square&logo=espressif&logoColor=white)
![STM32](https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00878F?style=flat-square&logo=arduino&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=mqtt&logoColor=white)
![LoRaWAN](https://img.shields.io/badge/LoRaWAN-1A1A1A?style=flat-square)
![OPC UA](https://img.shields.io/badge/OPC_UA-1A1A1A?style=flat-square)
![CLP Siemens](https://img.shields.io/badge/CLP_Siemens-009999?style=flat-square&logo=siemens&logoColor=white)

## Um pouco mais

- Pós-graduado em Indústria 4.0 e Inteligência Artificial pela Unoesc (2025).
- Publiquei no XXXVII Congresso de Iniciação Científica do INATEL (2025) um sistema de monitoramento em nuvem de CLP para IIoT, com OPC UA, Profinet e LoRaWAN. Ele virou o [machine-telemetry](https://github.com/carloslpv/machine-telemetry).
- No trabalho, montei o agente de IA da instituição com Spring AI e Ollama.

## Vamos conversar
O jeito mais fácil de me encontrar é pelo [site](https://carlosvieira.eng.br) ou pelo [LinkedIn](https://www.linkedin.com/in/carloslpv/).
