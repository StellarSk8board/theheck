# TheHeck

**Magnificent app which corrects your previous console command.**

*A family-friendly fork of [TheFuck](https://github.com/nvbn/thefuck) by Vladimir Iakovlev.*

![TheHeck in action](example.gif)

## What is this?

TheHeck is a command-line tool that automatically corrects your previous console command when you make a typo or mistake. Just type `heck` after a failed command, and it suggests the fix.

```bash
➜ git brnch
git: 'brnch' is not a git command. See 'git --help'.

Did you mean this?
    branch

➜ heck
git branch [enter/↑/↓/ctrl+c]
* main
```

## Why "TheHeck"?

Same great functionality as TheFuck, but with a name you can use:
- In professional environments
- In educational settings  
- Around kids
- In screen recordings and tutorials

## Installation

```bash
pip install theheck
```

Or via Homebrew (once published):
```bash
brew install theheck
```

## Setup

Add this to your `.bashrc`, `.zshrc`, or shell config:

```bash
eval $(theheck --alias)
```

Or with a custom alias:
```bash
eval $(theheck --alias OOPS)
```

Then restart your shell or run `source ~/.bashrc`.

## Usage

After a failed command, just type:
```bash
heck
```

Or use your custom alias.

### Options

- `heck -y` / `heck --yeah` - Run the fix without confirmation
- `heck -r` - Fix recursively until success
- `theheck --version` - Show version

## How It Works

TheHeck matches your failed command against a set of rules and suggests corrections. Rules exist for:

- **Git** - branch names, push/pull, stash, remote
- **Package managers** - apt, brew, pip, npm, cargo
- **Shell** - cd, ls, cat, chmod, mkdir
- **Languages** - python, go, cargo, lein
- **And many more...**

## Configuration

Create `~/.config/theheck/settings.py`:

```python
# Require confirmation before running (default: True)
require_confirmation = True

# Number of seconds to wait for commands (default: 3)
wait_command = 3

# Custom rules to exclude
excluded_rules = ['git_push']
```

## Contributing

Contributions welcome! This is an open-source project under the MIT license.

1. Fork it
2. Create your feature branch (`git checkout -b feature/amazing`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing`)
5. Open a Pull Request

## Credits

- **Original Author:** Vladimir Iakovlev ([@nvbn](https://github.com/nvbn))
- **Original Project:** [TheFuck](https://github.com/nvbn/thefuck)
- **Fork Maintainer:** Blair ([@StellarSk8board](https://github.com/StellarSk8board))

## License

MIT License - see [LICENSE.md](LICENSE.md)

This is a fork of TheFuck. The original copyright and license remain in effect.

---

*"What the heck just happened?" - Everyone, before discovering TheHeck*
