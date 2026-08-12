---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: terminal
role: fonts
---

# `mps.terminal.fonts`

Install and register Nerd Fonts and other TTF fonts

## Default variables

| Variable | Default | Description |
|---|---|---|
| `fonts_dir` | `/usr/share/fonts` | System font directory where downloaded fonts are installed |
| `fonts_list` | `- creates: '{{ fonts_dir }}/JetBrainsMono/JetBrainsMonoNerdFont-Regular.ttf'<br>  dst_unzip_path: '{{ fonts_dir }}/JetBrainsMono'<br>  name: JetBrainsMono<br>  url: https://github.com/ryanoasis/nerd-fonts/releases/download/v3.1.1/JetBrainsMono.zip<br>- dst_unzip_path: '{{ fonts_dir }}/codicon'<br>  file_only: true<br>  name: codicon<br>  url: https://github.com/microsoft/vscode-codicons/releases/download/0.0.36/codicon.ttf` | List of fonts to download and install |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.terminal.fonts
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 95

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
