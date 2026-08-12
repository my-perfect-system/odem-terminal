---
namespace: odem
collection: terminal
role: nvim
---

# `odem.terminal.nvim`

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

- `odem.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - odem.terminal.nvim
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 212

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
