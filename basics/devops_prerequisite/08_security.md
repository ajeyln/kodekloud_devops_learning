<h1 align="center"> SSL & TLS Basics </h1>

### TLS Certificate

When a user tries to access a web server, TLS certificates ensure that the communication <br />
between user and the server is encrypted and the server.

### Encryption Methods

+ Symmetric Encryption : It is a secure way of encryption, which uses the same key to encrypt and decrypt the data

+ Asymmetric Encryption : It uses a pair of ofkeys. i.e, A private key and a public key.

* To generate keys **ssh-keygen** 
which genearetes **id_rsa** - private key, **id_rsa.pub** - public key
* locking the public key by configuring conf file (cat ~/.ssh/authorized_keys)

+ CA (Certificate authorities) will provide the verified certificate by signing on it. 
+ When we generate a certifcate signing request or CSR using the generated key and domain name of the website.
**openssl req -new  -key <DOMAIN_NAME>.key -out <DOMAIN_NAME>.csr**
+ Browser are generate the public keyfor CA's and verify that the certification is validated by correct CAs.

### Labs

1. SSL-TLS - Question related Symmetric and asymmetric encryption, generating keys etc.