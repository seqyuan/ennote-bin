# ennote-bin
Ennote runtime binaries (ennogate + ennoworker), downloaded on demand by @seqyuan/ennote CLI

## How a release lands here

Binaries are built and tested in the private source repository
[`seqyuan/ennote`](https://github.com/seqyuan/ennote), then mirrored into a release
here by that repository's `release.yml`. This repository's
[`.github/workflows/attest.yml`](.github/workflows/attest.yml) attests the assets it
received, because GitHub only signs attestations for workflows in a public
repository.

Verify a downloaded binary:

```bash
gh attestation verify ennogate-linux-x64 --repo seqyuan/ennote-bin
```

The launcher `@seqyuan/ennote` downloads from
`https://github.com/seqyuan/ennote-bin/releases/download/<tag>/<asset>`.
