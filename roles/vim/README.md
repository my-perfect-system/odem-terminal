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
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 64
