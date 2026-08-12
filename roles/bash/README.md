---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: terminal
role: bash
---

# `mps.terminal.bash`

Configure bash dotfiles per user

## Default variables

| Variable | Default | Description |
|---|---|---|
| `bash_enable_aliases` | `true` | Deploy system-wide alias files to /etc/bash_aliases.d/ |
| `bash_enable_bash_completion` | `true` | Install bash-completion package |
| `bash_enable_fun_packages` | `true` | Install bash_fun_packages (shell fun utilities) |
| `bash_fun_packages` | `[5 items]` | Apt packages providing shell fun utilities (cowsay, figlet, fortune, cmatrix, etc.) |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.terminal.bash
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 113
