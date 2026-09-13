# 02 — Containers

## 🟢 Beginner

- Why containers exist
- Containers vs virtual machines
- Docker CLI
- Dockerfile
- Images and containers
- Ports
- Volumes
- Networks
- Registries

## 🟡 Intermediate

- Layers and cache
- Multi-stage builds
- Build contexts
- Health checks
- Resource limits
- Image tagging
- Private registries
- Container networking
- Compose concepts

## 🔴 Advanced

- OCI image/runtime concepts
- Container namespaces and cgroups
- Rootless containers
- Minimal images
- Runtime hardening
- Image provenance
- SBOMs and signatures

## 🟣 Security checklist

- Run as non-root
- Pin important dependencies
- Scan images
- Minimize packages
- Never bake secrets into images
- Use read-only filesystems where practical
- Drop unnecessary Linux capabilities
- Verify image provenance

## 🛠️ Lab

1. Containerize a small application.
2. Reduce image size with multi-stage builds.
3. Run as a non-root user.
4. Scan the image with Trivy.
5. Generate an SBOM with Syft.
6. Sign and verify the image with Cosign.
