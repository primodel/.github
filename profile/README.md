## Primodel

Primodel is a governed canonical data platform. It decouples the systems you buy from the systems you
build: data arrives from vendor systems, is mapped to a canonical information model, and is delivered
onward — so replacing an HR, finance or ordering system does not break everything downstream.

It runs **on your own infrastructure**, including **air-gapped** environments. A single container image
carries the API, the web UI and the bundled adapters.

- **[primodel.io](https://primodel.io)** — product, docs and pricing
- **[Security](https://primodel.io/security/)** — vulnerability reporting, SBOMs, VEX, support period
- **[get-started](https://github.com/primodel/get-started)** — Docker Compose and cloud blueprints
- **[releases](https://github.com/primodel/releases)** — changelog, SBOMs and the signing key

### Verify an image

Every image is signed. From **v3.1.2** onward it also carries a key-based signature, which verifies with
no network access to Sigstore — the case that matters when mirroring into an air-gapped registry:

```bash
curl -fsSLO https://raw.githubusercontent.com/primodel/releases/main/primodel.pub
cosign verify --key primodel.pub ghcr.io/primodel/primodel:<version>
```

### Reporting a vulnerability

With a GitHub account, [report privately on GitHub](https://github.com/primodel/releases/security/advisories/new).
Without one, email **security@primodel.io**. Please do not use public issues.
