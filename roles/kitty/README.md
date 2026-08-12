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
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 28

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
