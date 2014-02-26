Resumo: HTTP e HTTPS
====================

# HTTP

## Características Principais

  - Porta: 80
  - Arquitetura: cliente-servidor
  - Versão 1.0 utiliza conexões TCP não-persistentes
  - Versão 1.1 utiliza conexões persistentes
  - É stateless: nenhuma informação sobre as solicitações são mantidas no servidor web

## Métodos

Os métodos existentes são:

  - GET: Requisita algum recurso.
  - POST: Requisita uma operação sobre um recurso pelo servidor.
  - HEAD: Requisita apenas o cabeçalho de um recurso.
  - PUT: Requisita o armazenamento de um recurso no servidor.
  - DELETE: Requisita a remoção de determinado recurso.
  - OPTIONS: Retorna os métodos que o servidor suporta.
  - CONNECT: Método reservado para facilitar o uso de mensagens encriptadas.



# HTTPS

HTTPS (HTTP sobre SSL) se refere à combinação de HTTP e SSL para implementar comunicação segura entre um browser Web e um servidor Web.

HTTP normal usa a porta 80; HTTPS usa a 443.

Quando HTTPS é usado os seguites elementos da comunicação são criptografados:

  - URL do documento requisitado
  - Conteúdo do documento
  - Conteúdo de formulários do browser
  - Cookies
  - Conteúdo do cabeçalho HTTP

Não há diferença entre o uso de HTTP com TLS ou SSL e todos as duas combinações são chamadas HTTPS.

## Inicio da Conexão

Para o HTTPS, o agente que age como cliente HTTP também age como o cliente TLS. O cliente inicia a conexão ao servidor na porta apropriada e então envia o TLS ClientHello para começar o handshake TLS. Quando essa etapa está completa, o cliente pode enviar a primeira requisição HTTP.

# Fechamento da Conexão

A ordem em que o fechamento de conexão acontece é a seguinte:

  1. O cliente termina o registro HTTP com uma linha "Connection: close."
  2. A conexão TLS é fechada, após a conexão HTTP ter sido.
  3. Por fim, a conexão TCP é fechada.

