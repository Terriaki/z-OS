Certificate Generation and renewal process on z/OS

This document outlines the process for generating a new digital certificate on IBM z/OS using RACF or an equivalent security product. These steps include certificate and key generation, CSR creation, optional keyring setup, and importing the signed certificate.

Steps:
1. Generate a New Certificate with Private Key
Start by generating a new self-signed certificate that includes a private key.
2. Generate a Certificate Signing Request (CSR)
Once the certificate and key are created, generate a CSR to send to a Certificate Authority (CA) for signing. This step will be different for each customer, follow your internal processes.
3. Create a Keyring (Optional)
If you don't already have a keyring or wish to use a new one.
4. Import Signed Certificate
Once you receive the signed certificate (and optionally the CA certificates), upload them to dataset and import to RACF.
5. Connect Certificate to Keyring
Now link the certificate and any CA certificates to the keyring.

Notes:
If you are renewing an old certificate, note it's DEFAULT status keyring.
Product using this new certificate might require to be pointed to the new label, either directly in the application, or in AT-TLS Pagent config. Refer to the application and your installation specifics.

Examples are jobs using IKJEFT01 program to issue RACF TSO commands 
