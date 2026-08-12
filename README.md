# `odem.terminal` Ansible Collection

Terminal environment and per-user developer tooling — bash, vim, nvim,
tmux, kitty, fonts, python, rust, scripts, skeletons.

## Galaxy metadata

- **namespace**: `odem`
- **name**: `terminal`
- **version**: `0.3.1`
- **dependencies**: `odem.base`, `ansible.posix`

See [`galaxy.yml`](galaxy.yml) for the canonical values.

## Roles

| Role | Purpose |
|---|---|
| [`odem.terminal.bash`](roles/bash/README.md) | bash-completion, bash fun packages, system + per-user `.bashrc` and `.config/bashrc/`, legacy migration. |
| [`odem.terminal.vim`](roles/vim/README.md) | vim-nox + addons, lua dev packages, per-user `.vimrc` + `.NERDTreeBookmarks`. |
| [`odem.terminal.nvim`](roles/nvim/README.md) | apt deps, upstream nvim tarball + symlink, npm tools, per-user python venv + pip + cargo, yazi. |
| [`odem.terminal.tmux`](roles/tmux/README.md) | tmux + tmuxinator, per-user config trees. |
| [`odem.terminal.kitty`](roles/kitty/README.md) | kitty package + `x-terminal-emulator` alternative + per-user `.config/kitty/`. |
| [`odem.terminal.fonts`](roles/fonts/README.md) | Download → unzip → copy font archives + `fc-cache`. |
| [`odem.terminal.python`](roles/python/README.md) | Per-user python venv with pip + linters, auto-activate in `.bashrc`. |
| [`odem.terminal.rust`](roles/rust/README.md) | rustup install per user, default stable toolchain, PATH/env in `.bashrc`. |
| [`odem.terminal.scripts`](roles/scripts/README.md) | Per-user helper scripts in `~/.local/bin/`. |
| [`odem.terminal.skeletons`](roles/skeletons/README.md) | System-wide `/etc/mps/skeletons/`. |

## Installation

```bash
ansible-galaxy collection install odem.terminal
```

## Usage

```yaml
- hosts: all
  become: true
  vars:
    users_catalog:
      alice:
        shell: /bin/bash
        user_roles:
          terminal_bash: true
          terminal_python: true
          terminal_nvim: true
  roles:
    - odem.base.identity
    - odem.terminal.bash
    - odem.terminal.python
    - odem.terminal.nvim
```

## Documentation

- [`AGENTS.md`](AGENTS.md) — developer conventions
- `roles/<role>/README.md` — per-role variable docs

## License

GPL-3.0-or-later
