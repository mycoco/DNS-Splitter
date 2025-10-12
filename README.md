DNS-Splitter

DNS-Splitter is a Windows client-side intelligent DNS and proxy splitter designed to improve productivity in complex multi-environment network scenarios.
It provides a flexible and efficient way to manage multiple proxy and DNS routing strategies under an HTTP proxy mode.

<img width="973" height="835" alt="image" src="https://github.com/user-attachments/assets/d98d5029-b022-4b96-b4fe-fdc5c9e0ee22" />


🚀 Features

Smart DNS & Proxy Splitting
Dynamically route traffic to different DNS servers or proxy endpoints based on domain rules or hosts configuration.

Multi-Environment Access
Easily access multiple environments (e.g., test, staging, production) for the same domain without switching configurations manually.

HTTP Proxy Based
Works entirely under an HTTP proxy mode, compatible with browsers and most client applications.

Local & Secure
Runs locally on Windows with optional TLS support, certificate management, and user authentication.

Flexible Configuration
Supports rule-based routing, multiple accounts, and granular access control.

💡 Typical Use Case

Imagine you are developing or debugging across several environments:

Environment	Domain	Target
Production	api.company.com	10.10.1.10
Test Env 1	api.company.com	10.10.2.20
Test Env 2	api.company.com	10.10.3.30

With DNS-Splitter, you can access all of them at the same time without changing system DNS or proxy settings — simply define your rules, and it just works.

⚙️ Key Capabilities

Intelligent DNS routing

HTTP/HTTPS proxy forwarding

Multiple upstream DNS/DoH servers

Per-domain proxy rules

Auto TLS certificate generation

Optional username/password authentication

Hosts-like static overrides
