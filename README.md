# Continuum release workflow qualification snapshot

This repository mirrors, byte for byte, the reusable workflow
`.github/workflows/continuum-release.yml` from the audited Continuum change for
kodmial/continuum#472. It exists only so an isolated qualification consumer can
pin a `uses:` line to an exact commit before Continuum's own pull request is
merged.

The workflow checks out the release engine from `kodmial/continuum` at the
`continuum_ref` input; qualification uses the exact engine commit whose
`src/continuum/release/` bytes are identical to this change. This repository is
not a Continuum release channel and is not installed by `install.sh`.
