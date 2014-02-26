---
layout: post
title: Resumo: Storage
category: concursos
tags: [TI, storage]
---


# Resumo: Storage



# Directly Attached Storage (DAS)
---

Uma DAS é um sistema de armazenamento que é diretamente conectado ao servidor ou estação de trabalho. Ela pode ser um disco rígido de um computador ou uma estante com multiplos discos. Ao contrário de discos rígidos locais, estantes de discos requerem gerenciamento extra.


# SAN (Storage Area Network)
---

Diferentemente do DAS, uma SAN é uma rede separada e dedicada a dispositivos de armazenamento. Uma SAN consiste em um arranjo de discos que oferecem espaço compartilhado de armazenamento e que pode ser acessado por muitos servidores ou sistemas.

Outra definição diz que SAN são dois ou mais dispositivos se comunicando via protocolo serial SCSI, tal como Fibre Channel ou iSCSI. Segundo essa definição, uma LAN que trafega nada mais do que tráfego de storage não pode ser considerada uma SAN. O que diferencia uma LAN de uma SAN (ou de uma NAS) é o protocolo que é usado. Assim, se o tráfego de storage trafega em uma LAN através do protocolo iSCSI, então essa LAN pode ser considerada uma SAN. Entretanto, simplesmente enviar dados de backup através de uma LAN dedicada não a torna uma SAN. Enfim, uma SAN é uma rede que usa um protocolo serial SCSI para transferir dados.

## Hardware para SAN

- Servidor de Disco;
- Switches fiber channel;
- HBA (Host Bus Adapter).

## Topologias de SAN

As SANs atuais são todas construídas em uma topologia física de estrela. Um switch é conectado ao storage e neles conectamos todos os outros servidores da rede. A exceção fica com a ligação ponto-a-ponto (os servidores são ligados diretamente ao storage, sem nenhum equipamento intermediário).

- Ligação ponto-a-ponto: os servidores são ligados diretamente ao storage, sem nenhum equipamento intermediário.
- Loops ou anéis: Fibre Channel Arbitrated Loop (FC-AL). É similar ao uma rede token-ring.
- Malha (Switched Fabric ou Fabric): Nesta topologia utiliza-se switches Fibre Channel, o que permite um grande número e dispositivos interconectados. Dedica largura de banda integral a cada uma das portas e ermite transferências de dados simultaneamente para um único nó. É a topologia que permite mais escalabilidade e crescimento. Teoricamente, pode conter mais de 7,7 milhões de nós.



# NAS (Network Attached Storage) 
---

Comumente confundido com o SAN, o NAS é uma forma de armazenamento baseada em redes comuns (ou LAN) e acessível a todos os dispositivos ligados à LAN. Os protocolos de acesso a arquivos mais utilizados nos NAS são o NFS (Network File System) e o CIFS (Common Internet File System). Para acessar os arquivos normalmente é exigida alguma autenticação do usuário. Os grandes benefícios do NAS são a fácil instalação e grande capacidade.

(Network Attached Storage) é um computador dedicado a compartilhamento de arquivos através de NFS (Network File System, usado no Linux), CIFS (Common Internet File System, usado no Windows) ou DAFS(Direct Access Files). Cabe ressaltar que é um dispositivo dedicado exclusivamente ao compartilhamento de arquivos, centralizando a responsabilidade de servir os arquivos em uma rede e desse modo libera recursos de outros servidores.


# SAN x NAS
---

- Protocolo:
    – SAN: Serial SCSI-3
    – NAS: TCP/IP, NFS/CIFS
- Compartilhamento:
    – SAN: Drives de discos e fitas 
    – NAS: Sistemas de arquivos
- Permite:
    – SAN: Diferentes servidores acessarem o mesmo drive de disco ou fita de forma transparente para o usuário final.
    – NAS: Diferentes usuários acessarem o mesmo sistema de arquivos ou até um mesmo arquivo.
- Substitui:
    – SAN: Os drivers de discos e fitas locais, ou seja, drivers conectados diretamente ao servidor. Com SAN, centenas de sistemas podem compartilhar o mesmo drive de disco ou fita.
    – NAS: Servidores Unix NFS e servidores NT CIFS que possibilitavam sistemas de arquivos compartilhados em rede.
