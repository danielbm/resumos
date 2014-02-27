Red Hat: Servidores de Arquivo
==============================


# Samba

## Introdução

Samba é uma implementação open source do protocolo SMB (Server Message Block). Ele permite a criação de redes com sistemas operacionais diferentes, possibilitando o acesso a arquivos e impressoras compartilhados no Windows.

Recursos:

  - Serve arvores de diretórios e impressoras para clientes Linux, Unix e Windows
  - Assiste na navegação de rede (com ou sem NetBIOS)
  - Autentica logins em domínios Windows
  - Provê resolução de nomes WINS (Windows Internet Name Service)
  - Pode se juntar a um domínio LDAP

O que ele não pode fazer:

  - Atuar como um controlador de domínio do Active Directory


## Daemons

  1. **smbd:** provê compartilhamento de arquivos e impressoras para clientes Windows. Também é responsável por autenticação. As portas padrão do protocolo SMB são: 139 e 445.
  2. **nmbd:** entende e responde a requisições NetBIOS de serviço de nomes. Porta de tráfego NMB: 137 (UDP).
  3. **winbindd:** resolve informação de usuários e grupos em ambienes Windows de modo que sisteas Unix/Linux compreendam essa informação.



## Instalação

Comando:

        yum install samba


# FTP

**Objetivo:** transferir arquivos de forma confiável entre hosts em uma rede sem requerer que o usuário faça login no host remoto ou tenha conhecimento de como usar o sistema remoto.

## Protocolo

Quando um cliente FTP inicia a conexão com o servidor, este abre a porta 21 (porta de comandos). Essa porta é usada para enviar todos os comandos para o servidor. Qualquer dado requisitado ao servidor é enviado para o cliente por meio de uma porta de dados, cujo número varia dependendo do modo de conexão FTP.


## Modos

### Modo Ativo

É o modo usado para transferir dados para a aplicação cliente.

Quando uma transferência de dados no modo ativo se inicia pelo cliente FTP, o servidor abre uma conexão em sua porta 20, para uma porta aleatória, sem privilégios (maior que 1024) especificada pelo cliente.


### Modo Passivo

É iniciado pelo cliente FTP. Quando o cliente requisita dados do servidor, ele indica que o quer fazer em modo passivo. Assim, o servidor disponibiliza uma porta aleatória sem privilégios (acima de 1024) para que o cliente baixe os dados requisitados.


