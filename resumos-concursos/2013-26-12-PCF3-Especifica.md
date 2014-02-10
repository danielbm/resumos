=========================================================
Perito Criminal Federal - Area 3 - CESPE/UnB MJ/DPF/2013
=========================================================

---------------------------
# CONHECIMENTOS ESPECIFICOS
---------------------------

**Acerca da organiza��o e arquitetura de computadores e dos componentes
de um computador, julgue os itens a seguir.**

**51.** A diminui��o do tamanho dos chips resulta em ganho de desempenho
em hardware, uma vez que leva ao aumento da rela��o entre resist�ncia e
capacit�ncia, pois as interconex�es de fio se tornam mais finas,
aumentando a resist�ncia, e os fios est�o mais pr�ximos, aumentando a
capacit�ncia.

**52.** Arquitetura de computador refere-se aos atributos de um sistema
vis�veis a um programador, ou seja, atributos que possuem impacto direto
sobre a execu��o l�gica de um programa. Nesse contexto, � considerada
uma quest�o arquitetural, por exemplo, se uma instru��o de multiplica��o
ser� realizada por uma unidade de multiplica��o especial ou por um
mecanismo que fa�a uso repetido da unidade de adi��o do sistema.

* * * * *

**A respeito dos princ�pios de sistemas operacionais, das
caracter�sticas dos principais processadores do mercado e dos
processadores de m�ltiplos n�cleos, julgue os itens subsequentes.**

**53.** Por meio da t�cnica de pipeline, a arquitetura MIMD e a MISD
podem executar m�ltiplos threads ao mesmo tempo. Na arquitetura MISD, os
threads executados s�o independentes e manipulam dados diferentes.

**54.** No processamento das interrup��es geradas pelos componentes de
entrada e sa�da, � necess�rio que o processador identifique univocamente
qual dispositivo gerou a interrup��o. Uma das t�cnicas utilizadas para
essa identifica��o � a daisy chain, que realiza a identifica��o por
hardware, usando uma conex�o entre os m�dulos e o processador, na forma
de uma cadeia circular.

* * * * *

**Julgue o pr�ximo item, no que se refere � paravirtualiza��o.**

**55.** A substitui��o da chamada de uma instru��o sens�vel pela chamada
de um tratador de interrup��o de software (trap) com uma parametriza��o
adequada de registradores � conhecida como hypercall.

* * * * *

**Com refer�ncia a sistemas de arquivos e a sistemas RAID, julgue o item
seguinte.**

**56.** Em sistemas de arquivos NTFS, a tabela-mestra de arquivos (MTF)
� dividida em seis parti��es de tamanhos vari�veis. Para prover
toler�ncia a falhas nessa configura��o, � necess�rio e suficiente
organiz�-los utilizando-se RAID n�vel 4, pois, quanto maior o n�mero de
discos do arranjo, menor ser� a possibilidade de falha.

* * * * *

**Julgue o item abaixo, referente �s t�cnicas de recupera��o de arquivos
apagados.**

**57.** C�pias de seguran�a f�sicas armazenam dados, usando uma
estrutura de diret�rio e permitem que os dados de arquivo sejam
recuperados por sistemas heterog�neos. Salvar arquivos nesse formato �
eficiente, pois n�o ocorre sobrecarga na tradu��o entre o formato do
arquivo nativo e o formato de arquivamento.

* * * * *

**No que se refere a arquitetura, modelos l�gicos e representa��o f�sica
de banco de dados e implementa��o de SGBDs relacionais, julgue os itens
que se seguem.**

**58.** As depend�ncias de dados, que incluem as funcionais e as
multivaloradas, s�o consideradas depend�ncias sem�nticas da
implementa��o do banco de dados, por serem restri��es inerentes
embasadas no modelo.

**59.** A arquitetura ANSI de tr�s n�veis separa o n�vel externo dos
usu�rios, o n�vel conceitual do banco de dados e o n�vel de
armazenamento interno no projeto de um banco de dados. O n�vel interno
tem um esquema interno, que descreve a estrutura do armazenamento f�sico
do banco de dados e descreve os detalhes completos do armazenamento de
dados e os caminhos de acesso para o banco de dados.

**60.** Em SQL, triggers s�o conhecidas como t�cnicas de banco de dados
ativo, pois especificam a��es que s�o disparadas automaticamente por
eventos.