- Aplicações:
    – SAN: Processamento de aplicações de banco de dados de missão crítica; Backup de dados centralizado; Operações de recuperação de desastres; Consolidação de armazenamento.
    – NAS: Compartilhamento de arquivo em NFS e CIFS; Transferência de pequenos blocos de dados a longas distâncias; Acesso ao banco de dados limitado somente a leitura.
- Vantagens:
    – SAN: Alta disponibilidade; Confiabilidade na transferência de dados; Trafego reduzido na rede primaria; Flexibilidade de configuração; Alto desempenho; Alta escalabilidade; Gerenciamento centralizado; Oferta de múltiplos fornecedores.
    – NAS: Poucas limitações de distancia; Adição simplificada da capacidade de compartilhamento de arquivo; Fácil instalação e manutenção.


# Fibre Channel
---

É a arquitetura mais utilizada para implementações de SANs. Trata-se de um padrão tecnológico alternativo à Ethernet, que permite a transferência de dados de um nó para outro nó da rede em velocidades extremamente altas. Implementações atuais podem atingir taxas de transferência de dados de 10Gbps ou mais, e alcançar distâncias de até 10 km quando a fibra ótica é utilizada como o meio físico.

Fibre Channel é um protocolo da camada de transporte do modelo ISO que predomimantemente transporta comandos SCSI em redes de fibra óptica. Apesar do nome, esse protocolo pode utilizar tanto cabos par-trançado quanto fibra óptica. Para que um dispositivo possa acessar uma rede Fibre Channel, é necessário implementar um Host Bus Adapter (HBA). Fibre Channel tem HBAs disponíveis para a maioria dos sistemas operacionais modernos. A identificação dos HBAs usa WWN (World Wide Name), um sistema similar aos endereços MAC de placas de rede.


## Fibre Channel Zoning

Fibre Channel zoning é o particionamento de uma rede Fibre Channel em conjuntos menores, para restringir interferência, aumentar segurança e simplificar gerenciamento. Pode ser usado somente com a topologia switched fabric (CF-SW). É parecido com a criação de VSANs, mas em zoning, cada porta do switch pode fazer parte de várias zonas. Pode ser implementado por hardware (especializado) ou por software.


# SCSI
---

Small Computer Systems Interface (Pequena Interface de Sistema de Computador) foi originalmente definido como uma interface paralela universal a nível de sistema para conectar vários dispositivos através de um único cabo, chamado barramento SCSI. O SCSI é um barramento de entradas e saídas locais pelo qual diferentes dispositivos e um ou mais controladores podem se comunicar e trocar informações independentemente do que o resto do sistema está fazendo. 


No SCSI, o número de dispositivos que podem ser conectados ao barramento e o número de barramentos conectados ao servidor determinam a quantidade de dados disponíveis para o servidor. Mas, apesar de até 15 dispositivos poderem ser conectados a um servidor por meio de um único barramento SCSI, na prática, por causa das limitações de desempenho devido à arbitrariedade, é comum conectar no máximo cinco dispositivos, assim limitando a escalabilidade.


# iSCSI
---

O protocolo iSCSI (Internet Small Computer System Interface) é um mapeamento do protocolo SCSI normal para usar o protocolo TCP/IP, mais comumente usando Gigabit Ethernet. Ao contrário do Fibre Channel, que requer cabeamento especial, iSCSI usa a infraestrutura de rede existente. Usa os termos "iniciador" para o cliente (consumidor dos dados) e "alvo" para o arranjo de discos. A segurança e autenticação é feita usando o protocolo CHAP.

# CIFS / SMB
---

O protocolo SMB (Server Message Block), também conhecido como CIFS (Common Internet File System) opera na camada de aplicação do modelo OSI (camada 7) usado principalmente para prover acesso compartilhado a impressoras, arquivos, e etc. Ele também prove mecanismos de intercomunicação entre processos, tudo isso com autenticação. O SMB adota uma abordagem cliente-servidor, em que um cliente faz uma requisição e o servidor responde apropriadamente.


