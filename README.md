# noctalia-fish

Noctalia Shell template for fish. Follows dark/light mode, updates open sessions live.

## Install

```fish
mkdir -p ~/.config/noctalia/templates ~/.config/fish/conf.d
cp fish.theme ~/.config/noctalia/templates/fish.theme
```

Add to `~/.config/noctalia/templates.toml`:

```toml
[theme.templates.user.fish]
input_path    = "$XDG_CONFIG_HOME/noctalia/templates/fish.theme"
output_path   = "$XDG_CONFIG_HOME/fish/conf.d/noctalia-theme.fish"
requires_path = "$XDG_CONFIG_HOME/fish"
post_hook     = "fish -c 'source $XDG_CONFIG_HOME/fish/conf.d/noctalia-theme.fish'"
hook_async    = false
```

Uses fish universal variables (`set -U`), which write to `~/.config/fish/fish_variables`. Gitignore it if you version your dotfiles.