**61.** Diverg�ncia de imped�ncia � o termo usado para se referir aos
problemas que ocorrem devido �s diferen�as entre o modelo de banco de
dados e o modelo da linguagem de programa��o.

* * * * *

**Com rela��o a caracter�sticas e an�lise de logs em transa��es de banco
de dados, julgue o item subsequente.**

**62.** Para realizar a auditoria em um banco de dados, a utiliza��o de
um sistema gerenciador de streams de dados (SGSD) impede que o
administrador do banco de dados defina os par�metros de auditoria e os
dados a serem auditados mediante consultas, de tal forma que os
resultados sejam obtidos em tempo real, minimizando o volume de
registros de log que precisam ser armazenados.

* * * * *

**Acerca dos conceitos da engenharia reversa, julgue os itens
subsecutivos.**

**63.** A depura��o de programas utiliza m�todos de teste e an�lise para
tentar entender o software. Esses m�todos s�o classificados como
caixa-branca (white box) e caixa-preta (black box). Para se conhecer o
c�digo e seu comportamento, o teste caixa-branca � menos eficiente que o
teste caixa-preta, embora seja mais f�cil de ser implementado.

**64.** Red pointing � o m�todo mais r�pido para se realizar engenharia
reversa em um c�digo. Para criar um red pointing em um c�digo alvo, �
suficiente identificar no programa os locais potencialmente vulner�veis,
que fazem chamada ao sistema operacional, e detectar os dados fornecidos
pelo usu�rio, que s�o processados nesse local.

**65.** A engenharia reversa permite conhecer a estrutura do programa e
sua l�gica e, com base nessas informa��es, alterar a estrutura do
programa, afetando diretamente o fluxo l�gico. Essa atividade �
conhecida como patching.

* * * * *

**Com rela��o � ofusca��o de c�digo, a programas maliciosos e a
compactadores de c�digo execut�vel, julgue os itens seguintes.**

**66.** Programas maliciosos do tipo RootKits s�o os mais perigosos,
principalmente para usu�rios de Internet Banking, pois esses programas
t�m a fun��o de capturar as teclas digitadas no computador.

**67.** Um arquivo compactado do Linux cujo nome � prova.tar.gz poder�
ser descompactado para a sa�da padr�o, alterando-se o nome original, por
meio do comando `gzip dc prova.tar.gz tar xvf`.

* * * * *

**No que se refere �s linguagens de programa��o, julgue os itens
subsecutivos.**

**68.** A execu��o da fun��o x descrita abaixo para o valor n igual a 8
fornecer� 21 como resultado.

    long x(int n) {
      if (n<0)
        return -1; 
      if (n==0)
        return 0;
      if (n==1)
        return 1;
      return x(n-1) + x(n-2);
    }

**71.** No servlet e Jsp, o tratamento de caracteres especiais como
caractere comum, recebidos em p�ginas HTML, pode ser feito por meio do
m�todo est�tico encode da classe java.net.URLEncoder.

**72.** A propriedade readyState do objeto XMLHttpRequest em Ajax no
Internet Explorer possui 3 est�gios, sendo 0 correspondente a n�o
inicializado, 1 correspondente a carregado e 2 correspondente a
completo.

* * * * *

**Com rela��o aos conceitos e caracter�sticas de compiladores, julgue os
itens que se seguem.**

**73.** Interpretador � um tradutor de linguagem que executa o programa
fonte de imediato, em vez de gerar um c�digo objeto a ser executado ap�s
o t�rmino da tradu��o, enquanto o compilador recebe um programa fonte e
produz programa equivalente na linguagem alvo. No caso da linguagem
Java, os processadores combinam compila��o e interpreta��o.

**74.** Considere a gram�tica string = string + string | string string =
|0|1|2|3|4|5|6|7|8|9 e a string como um �nico n� n�o terminal, que pode
ser um d�gito ou uma senten�a. Nessa situa��o, a express�o 10 - 4 + 3
possibilita criar duas �rvores de deriva��o distintas.