# The Network File System (NFS)
---

O NFS é parecido com o SMB/CIFS no sentido de que ele também é um protocolo de camada 7 do modelo OSI. Em geral o NFS possui baixa complexidade quando comparado ao SMB: o NFS somente permite acesso a arquivos em uma rede Ethernet. No NFS, a inteligência fica no cliente. Além disso, no NFS o servidor não guarda estado das conexões. Isso acaba sendo uma vantagem caso o servidor fique fora de operação. Quando ele voltar a operar, os clientes somente precisam repetir a requisição.

NFS é mais frequentemente usado em ambientes Linux ou Unix, mas também está disponível para outras plataformas, como Windows (Windows Services for Unix / NFS Client or Server) ou Mac OS.

Inicialmente o NFS era baseado no UDP, por questões de performance, mas a partir da versão 3 foi adicionado suporte para conexões baseadas em TCP. Enquanto SMB/CIFS são centrados no usuário, ou seja, a autenticação acontece no nível do usuário, NFS (antes da versão 4, que inclui Kerberos) é centrado no sistema.

Um problema com as versões de NFS é que os dados trafegam pela rede na forma de texto simples, sem criptografia. Assim, é considerada uma boa prática usar NFS é redes consideradas seguras e isolar o tráfego a alguns switches específicos ou criar uma VLAN.


# Multipath I/O (MPIO)
---

Multipath I/O é uma técnica para tolerancia a falha e aumento de performance que usa componentes físicos redundantes (cables, switches, etc) para criar vários caminhos lógicos entre o servidor e os dispositivos de armazenamento. Caso um ou mais desses componentes falhe, o sistema multipath é capaz alternar o caminho de acesso aos dados, de forma que as aplicações continuem acessando os dados. Com esse mecanismo, o sistema consegue prover tolerancia a falhas e balanceamento de carga.

# Snapshots
---

Em sistemas de computação, um snapshot é o estado do sistema em um momento particular.

Uma abordagem para fazer backup de sistemas é desabilitar temporariamente acesso de escrita aos dados durante o backup. Isso é tolerável para sistemas com baixa disponibilidade (desktops, principalmente, ou pequenas redes, para as quais um pequeno downtime é aceitável). 

Sistemas 24/7, porém, não podem pagar um preço tão alto. Esses sistemas geralmente escolhem realizar backup fazendo um snapshot dos dados em um momento no tempo e permitir que as aplicações continuem a realizar escritas de dados. A maioria das implementações de snapshots permitem criar snapshots em O(1). Em muitos sistemas, uma vez criado um snapshot inicial, os subsequentes só copiam dados mudados desde o último snapshot.


# Storage Caching
---

Storage caching é usado para criar buffers de blocos de dados antes de realizar escritas no disco, para minimizar a utilização dos dispositivos de armazenamento e minimizar latência.


# Thin Provisioning
---

Thin provisioning é o ato de usar virtualização para dar a aparência de se ter mais recursos físicos do que existem realmente. Lembrar de memória virtual.

Thin provisioning é um esquema de armazenamento compartilhado, é um método para otimizar a utilização do espaço disponível. Ele usa alocação sob demanda dos blocos, em contraste ao método tradicional de alocar todos os blocos quando eles são criados. Essa metodologia elimina praticamente todos os espaços não alocados nos dispositivos de armazenamento, melhorando as taxas de utilização. No método tradicional de alocação, grandes porções de espaço são alocadas para servidores individuais mas não são usados (esse método é chamado "thick provisioning").

# Backup de Dados
---

Os backups podem ser classificados em quatro tipos:

## Backup Total 

Realiza uma cópia de todos os dados para a mídia, não importando o conteúdo do último backup. Ou seja, o atributo de arquivamento é desmarcado ou redefinido. Uma fita atualizada de backup total pode ser usada para restaurar um servidor completamente em um determinado momento.

## Backup Incremental

Salva os arquivos que foram alterados desde o último backup. Neste processo o novo arquivo é armazenado na mídia e o arquivo original não é removido da mídia. No processo de restauração devemos ter o último backup completo e dos os backups incrementais desde então.

