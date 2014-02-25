Red Hat: OpenSSH
================


# Introdução

SSH permite que usuários façam login em sistemas remotamente. Características principais:

  - Usa **arquitetura cliente-servidor**.
  - Substitui clientes telnet e rsh.
  - O scp substitui o antigo rcp.
  - Pacotes: openssl, openssh-server, e openssh-clients.

# O Protocolo SSH


## Principais Recursos

**Ninguém pode se passar pelo servidor:** depois da primeira conexão, o cliente pode verificar que está conectado ao mesmo servidor que se conectou da primeira vez.

**Ninguém pode capturar as informações de autenticação:** O cliente transmite suas informações de autenticação usando criptografia de 128 bits.

**Ninguém pode interceptar a comunicação:** Todos os dados enviados e recebidos durante uma sessão são transferidos usando-se criptografia de 128 bits.

**Provê meios seguros para uso de interface gráfica na rede:** Com o uso da técnica de X11 Forwarding, o cliente pode encaminhar aplicações X11 do servidor.

**Provê mecanismos para aumento de segurança de protocolos inseguros:** O SSH encripta tudo que envia e recebe. Usando uma tecnica chamada Port Forwarding, um servidor SSH pode fornecer segurança a protocolos inseguros, como POP.

**Pode ser usado para criar um canal seguro:** Cliente e servidor podem criar um tunel SSH, semelhante a uma VPN.

**Suporta autenticação por Kerberos:** Clientes e servidores OpenSSH podem usar GSSAPI, uma implementação do Kerberos.


# Versões do Protocolo

A versão 1 possui algumas vulnerabilidades. A versão 2 corrige essas vulnerabilidades.


# Sequencia de Eventos em uma Conexão SSH

  1. Hanshake criptográfico: o cliente pode verificar que está se comunicando com o servidor correto.
  2. A camada de transporte da conexão entre o cliente e o host remoto é criptografada usando uma cifra simétrica. Aqui também acontece a troca de chaves e a negociação dos algoritmos de criptografia usados durante a sessão.
  3. O cliente se autentica no servidor.
  4. O cliente remoto interage com o servidor usando a conexão criptografada.


# OpenSSH: Principais Arquivos

  - `~/.ssh/authorized_keys`: lista de chaves públicas de servidores.
  - `~/.ssh/id_rsa`: contém chave privada do cliente
  - `~/.ssh/id_rsa.pub`: contém a chave pública do cliente.
  - `~/.ssh/known_hosts`: lista de hosts conhecidos.

# OpenSSH: Gerenciando o Serviço

Comandos:

        systemctl start sshd.service

        systemctl stop sshd.service

        systemctl enable sshd.service


# Gerando um Par de Chaves


Comando:

        ssh-keygen -t rsa





