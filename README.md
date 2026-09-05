# Vanilla OS KDE Image

Containerfile for building a Vanilla OS KDE image.

> [!CAUTION]
> This image is NOT officially maintained by Vanilla OS.

This image is based on top of [`vanillaos/core`](https://github.com/Vanilla-OS/core-image/pkgs/container/core) and offers the Vanilla OS Desktop experience with KDE.

## Build

```bash
vib build recipe.yml
podman image build -t vanillakde/kde .
```

## Verify Image Build Provenance Attestation

All the image builds/pushes are attested for build provenance and integrity using the [attest-build-provenance`](https://github.com/actions/attest-build-provenance) action. The attestations can be verified [here](https://github.com/Vanilla-KDE/desktop-image/attestations) or by having the latest version of [GitHub CLI](https://github.com/cli/cli/releases/latest) installed in your system. Then, execute the following command:

```sh
gh attestation verify oci://ghcr.io/vanilla-kde/kde:latest --owner Vanilla-KDE
```