**76.** Considere `tnode` um n� de uma lista encadeada e a fun��o
`monta_lista` listados abaixo. Nesse caso, a utiliza��o da fun��o
`monta_lista` criar� uma lista encadeada com as informa��es ordenadas em
ordem decrescente alfabeticamente e o ponteiro topo apontar� para o n�
com a maior informa��o alfab�tica.

    struct tnode { 
      char info[100]; 
      struct tnode *prox;
    }; 

    monta_lista(struct tnode **topo, struct tnode *p)) { 
      struct tnode *atual, *ant; 
      if (*topo == NULL) { 
        *topo = p; return;
      } 

      if (strcmp((*topo)->info, p->info) >= 0) {
        p->prox = *topo; 
        *topo = p; 
        return;
      } 

      ant = *topo;
      atual = ant->prox;

      while (atual != NULL) {
        if (strcmp(atual->info,p->info) > 0) {
          p->prox = atual;
          ant->prox = p;
          return;
        } 

        ant = atual; 
        atual = atual->prox;
      }

      ant->prox = p;
    }

**78.** Considere um vetor C com valores entre 0 e 999, em que cada
elemento do vetor � dividido em tr�s partes (unidade, dezena e centena).
Nesse caso, o m�todo de classifica��o por distribui��o de chave,
aplicado sobre C, realizar� a ordena��o dos valores pela execu��o de
sucessivos passos, tomando-se em cada passo apenas uma parte do
elemento.

* * * * *

**Julgue os itens que se seguem, referentes a t�cnicas de comunica��o,
topologias, arquiteturas e protocolos relacionados �s redes de
computadores.**

**80.** Para assegurar uma topologia livre da ocorr�ncia de loops, o que
� fundamental para que redes IEEE 802.5 funcionem adequadamente, os
equipamentos de interconex�o, como switches e pontes, trocam informa��es
com a utiliza��o do protocolo STP (Spanning Tree Protocol).

**81.** Com rela��o � qualidade de servi�o (QoS) na camada de rede IP,
os servi�os diferenciados (DiffServ) s�o embasados no conceito de
classes de servi�os. Os servi�os integrados (IntServ), por sua vez,
utilizam uma abordagem de parametriza��o na qual � necess�ria a reserva
pr�via de recursos nos roteadores com o uso do protocolo de sinaliza��o
RSVP (Resource Reservation Protocol).

**82.** Utilizado em dispositivos de acesso a redes sem fio, o padr�o
IEEE 802.1x prov� um mecanismo de autentica��o para dispositivos que se
conectam a uma porta em uma LAN. Esse padr�o envolve tr�s partes: o
cliente (tamb�m conhecido como suplicante), um dispositivo autenticador
e o servidor de autentica��o (por exemplo, o Radius).

**83.** Em uma rede P2P (peer-to-peer), cada computador pode atuar como
cliente e como servidor de outros computadores, possibilitando, por
exemplo, o compartilhamento de arquivos. O BitTorrent � um dos
protocolos para redes P2P e caracteriza-se pela exist�ncia de um
mapeamento das taxas de download e upload entre os peers, de forma que
um cliente pode transferir um arquivo a partir do peer com maior taxa de
transfer�ncia.

**84.** Considerando-se o endere�amento IPv4 das redes com arquitetura
TCP/IP e sabendo-se que o \*\*endere�o de um host em uma sub-rede �
182.44.82.16/27, � correto afirmar que os endere�os 182.44.82.158 e
182.44.82.159 representam hosts em uma mesma sub-rede.

**85.** Com base nas caracter�sticas inerentes a um equipamento de
interconex�o de ponto de acesso sem fio (wireless access point), �
correto afirmar que ele funciona como uma ponte (bridge).

* * * * *

**Acerca de computa��o em nuvem, julgue os itens subsequentes.**

**86.** O GAE (Google App Engine) pertence � categoria de computa��o em
nuvem conhecida como IaaS (Infrastructure as a Service) e caracteriza-se
por prover m�quinas virtuais, infraestrutura de armazenamento,
firewalls, balanceamento de carga, entre outros recursos, de forma a
hospedar aplica��es web nos datacenters da Google.

**87.** Com o ambiente de computa��o em nuvem Azure, da Microsoft, �
poss�vel a cria��o de m�quinas virtuais com sistemas operacionais
distintos, desde o Windows Server at� m�quinas com distribui��o Linux,
como, por exemplo, CentOS, Suse e Ubuntu.

* * * * *

**Com rela��o � norma ISO/IEC 27001:2006, julgue os itens a seguir.**

**88.** De acordo com a norma ISO/IEC 27001:2006, a formula��o de um
plano de tratamento de riscos que identifique a a��o apropriada, os
recursos, as responsabilidades e as prioridades para a gest�o de riscos
est� relacionada � etapa Do do ciclo PDCA.

