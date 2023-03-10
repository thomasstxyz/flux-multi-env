# GitOps Multi-Env Config with Kustomize and Flux

## Bootstrap Flux

```bash
export GITHUB_TOKEN=<token>
export GITHUB_USER=<user>
export GITHUB_REPO=<repo>
```

```bash
flux bootstrap github \
--read-write-key \
--components-extra "image-reflector-controller,image-automation-controller" \
--owner=${GITHUB_USER} \
--repository=${GITHUB_REPO} \
--personal \
--path=clusters/dev
```
