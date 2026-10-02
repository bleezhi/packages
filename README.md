# bleelinux packages

Static package lanes for [bleep](../bleelinux) (the Bleelinux package manager).

Each lane is a GitHub Release holding `*.bleepkg` files plus
`index.json.zst` / `packages.json` indexes:

```
https://github.com/bleezhi/packages/releases/download/<lane>/index.json.zst
```

Wire it up:

```sh
bleep repo add core https://github.com/bleezhi/packages/releases/download/core-x86_64-glibc
bleep repo refresh
bleep search hello
```

Lanes are published by the `packages` workflow (manual dispatch) or
`repos/publish.sh --upload` from the distro repo.
