
# Padrão X.509




ITU-T recommendation X.509 is part of the X.500 series of recommendations that define a directory service. The directory is, in effect, a server or distributed set of servers that maintains a database of information about users. The information includes a mapping from user name to network address, as well as other attributes and information about the users.
X.509 defines a framework for the provision of authentication services by the X.500 directory to its users. The directory may serve as a repository of public-key certificates of the type discussed in Section 14.3. Each certificate contains the public key of a user and is signed with the private key of a trusted certification authority. In addition, X.509 defines alternative authentication protocols based on the use of public-key certificates.
X.509 is an important standard because the certificate structure and authenti- cation protocols defined in X.509 are used in a variety of contexts.

X.509 is based on the use of public-key cryptography and digital signatures. The standard does not dictate the use of a specific algorithm but recommends RSA. The dig- ital signature scheme is assumed to require the use of a hash function. Again, the stan- dard does not dictate a specific hash algorithm.
# Certificados

O coração do esquema X.509 é o certificado de chave pública associado a cada usuário. Assume-se que esses certificados do usuário são criados por uma entidade certificadora (CA) confiável.

Os certificados possuem os seguintes campos:

  - Versão
  - Número serial
  - Identificador do algoritmo de assinatura
  - Nome do emissor
  - Nome do dono do certificado
  - Informações sobre a chave pública do dono do certificado
  - Identificador único do emissor (ID)
  - Extensões
  - Assinatura (hash dos campos, criptografado com a chave privada da CA)


# X.509 Versão 3



version 3 includes a number of optional extensions that may be added to the version 2 format. Each extension consists of an extension identifier, a criticality indicator, and an extension value. The criticality

indicator indicates whether an extension can be safely ignored. If the indicator has a value of TRUE and an implementation does not recognize the extension, it must treat the certificate as invalid.
The certificate extensions fall into three main categories: key and policy infor- mation, subject and issuer attributes, and certification path constraints.



PKI

RFC 2822 (Internet Security Glossary) defines public-key infrastructure (PKI) as the set of hardware, software, people, policies, and procedures needed to create, manage, store, distribute, and revoke digital certificates based on asymmetric cryp- tography. The principal objective for developing a PKI is to enable secure, conve- nient, and efficient acquisition of public keys. 


Figure 14.16 shows the interrelationship among the key elements of the PKIX model. These elements are
• End entity: A generic term used to denote end users, devices (e.g., servers, routers), or any other entity that can be identified in the subject field of a pub- lic key certificate. End entities typically consume and/or support PKI-related services.
• Certificationauthority(CA):Theissuerofcertificatesand(usually)certificate revocation lists (CRLs). It may also support a variety of administrative functions, although these are often delegated to one or more Registration Authorities.

 Registration authority (RA): An optional component that can assume a num- ber of administrative functions from the CA. The RA is often associated with the end entity registration process but can assist in a number of other areas as well.
• CRL issuer: An optional component that a CA can delegate to publish CRLs.
• Repository: A generic term used to denote any method for storing certificates
and CRLs so that they can be retrieved by end entities.
PKIX Management Functions
PKIX identifies a number of management functions that potentially need to be sup- ported by management protocols. These are indicated in Figure 14.16 and include the following:
• Registration: This is the process whereby a user first makes itself known to a CA (directly or through an RA), prior to that CA issuing a certificate or cer- tificates for that user. Registration begins the process of enrolling in a PKI. Registration usually involves some offline or online procedure for mutual authentication. Typically, the end entity is issued one or more shared secret keys used for subsequent authentication.
• Initialization: Before a client system can operate securely, it is necessary to install key materials that have the appropriate relationship with keys stored

elsewhere in the infrastructure. For example, the client needs to be securely initialized with the public key and other assured information of the trusted CA(s), to be used in validating certificate paths.
• Certification: This is the process in which a CA issues a certificate for a user’s public key, returns that certificate to the user’s client system, and/or posts that certificate in a repository.
• Key pair recovery: Key pairs can be used to support digital signature creation and verification, encryption and decryption, or both. When a key pair is used for encryption/decryption, it is important to provide a mechanism to recover the nec- essary decryption keys when normal access to the keying material is no longer possible, otherwise it will not be possible to recover the encrypted data. Loss of access to the decryption key can result from forgotten passwords/PINs, corrupted disk drives, damage to hardware tokens, and so on. Key pair recovery allows end entities to restore their encryption/decryption key pair from an authorized key backup facility (typically, the CA that issued the end entity’s certificate).
• Keypairupdate:Allkeypairsneedtobeupdatedregularly(i.e.,replacedwith a new key pair) and new certificates issued. Update is required when the cer- tificate lifetime expires and as a result of certificate revocation.
• Revocationrequest:AnauthorizedpersonadvisesaCAofanabnormalsitua- tion requiring certificate revocation. Reasons for revocation include private- key compromise, change in affiliation, and name change.
• Cross certification: Two CAs exchange information used in establishing a cross-certificate. A cross-certificate is a certificate issued by one CA to another CA that contains a CA signature key used for issuing certificates.

# Protocolos de Gerenciamento PKIX

PKIX Management Protocols
The PKIX working group has defines two alternative management protocols between PKIX entities that support the management functions listed in the preced- ing subsection. RFC 2510 defines the certificate management protocols (CMP). Within CMP, each of the management functions is explicitly identified by specific protocol exchanges. CMP is designed to be a flexible protocol able to accommodate a variety of technical, operational, and business models.
RFC 2797 defines certificate management messages over CMS (CMC), where CMS refers to RFC 2630, cryptographic message syntax. CMC is built on earlier work and is intended to leverage existing implementations. Although all of the PKIX func- tions are supported, the functions do not all map into specific protocol exchanges.