**89.** Segundo a norma ISO/IEC 27001:2006, a organiza��o deve elaborar
uma declara��o de aplicabilidade, detalhando os ativos dentro do escopo
do SGSI e os seus propriet�rios, bem como as poss�veis amea�as aplicadas
a tais ativos e as vulnerabilidades por elas exploradas.

**90.** Segundo a norma ISO/IEC 27001:2006, no estabelecimento do
Sistema de Gest�o da Seguran�a da Informa��o (SGSI), devem-se
identificar e avaliar as op��es para o tratamento de riscos, cujas a��es
englobam a aceita��o consciente dos riscos (desde que satisfa�am �s
pol�ticas estabelecidas dentro da organiza��o), bem como a possibilidade
de transfer�ncia dos riscos para outras partes, como seguradoras e
fornecedores.

* * * * *

**A respeito de seguran�a da informa��o, julgue os pr�ximos itens.**

**91.** O ser humano possui tra�os psicol�gicos e comportamentais que o
tornam vulner�veis a ataques de engenharia social, como a vontade de ser
�til, a busca por novas amizades, esteganografia e autoconfian�a.

**92.** Um aplicativo que utiliza recursos biom�tricos para a
criptografia de arquivos, como a impress�o digital de um indiv�duo tanto
para encriptar quanto decriptar, assemelha-se a um sistema criptogr�fico
sim�trico.

* * * * *

**No que se refere a processos de desenvolvimento seguro de aplica��es,
julgue os itens subsecutivos.**

**93.** O processo SDL (Secure Development Lifecycle) tem sido adotado
pela Microsoft no desenvolvimento de alguns de seus produtos, como
Windows Server, SQL Server e Exchange Server, reduzindo o n�mero de
vulnerabilidades encontradas nesses produtos em vers�es desenvolvidas
sem o uso do SDL. Uma das caracter�sticas desse processo � que ele prov�
dois roteiros, sendo um com foco no suporte a desenvolvimento de novos
sistemas com base em um processo iterativo, e outro que enfoca a
manuten��o de sistemas j� existentes.

**94.** O CLASP (Comprehensive, Lightweight Application Security
Process) fornece uma taxonomia de vulnerabilidades que podem ocorrer no
c�digo-fonte e que podem ser verificadas com o uso de ferramentas
automatizadas para an�lise est�tica de c�digo.

* * * * *

**Julgue os seguintes itens, relativos � seguran�a em redes de
computadores.**

**95.** O termo APT (Advanced Persistent Threat) refere-se a ataques que
s�o altamente focados em uma empresa ou em um governo particular.
Geralmente, o ataque � conduzido de forma lenta e gradativa, podendo
levar meses ou anos para atingir seu objetivo. O v�rus Stuxnet, que
recentemente atingiu o programa nuclear iraniano, � considerado um
exemplo de APT.

**96.** O uso de criptografia SSL (Secure Socket Layer) como item de
seguran�a nas transmiss�es de dados via Internet dificulta o
monitoramento realizado por sistemas de detec��o de intrusos (IDS) de
redes. Uma solu��o para esse problema � o uso de proxies reversos, que
permite retirar o processo de criptografia do servidor web e,
consequentemente, possibilita ao IDS o monitoramento do tr�fego.

**97.** A captura de quadros de redes wireless IEEE 802.11 geralmente
n�o � alcan�ada com o uso do modo prom�scuo da interface de rede, sendo
necess�rio configurar a interface de rede para o modo de monitoramento
(monitor mode). Al�m disso, pode haver restri��es por parte do sistema
operacional, como ocorre no Windows, o que impede a captura de quadros
desse tipo.

**98.** O WIPS (Wireless Intrusion Prevention System) � um dispositivo
que monitora o espectro de ondas de r�dio, buscando identificar a
presen�a de pontos de acesso n�o autorizados. Ao detectar a presen�a de
sinais de r�dio n�o autorizados, o WIPS pode enviar alerta ao
administrador ou ao firewall da rede para prevenir poss�veis ataques.

**99.** O ARP Spoofing � um tipo de ataque no qual o computador do
atacante gera quadros com endere�os MAC falsos, para que a tabela de
endere�os MAC do switch da rede seja preenchida totalmente com endere�os
forjados. Com isso, muitos switches n�o conseguem armazenar os endere�os
MAC verdadeiros e acabam trabalhando como um hub, repassando os quadros
a todas as portas e permitindo que o atacante possa capturar o tr�fego
da rede.

