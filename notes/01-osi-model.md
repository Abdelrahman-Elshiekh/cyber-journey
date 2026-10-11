# Stage 1 — OSI Model Notes (Oct 10, 2026)

## What is the OSI model?
The OSI model stands for Open Systems Interconnection. It's a model that
helps people understand and talk about the different layers involved in
how two systems communicate over a network. Each layer does its own job,
and the layers work together in order to produce the final outcome
(data moving from one system to another).

## The seven layers
1. **Physical** — data is sent using cables or fiber.
2. **Data Link** — MAC addresses and switching happen here.
3. **Network** — IP addresses and routing happen here.
4. **Transport** — TCP and UDP control data delivery here.
5. **Session** — a session between two applications is initiated and managed here.
6. **Presentation** — the application's data gets encrypted/formatted here.
7. **Application** — the layer we actually interact with (the app itself).

## Where things map
- IP address → Layer 3 (Network)
- Port (e.g. 443) → Layer 4 (Transport)
- MAC address → Layer 2 (Data Link)
- TCP/UDP → Layer 4 (Transport)
- HTTP → Layer 7 (Application)
- TLS → Layer 6 (Presentation)

## Security connection
A security person benefits from knowing what each layer does because,
if something goes wrong, they can detect and fix it faster — e.g. a
networking problem points them to the network layer. More broadly, it
also tells you which attacks and tools belong to which layer: a DDoS
flood is usually a Layer 3/4 problem (firewalls, routers), SQL injection
or XSS is a Layer 7 problem (a firewall can't see it — you need a WAF
or app logs), and ARP spoofing is a Layer 2 problem invisible to
anything only watching IP addresses.