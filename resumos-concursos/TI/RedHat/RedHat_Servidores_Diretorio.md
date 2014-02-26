Red Hat: Servidores de Diretório
================================

# OpenLDAP

O LDAP (Lightweight Directory Access Protocol) é um conjunto de protocolos usado para acesso centralizado a informação em uma rede. Ele é baseado no X.500.

O LDAP organiza informação de maneira hierarquica usando diretórios. Esses diretórios podem armazenar uma variedade de informações, como nomes, endereços, números de telefone, ou podem ser usados como NIS (Network Information Services), possibilitando a qualquer pessoa acessar sua máquina conta de qualquer máquina dentro da rede LDAP.

LDAP é comumente usado para gerenciar, de forma centralizada, usuários, grupos, autenticação, ou configurações do sistema.

## Introdução

Usando arquitetura cliente-servidor, o LDAP provê meios confiáveis de se criar um diretório central de informações acessível da rede. Quando um cliente tenta modificar informação dentro desse diretório, o servidor verifica se o usuário tem permissão de fazer a mudança, e então adiciona ou atualiza a entrada requisitada. 

LDAP pode usar SSL ou TLS para aumentar a segurança. Atualmente, no Red Hat, o LDAP não usa mais SSL. Ele usa o Network Security Services (NSS) da Mozilla.

LDAP suporta vários sistemas de bancos de dados.

## Terminologia

  - **entrada:** uma unidade no diretório LDAP. Cada entrada é identificada por seu Distinguished Name (DN).
  - **atributo:** informação diretamente associada com uma entrada. Por exemplo, se uma organização é representada como uma entrada no LDAP, atributos associados a essa organização podem incluir endereço, número de telefone, etc. O mesmo se aplica a pessoas representadas como entradas LDAP. Um atributo pode ser um único valor, ou uma lista não-ordenada de valores separados por espaço.
  - **LDIF:** LDAP Data Interchange Format (LDIF) é uma representação em texto plano de uma entrada LDAP.



## Instalação

Comando:

        yum install openldap openldap-clients openldap-servers


## Configuração

Diretório com arquivos de configuração: /etc/openldap/.

Principais arquivos de configuração:

  - /etc/openldap/ldap.conf: arquivo de configuração para clientes que usam bibliotecas ldap.
  - /etc/openldap/slapd.d/: diretório contendo as configurações do slapd.