**100.** Phishing � a t�cnica empregada por v�rus e cavalos de troia
para obter informa��es confidenciais do usu�rio, como, por exemplo,
dados banc�rios.

**101.** Traffic shaping � uma pr�tica que tem sido adotada por empresas
de telefonia e provedoras de acesso � Internet que, apesar de ser
considerada abusiva por parte de �rg�os de defesa do consumidor,
geralmente � utilizada para otimizar o uso da largura de banda
dispon�vel, restringindo a banda para servi�os que demandam a
transfer�ncia de grande volume de dados, como P2P e FTP.

* * * * *

**A respeito de criptografia, julgue os itens subsequentes.**

**102.** Modos de opera��o de cifra de bloco permitem cifrar mensagens
de tamanhos arbitr�rios com a utiliza��o de algoritmos de cifragem de
blocos, que trabalham com blocos de tamanho fixo. Os modos de opera��o
existentes asseguram a confidencialidade e a integridade da mensagem
cifrada, embora nem todos possam ser utilizados para autentica��o.

**103.** A confidencialidade e a integridade de uma comunica��o s�o
garantidas com o uso de criptografia tanto sim�trica quanto assim�trica.
No entanto, para garantir autenticidade e irretratabilidade, �
necess�rio o uso combinado desses dois tipos de criptografia.

* * * * *

**Julgue os itens a seguir, a respeito de certifica��o digital e
algoritmos RSA, AES e RC4.**

**104.** Ao acessar um s�tio seguro na Internet e receber o certificado
digital do servidor, o navegador do cliente faz uma consulta �
autoridade certificadora que assinou aquele certificado para verificar,
por exemplo, se o certificado � v�lido ou n�o est� revogado. Essa
verifica��o � feita com o uso do protocolo OCSP (Online Certificate
Status Protocol).

**105.** AES � uma cifra de bloco, enquanto o RC4 � uma cifra de fluxo.
Apesar dessa diferen�a, ambos t�m em comum a utiliza��o de um tamanho de
chave de 128, 192 ou 256 bits.

**106.** Embora o algoritmo RSA satisfa�a aos requisitos necess�rios
para prover assinatura digital, ele � utilizado, por quest�es de
desempenho, em conjunto com fun��es de hashes criptogr�ficos, como
SHA-1. A respeito de hashes criptogr�ficos, julgue os itens que se
seguem.

**107.** SHA-1 e MD-5 s�o exemplos de hashes criptogr�ficos largamente
utilizados na Internet. O MD-5 tem sido substitu�do pelo SHA-1 pelo fato
de este gerar um hash maior e ser o �nico � prova de colis�es.

**108.** O SHA-1, comumente usado em protocolos de seguran�a, como TLS,
SSH e IPSec, tamb�m � utilizado por alguns sistemas de controle de
vers�o como Git e Mercurial para garantir a integridade das revis�es.

* * * * *

**Julgue os itens a seguir, acerca do sistema operacional Windows.**

**109.** Administradores de redes com Windows 7, em compara��o a
administradores de rede com Windows Vista, precisam conceder maior
n�mero de privil�gios a recursos de rede que exigem acesso de super
usu�rio. Isso se deve, entre outros fatores, ao maior n�mero de
aplicativos do Windows 7 que exigem acesso com privil�gios
administrativos.

**110.** Aplicativo, Seguran�a, Sistema, Instala��o e ForwardedEvents
s�o categorias de logs do Windows cuja finalidade � organizar os eventos
de aplicativos que s�o monitorados pelo sistema operacional, permitindo
aos administradores decidirem quais eventos ser�o gravados no log.

**111.** BitLocker � um recurso presente no Windows 7 que fornece
criptografia de todos os volumes de inicializa��o para um computador e
para dispositivos m�veis, como unidades flash USB.

**112.** AppLocker � um recurso do Windows 7 que permite especificar
quais aplicativos podem ser executados em um desktop ou notebook,
ajudando, assim, a diminuir a probabilidade de execu��o de malwares
nessas m�quinas. Com rela��o � governan�a de tecnologia da informa��o
(TI), julgue os itens subsequentes.

**113.** Registro do Windows � um banco de dados que cont�m informa��es
sobre os programas instalados, configura��es, perfis das contas de
usu�rios e sobre o hardware do sistema.

