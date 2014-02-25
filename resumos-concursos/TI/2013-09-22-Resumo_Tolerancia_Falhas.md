---
layout: post
title: Resumo: Tolerancia a Falhas
category: concursos
tags: [TI, tolerancia_falhas]
---



# Resumo: Tolerancia a Falhas



-----
# Definição

_Tolerancia a falhas_ é a habilidade de um sistema de lidar com partes que não estão funcionando corretamente. Uma falha em um sistema é algum desvio do comportamento esperado: um malfuncionamento.

_Tolerancia a falhas_ também está relacionada com **alta disponibilidade**. Um sistema tolerante a falhas tem a capacidade de continuar disponível independentemente de uma falha de hardware ou software.

Ao projetar um sistema tolerante a falhas é necessário ter em mente que 100% de disponibilidade nunca pode ser alcançado. Além disso, quanto mais tentamos nos aproximar de 100%, mais caro se tornará o sistema.

No cálculo da disponibilidade de um sistema normalmente leva-se em conta somente as **paradas não **planejadas**, pois são as que queremos evitar. No entanto, esses cálculos deveriam considerar também as **paradas planejadas**. Por isso, ao adotar uma solução, preste atenção na quantidade de paradas planejadas que o produto exige para manutenção. Quanto menos paradas, melhor a solução.


-----
# Abordagens para lidar com falhas

Há basicamente três abordagens:

* Evitar a falha: processo de projeto e validação do sistema para assegurar que o sistema é tão livre de falhas quanto possível.
* Remoção de falha: ato de corrigir um defeito no sistema.
* Tolerancia a falha: parte da percepção de que falhas sempre ocorrem: nenhum sistema é totalmente livre de falhas. Isso posto, o sistema deve ter a capacidade de "compensar" as falhas e manter seu funcionamento. A abordagem geral para a construção de sistemas tolerantes a falhas é a **redundância**.

-----
# Tipos de redundância

## Redundância de informação

Provê tolerância a falha usando replicação de dados ou códigos de correção de erro.

### Exemplos:

1. ECCs: um exemplo simples de detecção de erro é o uso de **bit de paridade**: bit extra que indica se a unidade possui um número par ou ímpar de 1s.
2. RAID: significa _Arranjo Redundante de Discos Independentes_. Existem vários níveis de RAID:
    * RAID 0: espalha os dados entre discos diferentes. Não oferece tolerância a falhas, seu objetivo principal é fornecer ganho de performance (dados podem ser escritos ou lidos concorrentemente).
    * RAID 1: realiza espelhamento de discos, isto é, dados são gravados simultaneamente em dois discos. Se um disco pára de funcionar, o outro contém todos os dados desejados. RAID 1 é um exemplo de abordagem **ativo-ativo**, ao contrário de abordagens **ativo-passivo**, nas quais somente um dos elementos redundantes está em uso em um dado momento.
    * FALAR SOBRE OUTROS TIPOS DE RAID

## Redundância de tempo

Busca contornar malfuncionamentos do sistema realizando uma mesma operação uma série de vezes.

### Exemplos:

1. Retransmissão de pacotes empregada no protocolo TCP/IP: ao enviar um pacote, o protocolo TCP/IP dispara um contador. Se em um dado intervalo de tempo o remetente não receber um pacote confirmando que o destinatário recebeu o dado enviado, esse dado é re-enviado.


## Redundância física

Adiciona equipamento extra para possibilitar ao sistema tolerar a falha de um componente de _hardware_.

### Exemplos:

1. RAID


-----
# Diferença entre replicação de redundância

Na **replicação** nós temos várias unidades operacionais funcionando simultâneamente e um sistema de votação para eleger o resultado de uma operação. Na **redundância**, por outro lado, somente uma unidade está em funcionamento e a unidade redundante fica em estado de espera para o caso de a unidade em funcionamento falhar.


-----
# Técnicas para tolerancia a falhas


## IP Takeover

Quando uma máquina sai do ar, uma segunda máquina assume seu endereço IP. Caso a máquina ainda esteja no ar mas um de seus serviços esteja fora, é necessário provocar uma parada total na máquina para que a substituta assuma o lugar da defeituosa.


## DNS Rotativo

Consiste em atribuir mais de um endereço IP a um mesmo nome de máquina. O DNS irá responder de forma circular às requisições àquele nome de máquina, ora direcionando a requisição a um IP, ora a outro. Isso balanceia o tráfego entre as máquinas.


## Link de Conexão Dedicado

Contratação de links dedicados de provedores de Internet diferentes. Isso possibilita alta disponibilidade no acesso aos sistemas de uma organização.

## Backup Primário (Active-Standby)

Com a abordagem de _backup primário_, o servidor primário faz o trabalho todo, quando ele falha, o servidor backup entra em cena. Para descobrir se o servidor primário está funcionando, o servidor backup pode enviar "pings" periódicos. Se o servidor primário falhar em responder, então o servidor backup pode assumir as funções do principal.


### Application Failover


#### Cold Failover

Requer reinicialização da aplicação na máquina backup. Quando a máquina backup assume o trabalho da defeituosa, todos os aplicativos devem ser inicializados naquela máquina. O trabalho feito na máquina defeituosa é perdido.


#### Warm Failover

A aplicação salva os dados periodicamente na máquina backup, usando um sistema de _check-points_. Quando a máquina defeituosa entra em cena, ela consegue reiniciar a aplicação no último _check-point_. Essa técnica é similar aos "Pontos de restauração do sistema" no Windows.


#### Hot Failover

Aplicações da máquina principal são executadas simultaneamente na backup. Quando a máquina backup assume o lugar da principal, a aplicação é reiniciada exatamente no ponto onde a máquina falhou. Se a falha é de software, há chances de que a máquina backup tenha passado pelo mesmo problema que a principal, uma vez que elas executam a mesma aplicação, com as mesmas entradas.

