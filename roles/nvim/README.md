---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: terminal
role: nvim
---

# `mps.terminal.nvim`

Install and configure Neovim with dependencies

## Default variables

| Variable | Default | Description |
|---|---|---|
| `nvim_enable_apt_deps` | `true` | Install apt dependencies for Neovim |
| `nvim_enable_fd` | `true` | Install fd-find apt package |
| `nvim_enable_npm_tools` | `true` | Install npm tools for Neovim |
| `nvim_enable_tarball` | `true` | Install Neovim tarball |
| `nvim_enable_tree_sitter` | `true` | Install tree-sitter-cli npm package |
| `nvim_enable_yazi` | `true` | Download and install yazi from GitHub releases |
| `nvim_yazi_version` | `v26.5.6` | Yazi release version tag to download |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.terminal.nvim
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 212
