
# Global solution - EDGE
Projeto de simulação indicador de poluição marinha



## Participantes

```http 
- Beatriz Vieira de Novais        | rm554746
- Mariana Neugebauer Dourado      | rm550494
```






## Informações sobre o projeto
Informações sobre alguns componentes usados na criação do projeto:

- Protoboard - sendo uma placa de circuito impresso (PCB) que permite a montagem temporária de circuitos eletrônicos. Ela é composta por uma matriz de furos condutores interligados internamente por trilhas condutoras, onde os componentes eletrônicos podem ser inseridos e conectados de forma rápida e sem a necessidade de solda.
- LED - é um componente eletrônico que emite luz quando uma corrente elétrica passa por ele.
- LDR - um resistor dependente de luz. Uma característica é que a resistência dele irá variar de acordo com a quantidade de luz;
- Resistor - sua função é de limitar o fluxo de corrente elétrica em um circuito. Eles podem ser usados para várias coisas, uma delas em exemplo: é limitar a corrente que passa por um LED para evitar danos;
- LCD - é uma tecnologia de tela que utiliza cristais líquidos e polarizadores de luz para transmitir imagens.
- TMP36 (sensor de temperatura) - é um sensor utilizado para medir a temperatura. É sensível a temperaturas na faixa entre -40°C até +125°C com precisão de ± 2ºC.
- Potenciômetro -  é um tipo de resistor ajustável, ou seja, um componentes cuja resistência elétrica pode ser regulada manualmente.
- Sensor ultrassônico - é usado para medir a distância entre objetos, e também pode ser usado para detectar objetos em movimento. 
- Jumpers - são cabos utilizados para fazer conexões entre os diversos componentes do circuito;


## Bibliotecas utilizadas
Dependências do projeto:

Só utilizamos uma biblioteca para incluir o LCD

<Adafruit_LiquidCrystal.h>

## Passo a Passo
Para você conseguir fazer esse projeto, você vai precisar desses componentes:

- 1 arduino uno;
- 1 Fotoresistores (LDR);
- 3 LEDS;
- 4 Resistores;
- 1 Protoboard;
- Vários jumpers;
- 1 TMP36;
- 1 Potenciômetro;
- 1 LCD;
- 1 Sensor ultrassônico.

Após você conseguir todos os matériais, você pode agora seguir os passos à passos.

1. montagem:

- Conecte dois leds, o potenciômetro e o TMP36, além disso conecte dois resistores alinhados com a perna negativa dos leds conectados a protoboard e conecte um resistor de forma horizontal a protoboard.
- Posicione o LDR e um led um frente ao o outro (não precisam estar conectados a protoboard);
- Conecte a perna negativa do LDR a uma perna do led conectado horizontalmente na protoboard;

2. produzindo conexão:
Todas as conexões foram feitas com auxílio dos jumpers

Conexões negativas:

- conecte o GND da placa arduino com a linha negativa da Protoboard e faça a mesma coisa com a parte positiva;
- Conecte a perna negativa do TMP36 a linha negativa da protoboard;
- Conecte a perna negativa do potenciômetro a linha negativa da protoboard;
- Conecte a perna negativa do LCD a linha negativa da protoboard;
- Conecte a perna negativa do TMP36 a linha negativa da protoboard;
- Conecte uma perna do resistor a linha negativa da protoboard e a outra perna deve ser conectada na linha do led na protoboard (isso serve para os dois leds);
- Conecte a outra perna do resistor conectado horinzontalmente a linha negativa da protoboard;
- Conecte a perna negativa do led alinhado ao LDR na linha negativa da protoboard;

Conexões positivas: 

- Conecte a perna positiva do LDR na linha positiva da Protoboard;
- Conecte a perna positiva do potenciômetro na linha positiva da Protoboard;
- Conecte a perna positiva do sensor ultrassônico na linha positiva da Protoboard;
- Conecte a perna positiva do TMP36 na linha positiva da Protoboard;
- Conecte a perna positiva do LCD na linha positiva da Protoboard;

Conexões portas:

Portas digitais:

- Conecte o pino trig do sensor ultrassônico a porta 8 do arduino;
- Conecte o pino echo do sensor ultrassônico a porta 7 do arduino;
- Conecte a perna positiva do led alinhado ao LDR a porta 6 do arduino;
- Conecte a perna positiva de um dos leds a porta 5 do arduino;
- Conecte a perna positiva do outro led a porta 4 do arduino;

Portas analógicas:

- Conecte a última perna do potenciômetro a porta A0 do arduino;
- Conecte a última perna do TMP36 a porta A1 do arduino;
- Conecte uma perna do resistor horizontal a porta A2 do arduino (a perna que está conectada somente no LDR);
- Conecte a perna SDA do LCD a porta A4 do arduino;
- Conecte a perna SCl do LCD a porta A5 do arduino;





## Explicação de como funciona o  projeto
Esse projeto simula um detector de poluição marinha (com os componentes disponíveis nos simuladores gratuitos).
## Link do projeto (modo simulação)

```http 
Link códiigo da simulação (tinkercad)
https://www.tinkercad.com/things/bQsZS2pOvRq-gs-ecomares

```

