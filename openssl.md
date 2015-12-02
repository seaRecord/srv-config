# openssl

### Key.pem & cert.pem

The two files you need are a PEM encoded SSL certificate and private key. PEM encoded certs and keys are Base64 encoded text with start/end delimiters that look like -----BEGIN RSA PRIVATE KEY----- or similar.

To create an SSL certificate you first need to generate a private key and a certificate signing request, or CSR (which also contains your public key).You can do this in a variety of ways, but here's how in OpenSSL.

`openssl req -newkey rsa:2048 -new -nodes -keyout key.pem -out csr.pem`

This will cause you to enter an interactive prompt to generate a 2048-bit RSA private key and a CSR that has all the information you choose to enter at the prompts. (Note: Common Name is where you'll want to put the domain name you'll be using to access your site.) Once you've done this you would normally submit this CSR to a trusted certificate authority and once they've validated your request you would receive a certificate.

If you don't care about your certificate being trusted (usually the case for development purposes) you can just create a self-signed certificate. To do this, we can use almost the same line, but we'll pass two extra parameters.

`openssl req -newkey rsa:2048 -new -nodes -x509 -days 3650 -keyout key.pem -out cert.pem`

This will give you a cert (valid for 10 years) and key pair that you can use in the code snippet you posted.
