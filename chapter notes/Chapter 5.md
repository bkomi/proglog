# Secure Your Services

- Taking security seriously from the beginning
- Tacking it later is a painful job


3 steps:
  1. encrypt data in-flight to prevent MITM attacks
     1. TLS successor to SSL
     2. TLS : mostly one-way auth authenticates the server
  2. authenticate to identify clients
     1. mutual TLS for authenticating both client and server. Usually used in machine-to-machine comm
  3. authorize to determine permissions of clients
     1. authorization is required for granular level-access of resources


CFSSL
- cfssl to sign, verify, and bundle TLS certificates and output the results as JSON.
- cfssljson to take that JSON output and split them into separate key, certificate, CSR, and bundle files.



TSL CA
- https://www.youtube.com/watch?v=r1nJT63BFQ0


Authorization
- Access Control Lists
  - (subject, action, resource, control)
  - casbin