## Backup Diferencial 

Copia todos os arquivos que foram alterados desde o último backup completo, por este motivo ocupa mais espaço nas mídias de backup e é mais lento de ser gerado, contudo é mais fácil de recuperá-lo. Para restaurar os dados a partir deste tipo de backup deve-se ter em mãos apenas o último backup completo e o último backup diferencial.

## Backup Delta

Só faz a cópia dos dados reais que foram modificados nos arquivos, é um processo de backup mais rápido e que ocupa menos espaço nas mídias de backup, contudo o processo de restauração é mais lento e complexo.


# RAID
---

O sistema RAID consiste em um conjunto de dois ou mais discos rígidos com dois objetivos básicos:

- tornar o sistema de disco mais rápido (isto é, acelerar o carregamento de dados do disco), através de uma técnica chamada divisão de dados (data striping ou RAID 0);
- tornar o sistema de disco mais seguro, através de uma técnica chamada espelhamento (mirroring ou RAID 1).

Essas duas técnicas podem ser usadas isoladamente ou em conjunto.


## RAID 0 (striping)

No striping, ou distribuição, os dados são subdivididos em segmentos consecutivos (stripes, ou faixas) que são escritos sequencialmente através de cada um dos discos de um array, ou conjunto.

Vantagens:

- acesso rápido as informações (até 50% mais rápido);
- custo baixo para expansão de memória.

Desvantagens:

- caso algum dos setores de algum dos HD’s venha a apresentar perda de informações, o mesmo arquivo que está dividido entre os mesmos setores dos demais HD’s não terão mais sentido existir, pois uma parte do arquivo foi corrompida, ou seja, caso algum disco falhe, não tem como recuperar;
- não é usada paridade.


## RAID 1 (Mirror)

RAID-1 é o nível de RAID que implementa o espelhamento de disco, também conhecido como mirror. Para esta implementação são necessários no mínimo dois discos. O funcionamento deste nível é simples: todos os dados são gravados em dois discos diferentes; se um disco falhar ou for removido, os dados preservados no outro disco permitem a não descontinuidade da operação do sistema.

Vantagens:

- caso algum setor de um dos discos venha a falhar, basta recuperar o setor defeituoso copiando os arquivos contidos do segundo disco;
- segurança nos dados (com relação a possíveis defeitos que possam ocorrer no HD).

Desvantagens:

- custo relativamente alto se comparado ao RAID 0;
- ocorre aumento no tempo de escrita;


## RAID 2

Usa ECC, mas um ECC complexo e confiável.


## RAID 3

RAID 2 simplificado. Usa paridade de bits.

## RAID 4 (Paridade)

O RAID 4 funciona com três ou mais discos iguais. Um dos discos guarda a paridade (uma forma de soma de segurança) da informação contida nos discos. Se algum dos discos avariar, a paridade pode ser imediatamente utilizada para reconstituir o seu conteúdo.


## RAID 5 (Paridade distribuída)

O RAID 5 é frequentemente usado e funciona similarmente ao RAID 4, mas supera alguns dos problemas mais comuns sofridos por esse tipo. As informações sobre paridade para os dados do array são distribuídas ao longo de todos os discos do array , ao invés de serem armazenadas num disco dedicado, oferecendo assim mais desempenho que o RAID 4, e, simultaneamente, tolerância a falhas.

Vantagens:

- maior rapidez com tratamento de ECC;
- leitura rápida (porém escrita não tão rápida).

Desvantagem:

- sistema complexo de controle dos HDs.


## RAID 6

É um padrão relativamente novo, suportado por apenas algumas controladoras. É semelhante ao RAID 5, porém usa o dobro de bits de paridade, garantindo a integridade dos dados caso até 2 dos HDs falhem ao mesmo tempo.

Vantagem:

- possibilidade falhar 2 HDs ao mesmo tempo sem perdas.

Desvantagens:

- precisa de N+2 HDs para implementar por causa dos discos de paridade;
- escrita lenta;
- sistema complexo de controle dos HDs.


