# GigVault Organization Profile

[![Website](https://img.shields.io/badge/website-gigvault.github.io-00ff00?style=for-the-badge&logo=github)](https://gigvault.github.io/.github/)
[![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)](LICENSE)
[![Go](https://img.shields.io/badge/Go-1.23-00ADD8?style=for-the-badge&logo=go)](https://go.dev/)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-Ready-326CE5?style=for-the-badge&logo=kubernetes)](https://kubernetes.io/)

```
   ____  _       __     __          _ _   
  / ___(_) __ _\ \   / /_ _ _   _| | |_ 
 | |  _| |/ _` |\ \ / / _` | | | | | __|
 | |_| | | (_| | \ V / (_| | |_| | | |_ 
  \____|_|\__, |  \_/ \__,_|\__,_|_|\__|
          |___/                          
```

## 🔐 Enterprise Zero Trust PKI Ecosystem

GigVault is an **Enterprise Zero Trust PKI Ecosystem** built entirely in **Go 1.23**. It provides a complete Certificate Authority solution with modern security practices, Kubernetes-native deployment, and enterprise-grade features.

## 🌟 Key Highlights

- **🔒 Custom Envelope Encryption**: HSM-backed master key with database-stored encrypted DEKs
- **🛡️ Zero Trust Architecture**: JWT, RBAC, mTLS, TLS 1.3
- **⚡ Production Ready**: Kubernetes-native with Helm charts
- **🌐 Modern Admin UI**: Next.js 14 with dark/light mode
- **💰 Cost Effective**: Save $5K-20K/year vs commercial solutions
- **🚀 Easy Deployment**: One-command local deployment

## 📊 Project Stats

| Metric | Value |
|--------|-------|
| Repositories | 18 |
| Microservices | 14 |
| Programming Language | Go 1.23 |
| Frontend | Next.js 14 + TypeScript 5 |
| Database | PostgreSQL 15 |
| Container Orchestration | Kubernetes + Helm |
| Security Features | 20+ |
| Annual Cost Savings | $5K-20K |

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    GigVault Ecosystem                        │
├─────────────────────────────────────────────────────────────┤
│                                                              │
│  Root CA ──▶ CA (Core) ──▶ RA (Registry Authority)          │
│               │                                              │
│       ┌───────┼──────────┬──────────┬──────────┐            │
│       │       │          │          │          │            │
│   KeyMgr  Enroll      OCSP        CRL      Policy           │
│                                                              │
│   Auth    Audit      Notify       CLI    Admin UI          │
│                                                              │
│            PostgreSQL (Envelope Encryption)                  │
└─────────────────────────────────────────────────────────────┘
```

## 🚀 Quick Start

```bash
# Clone infrastructure repository
git clone https://github.com/gigvault/infra
cd infra

# Create local Kubernetes cluster
make kind-up

# Build and deploy all services
make build-all
make deploy-local

# Run smoke tests
make smoke-test
```

## 📦 Repositories

### Core Services
- **[rootca](https://github.com/gigvault/rootca)** - Offline Root Certificate Authority
- **[ca](https://github.com/gigvault/ca)** - Certificate Authority core service
- **[ra](https://github.com/gigvault/ra)** - Registration Authority
- **[keymgr](https://github.com/gigvault/keymgr)** - Key Management service

### Enrollment & Validation
- **[enroll](https://github.com/gigvault/enroll)** - Certificate enrollment (ACME/EST/SCEP)
- **[ocsp](https://github.com/gigvault/ocsp)** - OCSP responder
- **[crl](https://github.com/gigvault/crl)** - CRL distribution point

### Policy & Security
- **[policy](https://github.com/gigvault/policy)** - Policy engine
- **[auth](https://github.com/gigvault/auth)** - Authentication service (JWT + RBAC)
- **[audit](https://github.com/gigvault/audit)** - Audit logging service
- **[notify](https://github.com/gigvault/notify)** - Notification service

### Tools & Management
- **[cli](https://github.com/gigvault/cli)** - Command-line interface
- **[admin-ui](https://github.com/gigvault/admin-ui)** - Admin web interface (Next.js)
- **[operator](https://github.com/gigvault/operator)** - Kubernetes operator

### Infrastructure
- **[shared](https://github.com/gigvault/shared)** - Shared Go libraries
- **[infra](https://github.com/gigvault/infra)** - Kubernetes manifests, Helm charts, scripts
- **[docs](https://github.com/gigvault/docs)** - Documentation

## 🔒 Security Features

✅ **Cryptography**: ECDSA P-256/P-384, AES-256-GCM, TLS 1.3  
✅ **Authentication**: JWT (ECDSA P-256), RBAC, mTLS  
✅ **Infrastructure**: Network Policies, Pod Security Standards  
✅ **Audit**: Immutable logs, ECDSA-signed entries  
✅ **Storage**: Envelope encryption with HSM-backed master key  

## 💰 Cost Comparison

| Feature | GigVault | HashiCorp Vault | HSM |
|---------|----------|-----------------|-----|
| PKI Management | ✅ Built-in | Additional | N/A |
| Secrets Storage | ✅ Encrypted | ✅ Encrypted | N/A |
| Key Protection | ✅ HSM-backed | ✅ Encrypted | ✅✅ Tamper-proof |
| **Annual Cost** | **$0-1K** | $5K-15K | $10K-20K |

## 🛠️ Technology Stack

- **Backend**: Go 1.23, PostgreSQL 15, gRPC
- **Frontend**: Next.js 14, React 18, TypeScript 5, Tailwind CSS
- **Infrastructure**: Kubernetes, Helm 3, Docker, kind
- **CI/CD**: GitHub Actions, automated testing

## 📖 Documentation

- **Website**: [gigvault.github.io/.github](https://gigvault.github.io/.github/)
- **Architecture Docs**: [gigvault/docs](https://github.com/gigvault/docs)
- **Getting Started**: [infra/README.md](https://github.com/gigvault/infra/blob/main/README.md)
- **Security Audit**: [docs/SECURITY.md](https://github.com/gigvault/docs/blob/main/SECURITY.md)

## 🤝 Contributing

GigVault is an open-source project. Contributions are welcome!

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📄 License

All GigVault repositories are licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

## 🌟 Star Us!

If you find GigVault useful, please ⭐ star our repositories!

---

<div align="center">

**Built with ❤️ using Go**

[Website](https://gigvault.github.io/.github/) • 
[Documentation](https://github.com/gigvault/docs) • 
[Get Started](https://github.com/gigvault/infra)

</div>

