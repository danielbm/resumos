# Resumo: Sistemas Distribuídos

## Introdução

Um sistema distribuído é uma **coleção de processadores** que **não compartilham memória ou clock**. Nesse tipo de sistema cada nodo tem sua **própria memória local** e os nodos se comunicam uns com os outros através da rede.

Uma outra definição diz que um sistema distribuído é uma **coleção de nodos fracamente acoplados**, interconectados pela rede.

## Vantagens de Sistemas Distribuídos

um sistema distribuído é uma coleção de nodos fracamente acoplados. Do ponto de vista de um nodo específico em um sistema distribuído, o resto dos nodos e seus respectivos recursos são remotos, enquanto os recursos do nodo em questão são locais.

Há quatro vantagens principais para a construção de sistemas distribuídos:

  - compartilhamento de recursos;
  - aumento de performance nas computações;
  - confiabilidade;
  - comunicação.

## Tipos de Sistemas Operacionais Baseados em Rede

### Sistema Operacional de Rede

Um sistema operacional de rede provê um ambiente no qual **usuários**, que estão **conscientes da multiplicidade de máquinas**, podem acessar recursos remotos por meio de login remoto ou de algum mecanismo de transferência de dados das máquinas remotas para sua própria máquina.


### Sistemas Operacionais Distribuídos

Em um sistema operacional distribuído, **usuários podem acessar recursos remotos da mesma maneira que eles acessam recursos locais**. Migração de dados e processos de um lugar para outro é responsabilidade do sistema operacional distribuído.

#### Migração de Dados

Há duas abordagens para tranferência de dados em um sistema distribuído. A primeira é transferir o arquivo todo para o computador do usuário, e, após ele fazer as modificações necessárias, o arquivo é enviado novamente para o computador remoto. A segunda abordagem é transferir somente partes do arquivo (aquelas necessárias para o usuário no momento), e, caso mais partes do arquivo sejam necessárias, novas tranferências serão realizadas. O NFS e o CIFS usam essa abordagem.


#### Migração de Computação

Em algumas circustâncias o usuário quer transferir computação em vez de dados. Suponha que há vários arquivos grandes em diferentes nodos e desejemos calcular o hash desses arquivos. Seria mais eficiente transferir a tarefa de computar o hash para os nodos do que transferir os arquivos para um nodo e então computar o hash. Sistemas distribuídos usam mensagens para transferir computação (na verdade, eles usam mensagens para comunicação em geral). Mais especificamente, sistemas distribuídos usam RPC para solicitar que alguma computação seja realizada nos nodos do sistema.

## Referências: Operating Systems Concepts - Silberschatz - Fourth Edition
