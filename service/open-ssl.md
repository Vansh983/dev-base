# OpenSSL Commands

## Overview
- [OpenSSL Commands](#openssl-commands)
  - [Overview](#overview)
  - [Installing OpenSSL](#installing-openssl)
  - [Checking OpenSSL Version](#checking-openssl-version)
  - [Generating a Private Key](#generating-a-private-key)
  - [Generating a CSR](#generating-a-csr)
  - [Generating a Self-Signed Certificate](#generating-a-self-signed-certificate)
  - [Viewing Certificate Details](#viewing-certificate-details)
  - [Converting Certificate Formats](#converting-certificate-formats)
  - [Encrypting a File](#encrypting-a-file)
  - [Decrypting a File](#decrypting-a-file)
  - [Creating a PFX File](#creating-a-pfx-file)
  - [Extracting Certificates from a PFX File](#extracting-certificates-from-a-pfx-file)
  - [Checking Certificate Expiration](#checking-certificate-expiration)
  - [Creating a Certificate Chain](#creating-a-certificate-chain)

## Installing OpenSSL

To install OpenSSL on macOS using Homebrew:

```sh
brew install openssl
```

## Checking OpenSSL Version

To check the version of OpenSSL installed:

```sh
openssl version
```

## Generating a Private Key

To generate a private key:

```sh
openssl genpkey -algorithm RSA -out private-key.pem -aes256
```

## Generating a CSR

To generate a Certificate Signing Request (CSR):

```sh
openssl req -new -key private-key.pem -out csr.pem
```

## Generating a Self-Signed Certificate

To generate a self-signed certificate:

```sh
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout private-key.pem -out certificate.pem
```

## Viewing Certificate Details

To view the details of a certificate:

```sh
openssl x509 -in certificate.pem -text -noout
```

## Converting Certificate Formats

To convert a certificate from PEM to DER format:

```sh
openssl x509 -outform der -in certificate.pem -out certificate.der
```

To convert a certificate from DER to PEM format:

```sh
openssl x509 -inform der -in certificate.der -out certificate.pem
```

## Encrypting a File

To encrypt a file:

```sh
openssl enc -aes-256-cbc -salt -in file.txt -out file.enc
```

## Decrypting a File

To decrypt a file:

```sh
openssl enc -aes-256-cbc -d -in file.enc -out file.txt
```

## Creating a PFX File

To create a PFX (PKCS#12) file:

```sh
openssl pkcs12 -export -out certificate.pfx -inkey private-key.pem -in certificate.pem -certfile ca-cert.pem
```

## Extracting Certificates from a PFX File

To extract certificates from a PFX file:

```sh
openssl pkcs12 -in certificate.pfx -out certificate.pem -nodes
```

## Checking Certificate Expiration

To check the expiration date of a certificate:

```sh
openssl x509 -enddate -noout -in certificate.pem
```

## Creating a Certificate Chain

To create a certificate chain file:

```sh
cat intermediate-cert.pem root-cert.pem > chain.pem
```