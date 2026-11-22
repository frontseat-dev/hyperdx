# Frontseat's build of HyperDX

This is [ai-1st/hyperdx](https://github.com/ai-1st/hyperdx) (upstream
HyperDX with OpenID Connect sign-in and users created on first sign-in),
as the [Frontseat](https://github.com/frontseat-dev) fleet runs it. MIT,
like upstream; upstream's licence and notices are unchanged.

- `main` follows ai-1st/hyperdx and is left as it is.
- `frontseat` is `main` plus `.github/workflows/frontseat-image.yml`.
- A tag `vX.Y.Z-frontseat.N` on `frontseat` publishes the all-in-one image
  with authentication, for linux/amd64 and linux/arm64, as
  `ghcr.io/frontseat-dev/hyperdx:X.Y.Z-frontseat.N`.

A new upstream release: sync `main` from ai-1st/hyperdx (which follows
hyperdxio/hyperdx), merge it into `frontseat`, tag. Fixes to the sign-in go
to ai-1st/hyperdx as pull requests, not here.
