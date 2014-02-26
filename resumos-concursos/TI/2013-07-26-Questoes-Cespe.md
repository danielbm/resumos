---
layout: post
title: Como procurar erros em questões do Cespe/UnB
category: concursos
tags: [concursos, cespe]
---



Douglas Teixeira. Belo Horizonte, Minas Gerais. Julho, 2013.

# Introdução

A banca [CESPE/UnB](http://www.cespe.unb.br/) é uma das mais 
famosas bancas organizadoras de concursos públicos no Brasil. 
Parte de sua fama vem do seu estilo de prova: questões no estilo
verdadeiro ou falso, em que cada questão que o candidato erra o 
faz perder um dos pontos ganhos nas questões que ele acertou.

# Tipos de Erro a Procurar

Identificar questões _certas_ é muitas vezes difícil, então uma 
boa estratégia é procurar por erros nas questões. Para me ajudar
a fazer isso, criei um pequeno catálogo com os tipos de questões
nas quais a banca considera o item como _errado_.

## Inversão de conceitos

Esse item refere-se a questões com **conceitos corretos, mas nomes invertidos** 
ou aquelas em que a banca traz a **explicação correta de um conceito,** 
mas o classifica como **outro conceito**.

**Exemplos:**

**(PCF - PF/2013)** O ARP Spoofing é um tipo de ataque no qual o computador do
atacante gera quadros com endereços MAC falsos, para que a
tabela de endereços MAC do switch da rede seja preenchida
totalmente com endereços forjados. Com isso, muitos switches
não conseguem armazenar os endereços MAC verdadeiros e
acabam trabalhando como um hub, repassando os quadros a
todas as portas e permitindo que o atacante possa capturar o
tráfego da rede.

_A questão deu o conceito de ARP flooding, e disse que é ARP spoofing. Só fez inverter os nomes/conceitos._

**(PCF - PF/2013)** Caso determinada contravenção penal tenha repercussão
interestadual, poderá o Departamento de Polícia Federal do
Ministério da Justiça, sem prejuízo da responsabilidade dos
órgãos de segurança pública, proceder à sua investigação.

_A questão usou o termo contravenção penal, enquanto o correto seria crime. Só fez usar um nome correto para o conceito errado._

**Dica:** verifique se os conceitos estao corretos e com os nomes corretos
(cuidado: os nomes podem estar invertidos ou incorretos)


## Conceitos ou explicações sem nexo

**Exemplos:**

**(Analista Judiciário - STF/2008)** O serviço de FTP (file transfer protocol)
é um exemplo prático do uso de RPC (remote procedure call).

_Apesar de o protocolo FTP ser usado para transferir arquivos, ele não tem relação direta com RPC._

**Dica:** verifique se tudo que a questão falou faz sentido e se realmente estão 
relacionados.


## Palavras restringentes demais ou abrangentes demais 

Esse tipo de questões é conhecido por todos os candidatos. 
Elas ocorrem quando o examinador insere palavras como _apenas, tudo, todos, nenhum, etc_
na assertiva da questão. Esse tipo de questão é, **quase sempre**, _errada_.

**Exemplos:**

**(Agente Técnico de Inteligência - ABIN/2010)** Por padrão, qualquer dispositivo
que suporte gerenciamento de rede, seja por SNMP seja por RMON, suporta acesso via SSH.

_Falso, por causa da palavra **qualquer**._

**Dica:** verifique se a questão não restringe demais os conceitos ou os restringe além da conta.


## Explicação certa, conceito certo, razão errada

**Exemplos:**

**(PCF - PF/2013)** SHA-1 e MD-5 são exemplos de hashes criptográficos
largamente utilizados na Internet. O MD-5 tem sido substituído
pelo SHA-1 pelo fato de este gerar um hash maior e ser o
único à prova de colisões.

_O SHA-1 não é à prova de colisões._

**Dica:** cuidado com as questões grandes: elas podem conter pequenos erros, 
muitas vezes dificeis de perceber, em sentenças explicativas ou restritivas.


## Foco em uma parte do enunciado, pergunta sobre outra parte

Às vezes a questão dá enfase a um aspecto em detrimento de outro, mas cobra 
algo sobre o que negligenciou.

**Exemplo:**

Julgue o fragmento contido no item a seguir quanto à sua correção gramatical 
e à sua adequação para compor um documento oficial, que, de acordo com o Manual 
de Redação da Presidência da República, deve caracterizar-se pela impessoalidade, 
pelo emprego do padrão culto de linguagem, pela clareza, pela concisão, pela 
formalidade e pela uniformidade.

    Senhor Delegado,
    
    Segue para divulgação os relatórios das investigações realizadas no órgão,
    a fim de fazer cumprir a lei vigente.

_O correto seria "seguem". A questao deu enfase à redação oficial mas cobrou gramática._

**Dica:** atentar para todos os aspectos da questão.

## Erros em questões que contêm código-fonte

Frequentemente, as questões pedem ao candidato para analisar um fragmento de código e dizer o que o referido código faz. Entretanto, se o candidato olhar atenciosamente, verá que o **código sequer compila**. A banca costuma inserir pequenos erros, como deixar de fechar uma chave, comentar uma parte essencial do código, etc. Assim, o candidato mais atento encontra o erro da questão facilmente.

**Exemplo:**

**(OTI - ABIN/2010 Suporte a Rede de Dados)**

    for var1 in *; do
      var2=`echo $ var1
                  tr ' [:upper:]' '[:lower:]'
      if [ ! -e $ var2 ]; then
        mv $ var1 $ var2
      fi
    done

Considerando o trecho de código acima, no formato _shell script_, julgue o item a seguir.

O script acima verifica se já existe `var2` no sistema de arquivos e, caso não exista, renomeia `var1` para `var2`

_O erro nessa questão é sutil. Perceba que na segunda linha de código, deveríamos ter o fechamento do sinal de "\`", ao fazer a atribuição para a variável `var2`._

**Dica:** atentar para questões sintáticas do código, verificar as chaves, parenteses, etc.
