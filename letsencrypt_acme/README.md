# Home Assistant Add-on: Letsencrypt

Let's Encrypt is a certificate authority that provides free X.509 certificates for Transport Layer Security encryption via an automated process designed to eliminate the hitherto complex process of manual creation, validation, signing, installation, and renewal of certificates for secure websites.

![Supports armv7 Architecture][armv7-shield]

Setting up Letsencrypt allows you to use validated certificates for your webpages and web-interfaces.
It requires you to own the domain you are requesting the certificate for.

The generated certificate can be used within others addons. By default the path and file for the certificates within other addons will refer to the files generated within this addon.

[acme.sh]: https://github.com/acmesh-official/acme.sh

[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
