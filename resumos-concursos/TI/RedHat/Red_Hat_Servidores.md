Red Hat: Servidores
===================


# Apache

O servidor web Apache é compatível com o protocolo HTTP versão 1.1. Suas funcionalidades são mantidas através de uma estrutura de módulos, permitindo inclusive que o usuário escreva seus próprios módulos — utilizando a API do software.

## Novos Recursos do Apache 2.2

  - Novos módulos de cache: mod_cache e mod_disk_cache
  - Suporte a balanceamento de carga a través do módulo mod_proxy_balancer
  - Suporte a arquivos maiores que 2GB em arquiteturas de 32 bits
  - Nova estrutura de autenticação


## Checando Erros de Configuração

Comando:

        service httpd configtest


## Instalando o Serviço

Comando:

        yum install httpd


## Iniciando e Reiniciando o Serviço

Comando:

        systemctl start httpd.service

Se você quer que o serviço inicie automaticamente quando o computador der boot, use:

        systemctl enable httpd.service

        ln -s '/usr/lib/systemd/system/httpd.service' '/etc/systemd/system/multi-user.target.wants/httpd.service'


Para reiniciar o serviço, digite:

        systemctl restart httpd.service

## Parando o Serviço

Comando:

        systemctl stop httpd.service

Para impedir o serviço de iniciar quando o computador é ligado:

        systemctl disable httpd.service

        rm '/etc/systemd/system/multi-user.target.wants/httpd.service'


## Verificando o Status

Comando:

        systemctl is-active httpd.service


## Arquivos de Configuração

O principal arquivo de configuração do Apache é o `/etc/httpd/conf/httpd.conf`. Existe também um diretório com arquivos de configuração auxiliares: `/etc/httpd/conf.d/`.

Após configurar algo, para checar se o arquivo não possui nenhum erro de sintaxe, digite:

        service httpd configtest


## Diretivas de Configuração mais Comuns

### `<Directory>`

Essa diretiva permite que configurações sejam aplicadas a um único diretório. Ela possui a seguinte estrutura:

        <Directory directory>
            directive
            directive
            ...
        </Directory>

Exemplo:

        <Directory /var/www/html>
            Options Indexes FollowSymLinks
            AllowOverride None
            Order allow,deny
            Allow from all
        </Directory>



### `<IfDefine>`

Essa diretiva permite que outras diretivas sejam aplicadas somente quando um parametro é fornecido na linha de comando. Exemplo:

        <IfDefine EnableHome>
            UserDir public_html
        </IfDefine>



### `<IfModule>`

Permite que outras diretivas sejam aplicadas somente se um dado módulo estiver carregado. Exemplo:

        <IfModule mod_disk_cache.c>
            CacheEnable disk /
            CacheRoot /var/cache/mod_proxy
        </IfModule>


### `DirectoryIndex`

Permite especificar um documento a ser exibido caso um cliente requisite um diretório. Exemplo:


        DirectoryIndex index.html index.html.var

Faz com que os documentos index.html e index.html.var sejam exibidos caso o usuário digite a url do diretório em que eles estão.


### `KeepAlive`

Possibilita habilitar conexões persistentes. Exemplo:

        KeepAlive on


# Servidores de Email

## Protocolos de Email

Serviços de email usam arquitetura cliente-servidor. O processo de envio de um email é o seguinte:

  1. A mensagem é criada usando um programa cliente de email.
  2. A mensagem é enviada a um servidor.
  3. O servidor encaminha a mensagem ao servidor de email do destinatário.
  4. A mensagem é entregue ao destinatário.

### SMTP

O objetivo primário do SMTP é transferir emails entre servidores de email.

**Porta:** 25 (default), SMTPS usa a 465.

Observação importante: SMTP não requer autenticação, fazendo com que qualquer um possa enviar email pra qualquer um.


### POP

O servidor POP default to Red Hat é o Dovecot. Instale-o através do seguinte comando:

        yum install dovecot

Com o POP, as mensagens de email são baixadas pelo cliente de email. Por padrão, a maioria dos clientes de email POP são configurados para deletar as mensagens de email do servidor depois que elas são lidas.

POP é compatível com MIME.

**Porta:** 110

A versão atual do protocolo é a versão 3: POP3. Entretanto, existem algumas variações do protocolo que ainda são usadas:

  - KPOP: POP3 com autenticação Kerberos.
  - APOP: POP com Monash Directory Service. Um hash da senha do usuário é enviado ao servidor, em vez de enviar a senha não-criptografada.
  - RPOP: usa um ID de usuário para fazer autenticação.


### IMAP

Com IMAP, as mensagens de email permanecem no servidor, mesmo depois de serem lidas pelo usuário. Ele é útil para pessoas que acessam email de máquinas diferentes.

Pode manter um cache local das mensagens.

É compatível com MIME.

**Porta:** 143


## Classificação de Programas de Email


### Mail Transport Agent

Um MTA transporta mensagens entre hosts usando SMTP. O MTA do Red Hat é o sendmail.

### Mail Delivery Agent

O MDA é invocado pelo MTA para registrar um email que chega à caixa postal do usuário. MDAs distribuem e ordenam mensagens na máquina para um cliente de email acessar.


### Mail User Agent

É um sinônimo para cliente de email.



