# startship

```bash
└> cat ~/.config/starship.toml
# Inserts a blank line between shell prompts

format = """
[┌───────────────────>](bold green)
[│](bold green)$memory_usage$battery
[│](bold green)$aws
[│](bold green)$kubernetes
[│](bold green)$directory$python$git_branch$git_state$git_status$cmd_duration
[└>](bold green) """

add_newline = true

[memory_usage]
disabled = false
threshold = -1
#symbol = " "
style = "bold dimmed green"

[kubernetes]
format = 'on [⛵ $context \($namespace\)](green blue) '
disabled = false
[kubernetes.context_aliases]
"dev.local.cluster.k8s" = "dev"

[git_branch]
symbol = "🌱 "
truncation_length = 10
truncation_symbol = ""

[python]
symbol = "👾 "
pyenv_version_name = true

[battery]
full_symbol = "🔋 "
charging_symbol = "⚡️ "
discharging_symbol = "💀 "
```
