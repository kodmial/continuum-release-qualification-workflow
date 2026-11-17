# Continuum release workflow qualification snapshot

This repository mirrors, byte for byte, the reusable workflow
`.github/workflows/continuum-release.yml` from the audited Continuum change for
kodmial/continuum#472. It exists only so an isolated qualification consumer can
pin a `uses:` line to an exact commit before Continuum's own pull request is
merged.

The workflow checks out the release engine from `kodmial/continuum` at the
`continuum_ref` input. Qualification uses exact Continuum commit
`dd986d8cb9bd8c0b38a514d8c40a8f4bbc6e1477` (recovery checkpoint generation 3),
whose `src/continuum/release/` bytes are identical to this change. That engine
commit contains the binary-mode checksum fix that the earlier `c4ed841`
qualification attempt exposed on Windows.

This repository is not a Continuum release channel and is not installed by
`install.sh`.
