# `mps.terminal` Ansible Collection

Terminal environment and per-user developer tooling — bash, vim, nvim,
tmux, kitty, fonts, python, rust, scripts, skeletons.

## Galaxy metadata

- **namespace**: `mps`
- **name**: `terminal`
- **version**: `0.3.1`
- **dependencies**: `mps.base`, `ansible.posix`

See [`galaxy.yml`](galaxy.yml) for the canonical values.

## Roles

| Role | Purpose |
|---|---|
| `mps.terminal.bash` | bash-completion, bash fun packages, system + per-user `.bashrc` and `.config/bashrc/`, legacy migration. |
| `mps.terminal.vim` | vim-nox + addons, lua dev packages, per-user `.vimrc` + `.NERDTreeBookmarks`. |
| `mps.terminal.nvim` | apt deps, upstream nvim tarball + symlink, npm tools, per-user python venv + pip + cargo, yazi. |
| `mps.terminal.tmux` | tmux + tmuxinator, per-user config trees. |
| `mps.terminal.kitty` | kitty package + `x-terminal-emulator` alternative + per-user `.config/kitty/`. |
| `mps.terminal.fonts` | Download → unzip → copy font archives + `fc-cache`. |
| `mps.terminal.python` | Per-user python venv with pip + linters, auto-activate in `.bashrc`. |
| `mps.terminal.rust` | rustup install per user, default stable toolchain, PATH/env in `.bashrc`. |
| `mps.terminal.scripts` | Per-user helper scripts in `~/.local/bin/`. |
| `mps.terminal.skeletons` | System-wide `/etc/mps/skeletons/`. |

## Installation

```bash
ansible-galaxy collection install mps.terminal
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
    - mps.base.identity
    - mps.terminal.bash
    - mps.terminal.python
    - mps.terminal.nvim
```

## Documentation

- [`AGENTS.md`](AGENTS.md) — developer conventions
- `roles/<role>/README.md` — per-role variable docs

## License

GPL-3.0-or-later
