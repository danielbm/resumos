---
layout: post
title: Resumo: Clusters
category: concursos
tags: [TI, clusters]
---


# Resumo: Clusters



# Introdução
-----

Se queremos disponibilidade em um sistema de computação, a solução geralmente é usar componentes confiáveis (uma boa fonte de alimentação, por exemplo) e incorporar a esse sistemas elementos para tolerância a falhas. Em um nível mais sério, usaríamos fontes de alimentação hot-swappable, memórias com correção de erro, etc.


# Clusters
-----

O objetivo dos clusters é alcançar disponibilidade e escalabilidade usando multiplos sistemas de computação independentes conectados. Um cluster é uma coleção de computadores em uma configuração tal que eles operem com se fossem uma única máquina.


## Tipos de Cluster
-----

## Cluster para Computação de Alta Performance

Computação de Alta Performance (HPC) é uma tentativa de agregar poder de computação de vários computadores para prover uma solução. Existem algumas variações:

- Supercomputação: usa supercomputadores. Geralmente usados para aplicações numérico-científicas. Comunicação entre processadores é necessária.
- Balanceamento de carga: necessita de comunicação via rede para saber para onde enviar as tarefas a serem realizadas. Provê tolerância a falha.
- Processamento em lotes (batch processing): ambientes não interativos nos quais é possível submeter uma série de tarefas e obter os resultados posteriormente. Essas tarefas tendem a requerer muito processamento por parte da CPU e executarem por um longo tempo.


# Clusters de Alta Disponibilidade
-----

Com clusters, gostaríamos de ter uma solução que tem alta disponibilidade usando computadores convencionais. Além disso, Uma falha em um servidor não deve prejudicar os demais, a carga de trabalho deve ser dividida entre os nós restantes do cluster. Isso possibilita que uma máquina seja tirada do ar para manutenção sem interromper o funcionamento do sistema como um todo.

Para construir esse tipo de sistema, precisamos de software que possa detectar quando uma máquina pára de funcionar ou quando uma aplicação sai do ar. Um assunto importante nesse sentido é o _failover_. Soluções podem empregar um dentre os três tipos de failover: **hot failover, warm failover, ** ou **cold failover**.


# Clusters de Balanceamento de Carga
-----

Uma característica marcante dos clusters de balanceamento de carga é o fato de eles geralmente executarem multiplas instâncias de uma mesma aplicação (um servidor web, por exemplo).

Uma das principais estratégias para se alcançar balanceamento de carga em um sistema é o uso do código de erro REDIRECT do protocolo HTTP. Com isso, um cliente faz uma requisição a um servidor proxy, que então seleciona uma das máquinas disponíveis no cluster e envia a requisição a ela.

Outra solução é o uso de roteadores especiais (como os da série Cisco LocalDirector).









