# prj

**prj** is a CLI utility for quickly jumping between your Git project directories using [fd](https://github.com/sharkdp/fd) and [fzf](https://github.com/junegunn/fzf).

## Features

- Fuzzy search your Git project folders with `fzf`
- Automatically detects projects by searching for `.git` directories
- Simple command-line interface with help and version flags

## Installation

macOS:

```sh
brew tap mattmc3/tools
brew install prj
```

Make sure you have [fd](https://github.com/sharkdp/fd) and [fzf](https://github.com/junegunn/fzf) installed.

### Shell Setup

Initialize prj in your shell's config file:

**Fish:**
```fish
# ~/.config/fish/config.fish
prj -i fish | source
```

**Bash/Zsh:**
```bash
# ~/.bashrc or ~/.zshrc
eval "$(prj -i sh)"
```

## Usage

```sh
prj [-h] [-i <shell>] [-v] [<query>]
```

**Options:**
- `-h` - Show help message
- `-i <shell>` - Output shell initialization code (sh, bash, zsh, or fish)
- `-v` - Show version information
- `<query>` - Optional search query to filter projects

## Examples

```sh
# Interactive selection
prj

# Search with a query
prj myproject

# Generate shell initialization
prj -i fish
prj -i sh
```

## Configuration

By default, `prj` searches for projects in `$HOME/Projects`.
You can override this by setting the `PRJ_DIR` environment variable:

```fish
set -gx PRJ_DIR /path/to/your/projects
```

## License

MIT License

---

Inspired by project jumpers in other shells.
