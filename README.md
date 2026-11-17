# Continuum release qualification snapshot

This repository mirrors, byte for byte, the audited Continuum change for
kodmial/continuum#472:

- `.github/workflows/continuum-release.yml` — the reusable release workflow;
- `src/continuum/` — the release engine and the modules it imports, including
  the binary-mode checksum fix that the earlier `c4ed841` qualification attempt
  proved was required on Windows.

The mirror exists only so an isolated qualification consumer can pin a `uses:`
line and a `continuum_ref` to exact commits before Continuum's own pull request
is merged. It is not a Continuum release channel and is not installed by
`install.sh`.

Provenance: the files were copied from the recovery worktree generation 3
(`dd986d8cb9bd8c0b38a514d8c40a8f4bbc6e1477`) plus the qualified fixes in this
change. The corresponding Continuum `src/` tree hash is recorded in
`QUALIFICATION.md` in the consumer repository.
