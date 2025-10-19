# jalbfil.github.io · DID host (`did:web`)

Este repositorio sirve el DID Document público del emisor del TFG **tfg-dap** usando el método `did:web`.

- **DID**: `did:web:jalbfil.github.io`
- **DID Document**: `https://jalbfil.github.io/.well-known/did.json`

## ¿Para qué se usa?
El verificador del MVP (tfg-dap) resuelve este `did.json` para obtener la **JWK pública** del emisor y validar la firma RS256 de las credenciales (VC-JWT).

## Rotación de claves (resumen)
1. Generar un nuevo par de claves **fuera** de los repos:
   ```bash
   openssl genrsa -out issuer_private.pem 2048
   openssl rsa -in issuer_private.pem -pubout -out issuer_public.pem
