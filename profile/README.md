# 🔐 GigVault - Next-Generation PKI Ecosystem

A complete, production-grade Certificate Authority platform built in Go 1.23, deployable on Kubernetes.

## 🌟 Overview

GigVault is a microservices-based PKI ecosystem featuring:

- ✅ **17 Services** - Fully modular architecture
- 🔒 **ECDSA-First** - P-256/P-384 for modern cryptography
- ☸️ **Kubernetes-Native** - Deploy anywhere with Kubernetes
- 🚀 **Production-Ready** - Complete with CI/CD, monitoring, and HA
- 📚 **Comprehensive Docs** - Architecture, operations, and API references

## 📦 Repositories

### Core PKI Services
- [`rootca`](https://github.com/gigvault/rootca) - Offline Root CA tools
- [`ca`](https://github.com/gigvault/ca) - Intermediate Certificate Authority
- [`ra`](https://github.com/gigvault/ra) - Registration Authority

### Key Management & Enrollment
- [`keymgr`](https://github.com/gigvault/keymgr) - Key lifecycle management
- [`enroll`](https://github.com/gigvault/enroll) - ACME/EST/SCEP protocols

### Revocation Services
- [`ocsp`](https://github.com/gigvault/ocsp) - OCSP responder
- [`crl`](https://github.com/gigvault/crl) - CRL generator/publisher

### Policy & Security
- [`policy`](https://github.com/gigvault/policy) - Certificate policy engine
- [`auth`](https://github.com/gigvault/auth) - Authentication (OIDC/JWT)
- [`audit`](https://github.com/gigvault/audit) - Immutable audit logging
- [`notify`](https://github.com/gigvault/notify) - Notifications (email/Slack)

### Developer Tools
- [`cli`](https://github.com/gigvault/cli) - Operator CLI (`gigvault` command)
- [`admin-ui`](https://github.com/gigvault/admin-ui) - React admin dashboard

### Infrastructure
- [`operator`](https://github.com/gigvault/operator) - Kubernetes operator
- [`infra`](https://github.com/gigvault/infra) - Helm charts, deployment scripts
- [`shared`](https://github.com/gigvault/shared) - Common Go utilities library

### Documentation
- [`docs`](https://github.com/gigvault/docs) - Architecture, guides, API docs

## 🚀 Quick Start

```bash
# Clone infrastructure repo
git clone https://github.com/gigvault/infra.git
cd infra

# Bootstrap local environment
make kind-up
make build-all
make deploy-local
make smoke-test
```

## 📚 Documentation

- [Architecture](https://github.com/gigvault/docs/blob/main/architecture/ARCHITECTURE.md)
- [Local Bootstrap Guide](https://github.com/gigvault/docs/blob/main/guides/BOOTSTRAP_LOCAL.md)
- [Operations Manual](https://github.com/gigvault/docs/blob/main/guides/OPSEC.md)

## 🤝 Contributing

We welcome contributions! Please see individual repository CONTRIBUTING.md files.

## 📄 License

Copyright © 2025 GigVault. All rights reserved.

---

**Status**: ✅ Production-Ready | **Version**: 1.0.0 | **Go**: 1.23

