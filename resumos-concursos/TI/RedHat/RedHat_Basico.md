Red Hat: Configurações Básicas
==============================


# System Locale e Configurações de Teclado

Há duas formas de se configurar o locale:

  1. Editando o arquivo /etc/locale
  2. Usando a ferramenta localectl

## Arquivo /etc/locale

Este arquivo consiste numa lista de variáveis, uma em cada linha, conforme abaixo:

        LANG=de_DE.UTF-8 
        LC_MESSAGES=C

## Ferramenta localectl

Comandos úteis:

        localectl status

        localectl list-locales

        localectl set-locale LANG=locale

        localectl set-locale LANG=en_GB.utf8

## Mudando o Layout do Teclado

Comandos úteis:

        localectl list-keymaps

        localectl list-keymaps | grep en

        localectl set-keymap map

# Configurações de Data e Tempo

Ferramentas:

  - timedatectl
  - date

## timedatectl

Saída do comando:

        ~]$ timedatectl
          Local time: Mon 2013-09-16 19:30:24 CEST
          Universal time: Mon 2013-09-16 17:30:24 UTC
          Timezone: Europe/Prague (CEST, +0200)
          NTP enabled: no
          NTP synchronized: no
          RTC in local TZ: no
          DST active: yes
          Last DST change: DST began at
                  Sun 2013-03-31 01:59:59 CET
                  Sun 2013-03-31 03:00:00 CEST
          Next DST change: DST ends at
                  Sun 2013-10-27 02:59:59 CEST
                  Sun 2013-10-27 02:00:00 CET

Outros comandos úteis:

        timedatectl set-time YYYY-MM-DD

        timedatectl set-time HH:MM:SS

        timedatectl list-timezones

        timedatectl set-timezone Europe/Prague

## date

Comandos úteis:

        ~]$ date --utc
        Mon Sep 16 17:30:24 CEST 2013

        ~]# date +%T --set 23:26:00

        ~]# date +%F -s 2013-06-02


# Gerenciando Usuários e Grupos

No sistema normal de grupos do Linux, quando um usuário cria um arquivo, somente ele pode alterar este arquivo.

O Red Hat usa o esquema de Grupo Privado de Usuário (UPG). Com isso, o esquema de proteção de grupos descrito acima não é necessário porque cada usuário possui seu próprio grupo privado.

# Senhas Shadow

Vantagens desse tipo de senha:

  1. Move o hash das senhas do arquivo /etc/passwd (acessível, para leitura, a todos os usuários) para o arquivo /etc/shadow (acessível somente ao root).
  2. Armazenam informação sobre o "envelhecimento" de senhas
  3. Permite que políticas de segurança sejam impostas, usando o arquivo /etc/login/defs

Por exemplo, considere a seguinte entrada do arquivo /etc/passwd:

        juan:x:501:501::/home/juan:/bin/bash

O `x` indica o uso de senhas shadow.

Comandos que requerem que senhas shadow estejam habilitadas:

  - chage
  - gpasswd
  - usermod (opções -e ou -f)
  - useradd (opções -e ou -f)

# Usando a Ferramenta de Gerenciamento de Usuários

A ferramenta de gerenciamento de usuários permite a visualização e modificação de usuários e grupos. Há duas formas de usar a ferramenta:

  1. Menu Sistema -> Administração -> Usuários e Grupos
  2. Comando: system-config-users

Observação: tarefas administrativas envolvendo gerenciamento de usuários e grupos requerem acesso root.


# Adicionando um Novo Usuário

Por linha de comando:

        useradd [options] username

Quando um usuário é adicionado usando-se o comando acima os seguintes eventos ocorrem:

  1. Uma nova linha é criada para o usuário no arquivo /etc/passwd
  2. Uma nova linha é criada para o usuário no arquivo /etc/shadow
  3. Uma nova linha é criada para um grupo do usuário (lembre-se do UPG) no arquivo /etc/group
  4. Uma nova linha é criada para um grupo do usuário no arquivo /etc/gshadow
  5. Um diretório é criado para o usuário dentro do diretório /home
  6. Os arquivos dentro do diretório /etc/skel (que contém configurações-padrão de usuários) são copiados para o diretório home do usuário


# Ganhando Privilégios

## O Comando su

Quando um usuário digita `su` e a senha de root, ele se **transforma** em root. Uma vez root, o usuário pode usar `su <username>` para se transformar em qualquer outro usuário do sistema.

### Permitindo que Usuários Usem o Comando su

Basta usar:

        usermod -G wheel <username>

## O Comando sudo

O comando `sudo` permite que o usuário execute um comando como root, sem se tornar root efetivamente.

### Permitindo que Usuários Usem o Comando sudo

Basta usar:

        visudo

Isso abrirá o arquivo /etc/sudoers. Alguns exemplos de alterações nesse arquivo:

        juan ALL=(ALL) ALL

Permite que o usuário juan execute o comando sudo de qualquer host para executar qualquer comando.

        %users localhost=/sbin/shutdown -h now

Permite que qualquer usuário pode executar, no host, o comando `/sbin/shutdown -h now`.







