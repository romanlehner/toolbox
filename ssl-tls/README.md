# SSL/TLS

## Manage certificates with `openSSL`

Create a self signed certificate with CSR and private key:

    openssl x509 -req -in <csr-file> -signkey <private-key-file> -days 1 -out cert.pem

Convert a certificate from PEM to DER format:

    openssl x509 -in <pem-certificate-file> -out <der-certificate-file> -outform DER

Get certificate from server:

    openssl s_client -showcerts -connect <domain>:443

Decode certificate:

    openssl x509 -in <certificate-file> -text -noout
    
