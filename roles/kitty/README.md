---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: terminal
role: kitty
---

# `mps.terminal.kitty`

Configure kitty terminal emulator per user

## Default variables

| Variable | Default | Description |
|---|---|---|
| `kitty_enable_alternatives` | `true` | Set kitty as default x-terminal-emulator via update-alternatives |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.terminal.kitty
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 28
