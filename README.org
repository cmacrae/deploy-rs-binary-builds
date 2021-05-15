# Nightly [deploy-rs](https://github.com/serokell/deploy-rs) builds
[![.github/workflows/build.yaml](https://github.com/cmacrae/deploy-rs-binary-builds/actions/workflows/build.yaml/badge.svg)](https://github.com/cmacrae/deploy-rs-binary-builds/actions/workflows/build.yaml)
[![BuiltWithNix badge](https://img.shields.io/badge/Built_With-Nix-5277C3.svg?logo=nixos&labelColor=73C3D5)](https://builtwithnix.org)
[![Cachix badge](https://img.shields.io/badge/Cachix-store-blue.svg?logo=hack-the-box&logoColor=73C3D5)](https://app.cachix.org/cache/deploy-rs)

This repository provides nightly automated builds of [serokell/deploy-rs](https://github.com/serokell/deploy-rs) for:
- `x86_64-linux`
- `aarch64-linux`
- `x86_64-darwin`

Resulting builds are then pushed to a [binary cache](https://app.cachix.org/cache/deploy-rs) for convenience.

## Usage
```nix
{
  nix.binaryCaches = [
    "https://cachix.org/api/v1/cache/deploy-rs"
  ];

  nix.binaryCachePublicKeys = [
    "deploy-rs.cachix.org-1:M+ZN++7fdqZFeIsvJyqeQrgnAbgsPNuv8z93uAJO43w="
  ];
}
```
