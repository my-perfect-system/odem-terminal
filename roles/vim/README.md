---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: terminal
role: vim
---

# `mps.terminal.vim`

Configure vim dotfiles per user

## Default variables

| Variable | Default | Description |
|---|---|---|
| `vim_enable_lua` | `true` | Install lua development packages |
| `vim_enable_vim_nox` | `true` | Install vim-nox and vim plugin packages |
| `vim_enable_xclip` | `true` | Install xclip package |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.terminal.vim
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 64

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
