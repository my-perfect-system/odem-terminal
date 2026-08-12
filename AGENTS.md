# AGENTS.md — odem-terminal

Shell and editor environment — bash, vim, nvim, tmux, kitty, fonts,
python, rust, scripts, skeletons. Mostly per-user (filtered via
`odem_filter_users('terminal_<X>')`).

## Galaxy

- **namespace**: `odem`
- **name**: `terminal`
- **version**: `0.3.1`
- **dependencies**: `odem.base >=0.1.0`, `ansible.posix >=1.0.0`

## Roles

| Role | Description | Complexity |
|---|---|---|
| `odem.terminal.bash` | bash-completion (optional), bash fun packages, system bash aliases (in `/etc/bash_aliases.d/`), per-user `.bashrc` and `.config/bashrc/`, legacy migration (`.bash_logout`, `.bash_history`, `.bash_aliases` cleanup). | 2 |
| `odem.terminal.vim` | vim-nox + addons (optional), lua dev packages (optional), per-user `.vimrc` + `.NERDTreeBookmarks`. | 1 |
| `odem.terminal.nvim` | apt deps, upstream nvim tarball + symlink, npm tools, per-user python venv + pip + cargo, yazi download/extract/install. | 3 (accepted) |
| `odem.terminal.tmux` | tmux + tmuxinator packages, per-user `.config/tmux/` and `.config/tmuxinator/` config trees. | 1 |
| `odem.terminal.kitty` | kitty package, `x-terminal-emulator` alternative registration, per-user `.config/kitty/` config tree. | 1 |
| `odem.terminal.fonts` | Download → unzip → copy font archives into `/usr/local/share/fonts/`, trigger `fc-cache` handler. | 3 (accepted) |
| `odem.terminal.python` | python3 + venv + packaging packages. Per-user `.venvs/default/` with pip + setuptools + black + ruff + pylint, auto-activate in `.bashrc`. | 2 |
| `odem.terminal.rust` | clang (for cargo), rustup installer, per-user rustup install (with optional clean-reinstall), default toolchain `stable`, PATH + `source $HOME/.cargo/env` in `.bashrc`, ownership sweep on `.cargo` + `.rustup`. | 2 |
| `odem.terminal.scripts` | Per-user helper scripts in `~/.local/bin/` (recursively chmod'd). | 1 |
| `odem.terminal.skeletons` | System-wide `/etc/mps/skeletons/` directory with static files deployed via `copy`. | 1 |

## Conventions

- All per-user loops use `loop: "{{ identity_users_resolved | odem_filter_users('terminal_<x>') }}"`.
- `bash` and `python` and `rust` and `nvim` are full single-file `tasks/main.yml` (no install/configure/tools sub-step).
- `vim` and `tmux` and `kitty` and `fonts` and `scripts` and `skeletons` are single-file roles (small enough).
- Toggle variables prefixed `bash_enable_*`, `nvim_enable_*`, `rust_enable_*`, `vim_enable_*`, `kitty_enable_*` — gate individual tasks.
