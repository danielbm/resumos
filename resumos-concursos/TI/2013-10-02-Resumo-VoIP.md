---
layout: post
title: Resumo: VoIP
category: concursos
tags: [TI, VoIP]
---


# Resumo: VoIP


# Introdução
---

VoIP (Voice over Internet Protocol) é um método para converter sinais analógicos de audio em sinais digitais e transmiti-los através da Internet.


## Benefícios da Tecnologia VoIP

- Integração de voz e dados;
- Redução de custos;

Os fatores acima são os dois principais.

# Qualidade de Voz

Os seguinte fatores determinam qualidade de voz nas transmissões VoIP:

- Uso de um Codec de qualidade: o recomendado é o G.711
- Cancelamento de echo;
- Redução do delay:
    - Delay total da transmissão;
    - Jitter Delay.



## Consumo de Banda

Uma chamada telefonica de qualidade requer pelo menos uma taxa de transmissão de 64Kbps. Esse valor é muito alto. Mas técnicas de compressão como as usadas no G.729 reduzem essa taxa para cerca de 8Kbps. O overhead do roteador é cerca de 7Kbps, totalizando 15Kbps. Entretanto, há várias pausas durante a conversação, assim é usada uma tecnologia de **supressão de silêncio**. Com isso, chamadas requerem apenas cerca de 6Kbps.


## TCP x UDP

Para evitar a tentativa do TCP/IP de retransmitir pacotes corrompidos, normalmente usa-se UDP em VoIP. Mas para transferências de Fax o TCP pode ser uma opção melhor porque caso haja perda de pacotes durante a negociação da página a conexão pode ser terminada.



# Serviços VoIP
---

## PC to Phone

Requer um gateway no lado do receptor para converter os pacotes IP de volta para sinal analógico.

## PC to PC

Pode ser provido sem o uso de gateways. Usa software para fazer as chamadas.

## Phone to Phone

Algumas companhias proveem esse serviço e cobram taxas menores que as de telefonia convencionais.


# H.323
---

## Componentes

1. Terminais: são os clientes, os endpoints da comunicação.
2. Gateways: realizam a função de tradutor, isto é, traduzem diferentes formatos de transmissão (H.225 para H.221, por exemplo).
3. Gatekeepers: componente vital do sistema H.323. Realiza a função de gerente de conexões e chamadas. É o ponto central para chamadas dentro de sua zona (zona é a junção de um gatekeeper e dos endpoints registrados nele).
4. Multipoint Control Units (MCU): provê a capacidade de três ou mais terminais e gateways participarem em uma conferência multipoint. O MCU consiste de um Controlador Multipoint (MC), que é obrigatório, e um Processador Multipoint (MP), que é opcional.

## Protocolos

Os protocolos usados no H.323 são:

  - H.225 Registration, Admission and Status (RAS): é usado entre um endpoint H.323 e um Gatekeeper para prover resolução de endereço e serviços de controle de admissão.
  - H.225 Call Signalig: é usado entre duas entidades H.323 para estabelecer comunicação entre elas.
  - H.245: descreve mensagens e procedimentos para abertura de canais lógicos para áudio, vídeo e dados.
  - Real-time Transport Protocol (RTP): é usado para o envio e recebimento de informação multimídia entre duas entidades H.323. O RTP, apesar de poder usar TCP, usa UDP, pois valoriza mais a velocidade na comunicação do que a confiabilidade.


# SIP
---

É um protocolo da camada de aplicação do modelo OSI, usado para criar, modificar e terminar sessões com um ou mais participantes. A arquitetura do SIP é similar à do HTTP. Requisiões são enviadas pelos clientes, processadas e respondidas pelo servidor. Uma requisição e as respostas a ela formam uma transação.


## Componentes

- User agents: sistema fim agindo em favor do usuário. Consiste de duas partes: clientes (User Agent Client - UAC) e servidores (User Agent Server - UAS). 
- Servidores de rede: há três tipos de servidores em uma rede:
    - Servidor de registro: recebe informações sobre a localização dos usuários;
    - Servidor proxy: recebe requisições e as encaminha para o próximo hop, que possui mais informações sobre a parte que está sendo contactada;
    - Servidor de redirecionamento: recebe a requisição, determina o endereço do próximo hop, e retorna esse endereço, em vez de encaminhar a requisição.

## Comandos SIP

- INVITE: usado para convidar um usuário para uma ligaçnao.
- BYE: termina a conexão entre dois endpoints.
- ACK: confirmação de recebimento de mensagens de convite.
- OPTIONS: requisita informações sobre as características de uma ligação.
- REGISTER: prove informação sobre a localização de um usuário para o servidor SIP.
- CANCEL: encerra a pesquisa por um usuário.


# Comparação de SIP e H.323

H.323:

- Complexo
- Representação binária das mensagens
- Requer plena compatibilidade reversa
- Não é muito modular
- Não é muito escalável
- Sinalização complexa
- Grande fatia de mercado
- Centenas de elementos
- Detecção de loop é difícil

SIP:

- Comparativamente simples
- Representação textual das mensagens
- Não requer plena compatibilidade reversa
- Bastante modular
- Altamente escalável
- Sinalização simples
- Promovido pela IETF
- Somente 37 cabeçalhos
- Detecção de loops é simples



# RTP (Real-time Transport Protocol)
---

RTP suporta a transferência de mídia (audio e video) em tempo real usando. Este protocolo é usando tanto pelo H.323 quanto pelo SIP. O protocolo de transporte precisa permitir ao receptor detectar perdas em pacotes além de prover informação de tempo sobre os pacotes. O cabeçalho RTP contém informação que especifica como os fluxos de bits do codec devem ser quebrados em pacotes. O RTP não reserva recursos na rede, em vez disso ele provê informação para que o receptor possa recuperar o pacote em caso de perda e jitter.

As principais funções providas por esse protocolo são:

- Sequenciamento;
- Identificação (do tipo de mídia) no Payload;
- Identificação (de início e fim) no frame;
- Timestamps dos pacotes.


# RTCP (Real-time Control Protocol)
---

RTCP é um protocolo de controle e funciona em conjunto com o RTP. Em uma sessão RTP, os participantes enviam periodicamente pacotes RTCP para obter informação sobre QoS e fatores relacionados. Além disso, o RTCP provê alguns serviços adicionais:

- QoS Feedback: o RTCP é usado para reportar a qualidade do serviço (número de pacotes perdidos, jitter, etc);
- Controle de sessão: usa o pacote BYE para sinalizar o fim da conexão;
- Identificação: informações como endereço de email, nome e telefone são incluídas nos pacotes;
- Sincronização: informação extra para sincronizar os fluxos de dados.

