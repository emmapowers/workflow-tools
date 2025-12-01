# wt - Git Worktree Manager

CLI tool for managing git worktrees with interactive selection and fuzzy search.

## Installation

```bash
pixi run install    # Builds and installs to ~/.local/bin/wt
wt install          # Set up shell integration (cd support + completions)
```

## Usage

```bash
wt                  # Interactive picker to switch worktrees
wt create           # Interactive branch picker
wt create <name> -b <branch>  # Non-interactive
wt pr               # Pick from open PRs
wt fork <name>      # Fork from current branch
wt list             # List worktrees
wt remove           # Interactive picker
wt remove <name>    # Remove specific worktree
wt claude           # Interactive picker, open Claude Code
wt claude <name>    # Open Claude Code in worktree
wt path <name>      # Print worktree path
```

### Aliases

| Command | Alias |
|---------|-------|
| `create` | `cr` |
| `switch` | `sw` |
| `list` | `ls` |
| `remove` | `rm` |
| `fork` | `fk` |
| `claude` | `c` |

## Shell Integration

Run `wt install` to enable:
- Auto-cd to worktree after `create`, `pr`, `fork`, `switch`
- Tab completions for commands, worktree names, and branches

Worktrees are created at `repo.worktrees/<name>` (sibling to main repo).
