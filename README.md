# Homebrew tap for Open Walnut

```bash
brew install evanzhang008/tap/open-walnut
walnut web
```

Then open http://localhost:3456. Walnut runs its sessions with
[Claude Code](https://claude.com/product/claude-code).

`Formula/open-walnut.rb` is a copy of the `open-walnut.rb` attached to the newest
[Open Walnut release](https://github.com/EvanZhang008/open-walnut/releases). That release's
workflow writes it from the release's own archives, installs it with brew and runs `brew test`
before attaching it; `.github/workflows/follow.yml` here only copies it, every hour. Do not
edit the formula by hand: the next release replaces it.

The formula installs the release's self-contained archive (its own Node inside) and needs
nothing else. Walnut keeps itself up to date when it starts; `brew upgrade open-walnut` works
too.

Without Homebrew: `curl -fsSL https://github.com/EvanZhang008/open-walnut/releases/latest/download/install.sh | sh`
