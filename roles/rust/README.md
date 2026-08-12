---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: terminal
role: rust
---

# `mps.terminal.rust`

Install and configure Rust toolchain (rustup, cargo, CLI tools)

## Default variables

| Variable | Default | Description |
|---|---|---|
| `rust_enable_toolchain_reinstall` | `false` | Nuke ~/.rustup/toolchains and reinstall Rust toolchain from scratch |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.terminal.rust
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 108
