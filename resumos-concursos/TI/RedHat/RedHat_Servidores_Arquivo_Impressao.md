Red Hat: Servidores de Arquivo e Impressão
==========================================


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




