# FarmTech Solutions - Fase 2

## Descrição do projeto
Este projeto simula um sistema de irrigação inteligente utilizando ESP32 na plataforma Wokwi. O objetivo é automatizar a irrigação de uma lavoura com base em leituras de sensores simulados.

## Componentes utilizados
- ESP32
- Sensor DHT22 (simulando a umidade do solo)
- Sensor LDR (simulando o pH do solo)
- 3 botões para simular os nutrientes N, P e K
- Relé azul para simular a bomba d’água

## Equivalência dos sensores
Como o Wokwi não possui sensores agrícolas específicos, foram utilizadas substituições didáticas:
- Botão 1 = Nitrogênio (N)
- Botão 2 = Fósforo (P)
- Botão 3 = Potássio (K)
- LDR = pH do solo
- DHT22 = umidade do solo
- Relé = bomba de irrigação

## Lógica de funcionamento
A irrigação é ligada quando todas as condições abaixo são satisfeitas:
- a umidade do solo está menor ou igual a 40%
- pelo menos 2 dos 3 nutrientes estão ativos
- o valor analógico do LDR está entre 1000 e 3000

Caso qualquer uma dessas condições não seja atendida, a irrigação permanece desligada.

## Pinos utilizados
- DHT22 = GPIO 23
- Botão N = GPIO 32
- Botão P = GPIO 33
- Botão K = GPIO 25
- LDR = GPIO 34
- Relé = GPIO 26