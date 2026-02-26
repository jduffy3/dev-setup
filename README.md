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

Early in the run the playbook prompts once for your macOS password so Docker Desktop (installed via Homebrew Cask) can run its privileged post-install steps. If you do **not** want an interactive prompt, export `HOMEBREW_CASK_PASSWORD` with the same password before running Ansible.
