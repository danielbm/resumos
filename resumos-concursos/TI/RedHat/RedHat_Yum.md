Red Hat: Gerenciamento de Pacotes com Yum
=========================================


# Introdução

O Yum é o gerenciador de pacotes do Red Hat. Ele é o equivalente, nos sistemas Red Hat, ao apt, no Ubuntu. É necessário que se execute o Yum como root.

# Trabalhando com Pacotes

## Procurando Atualizações

Comando:

          yum check-update

Para procurar somente por atualizações de segurança, use:

          yum check-update --security

Esse comando requer que o plugin yum-plugin-security esteja instalado.


## Atualizando Pacotes

Comando:

        yum update package_name


## Atualizando Todos os Pacotes e Dependências

Comando:

        yum update


## Procurando Pacotes

Comando:

        yum search <term>


## Listando Pacotes

Comandos:

         yum list all
         yum list installed glob_expression…
         yum list available glob_expression…

A expressão a ser pesquisada (glob_expression…) aceita expressões regulares. Exemplo:

          ~]$ yum list abrt-addon\* abrt-plugin\*


## Listando Repositórios

Comandos:

        yum repolist
        
        yum repolist -v
        
        yum repolist all


## Exibindo Informação de Pacotes

Comando:

        yum info package_name

Para informações mais detalhadas, use:

        yumdb info package_name


## Instalando Pacotes

Instalando um pacote:

        yum install package_name

Instalando vários pacotes:

        yum install package_name1 package_name2

Instalando pacotes para uma arquitetura específica:

        yum install package_name.arch

Exemplo:

        yum install sqlite2.i686

Observação: pode-se usar expressões regulares nos nomes para instalar pacotes semelhantes. Exemplo:

        ~]# yum install audacious-plugins-\*


## Removendo Pacotes

Comando:

        yum remove package_name

Observações:

  1. Não é possível remover um pacote sem também remover os pacotes que dependem dele
  2. Pode-se remover múltiplos pacotes de uma vez


# Configurando o Yum

As configurações do Yum são armazenadas no arquivo /etc/yum.conf. A seguir mostramos um exemplo desse arquivo:


        [main]
        cachedir=/var/cache/yum/$basearch/$releasever
        keepcache=0
        debuglevel=2
        logfile=/var/log/yum.log
        exactarch=1
        obsoletes=1
        gpgcheck=1
        plugins=1
        installonly_limit=3

        [comments abridged]

        # PUT YOUR REPOS HERE OR IN separate files named file.repo
        # in /etc/yum.repos.d



Informações sobre repositórios são armazenadas no diretório /etc/yum.repos.d/.

Obrigatóriamente, um arquivo de configuração de repositório deve ter o seguinte:

        [repository]
        name=repository_name
        baseurl=repository_url

A seguir é mostrado um exemplo de arquivo de configuração de um repositório (/etc/yum.repos.d/redhat.repo):

        [red-hat-enterprise-linux-scalable-file-system]
        name = Red Hat Enterprise Linux Scalable File System
        baseurl = https://cdn.redhat.com/content/dist/rhel/entitlement-6/releases/$releasever/$basearch/scalablefilesystem/os
        enabled = 1
        gpgcheck = 1
        gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-redhat-release
        sslverify = 1
        sslcacert = /etc/rhsm/ca/redhat-uep.pem
        sslclientkey = /etc/pki/entitlement/key.pem
        sslclientcert = /etc/pki/entitlement/11300387955690106.pem

## Usando Variáveis do Yum

- `$releaseserver`: o valor dessa variável é obtido da linha `distroverpkg=value` do arquivo /etc/yum.conf e se refere à versão de release do Red Hat em uso.
- `$arch`: valores válidos são: i586, i686, X86_64.
- `$basearch`: valores válidos: i386 e X86_64.

## Adicionando um Repositório

Comando:

        yum-config-manager --add-repo repository_url

## Habilitando um Repositório

Comando:

        yum-config-manager --enable repository


## Desabilitando um repositório

Comando:

        yum-config-manager --disable repository


## Criando um Repositório

São precisos três passos:

  1. Instale o pacote `createrepo`:
        yum install createrepo
  2. Copie todos os pacotes que deseja para um repositório, como o `/mnt/local_repo/`, por exemplo.
  3. Vá para esse diretório e execute o seguinte comando:
        createrepo --database /mnt/local_repo




