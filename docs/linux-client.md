# Using this catalog from Linux

The `saintromuald/MechabellumMods` fork exists so the Linux client developed in
[`saintromuald/MechabellumModManager`](https://github.com/saintromuald/MechabellumModManager/tree/linux-port/linux)
can be pointed at a catalog under our control. The catalog format is unchanged;
this branch is a straight mirror of upstream `llxlzx/MechabellumMods`.

The native client defaults to upstream. To use this fork instead:

```bash
MBMM_CATALOG_BASE="https://raw.githubusercontent.com/saintromuald/MechabellumMods/master/" \
  mbmm catalog --refresh
```

Everything in `catalog.json` — `parts`, `bundle`, `sha256`, `size`,
`removedSigned` — is consumed as-is. Keep this fork synced with upstream before
relying on it; mod binaries are still fetched from the paths listed in the
catalog.
