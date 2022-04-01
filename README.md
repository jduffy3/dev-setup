# dev-setup

A ansible playbook to setup your shiny new (mac) laptop.

## Prerequisites

1. Install brew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> $HOME/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

2. `brew install ansible`

3. Setup ssh keys https://github.com/settings/keys

4. Run playbook

`ansible-playbook ansible-macos-setup.yml`