* * * * *

**Julgue os itens seguintes, com rela��o ao Linux.**

**114.** Squid � uma aplica��o nativa do Linux que prov� servi�os de
correio eletr�nico compat�veis com o SMTP (Simple Mail Transfer
Protocol), IMAP (Internet Message Access Protocol) e POP3 (Post Office
Protocol).

**115.** O escalonador de tarefas do Linux presente na vers�o 2.6
fornece afinidade de processador, balanceamento de carga e suporte para
multiprocessamento sim�trico por meio de algoritmo preemptivo embasado
em prioridades. Dessa forma, quanto maior for a prioridade, maior ser� a
quota de tempo fornecida.

**116.** No Linux, os usu�rios s�o cadastrados no sistema no arquivo
/home, que guarda uma entrada para cada usu�rio, incluindo-se o
diret�rio e o shell.

* * * * *

**No que se refere aos sistemas Android e iOS, julgue os pr�ximos
itens.**

**117.** O sistema Android 4.0 foi desenvolvido com base no kernel Linux
vers�o 2.6 e � voltado para dispositivos m�veis, controlando os servi�os
do sistema, como gerenciamento de mem�ria e de tarefas, diretivas de
seguran�a e drivers.

**118.** A arquitetura do iOS possui quatro camadas (layers) que
funcionam como interface entre a aplica��o e o hardware. Essas camadas,
listadas da mais baixa para a mais alta, s�o: Core OS, Core Services,
Media e CoCoa Touch.

* * * * *

**Com rela��o � governan�a de tecnologia da informa��o (TI), julgue os
itens subsequentes.**

**119.** O COBIT abrange controles acerca de ger�ncia de central de
servi�os especificamente no dom�nio Entregar e Suportar.

**120.** No ITIL v3, a central de servi�os � tipificada como uma fun��o
do est�gio Opera��o de Servi�os. Com base na SLTI MP IN n. 4/2010, em
uma contrata��o de solu��o de TI, a fase de planejamento da contrata��o
prescinde a fase de sele��o do fornecedor.

* * * * *

PROVA DISCURSIVA
================

Nesta prova, fa�a o que se pede, usando, caso deseje, o espa�o para
rascunho indicado no presente caderno. Em seguida, transcreva o texto
para a FOLHA DE TEXTO DEFINITIVO DA PROVA DISCURSIVA, no local
apropriado, pois n�o ser�o avaliados fragmentos de texto escritos em
locais indevidos.

Qualquer fragmento de texto que ultrapassar a extens�o m�xima de linhas
disponibilizadas ser� desconsiderado. Na folha de texto definitivo,
identifique-se apenas na primeira p�gina, pois n�o ser� avaliado o texto
que apresentar qualquer assinatura ou marca identificadora fora do local
apropriado.

Ao dom�nio do conte�do ser�o atribu�dos at� 13,00 pontos, dos quais at�
0,60 ponto ser� atribu�do ao quesito apresenta��o e estrutura textual
(legibilidade, respeito �s margens e indica��o de par�grafos).

*Se uma intrus�o em um sistema computacional for detectada com rapidez
suficiente, o intruso poder� ser identificado e expulso do sistema antes
que qualquer dado seja comprometido. Mesmo que a detec��o n�o seja
suficiente para impedir o intruso, quanto mais cedo for detectada a
intrus�o, menores ser�o os danos e mais rapidamente a recupera��o poder�
ser obtida.* *William Stallings. Criptografia e seguran�a de redes:
princ�pios e pr�ticas. 4.� ed. S�o Paulo: Pearson Prentice Hall, 2008,
p. 408 (com adapta��es).*

Considerando que o fragmento de texto acima tem car�ter unicamente
motivador, redija um texto dissertativo acerca do seguinte tema.
**SISTEMAS DE DETEC��O DE INTRUS�O (IDS: INTRUSION DETECTION SYSTEMS)**
Ao elaborar seu texto, aborde, necessariamente, os seguintes aspectos:

-   defini��o de IDS; [valor: 3,00 pontos]
-   diferen�as entre IDS e firewall; [valor: 3,00 pontos]
-   tipos de IDS, em especial aqueles embasados em rede e em host;
    [valor: 3,00 pontos]
-   principais t�cnicas de detec��o de intrusos e suas limita��es.
    [valor: 3,40 pontos]
