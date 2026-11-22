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

`frontseat` follows upstream's releases directly, whether or not
ai-1st/hyperdx has synced yet: a new release is its tag
(`@hyperdx/app@X.Y.Z` in hyperdxio/hyperdx) merged into `frontseat`, then
`vX.Y.Z-frontseat.1` tagged. Changes to the sign-in go to ai-1st/hyperdx as
pull requests as well, so the fork carries as little of its own as it can.
