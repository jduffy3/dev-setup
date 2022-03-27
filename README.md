# dev-setup

## Prerequisites

0. Install brew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/james/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

1. Install command line tools

xcode-select --install

2. Install ansible

```bash
python3 -m pip install --upgrade pip
python3 -m pip install --user ansible
./Library/Python/3.8/bin/ansible
./Library/Python/3.8/bin/ansible-galaxy collection install community.general
```

3. Setup key

```bash
ssh-keygen -t ed25519 -C "user@email.com"
start ssh-agent in background
eval "$(ssh-agent -s)"
touch ~/.ssh/config

cat << EOF > ~/.ssh/config
Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519
EOF
```

ssh-add -K ~/.ssh/id_ed25519

pbcopy < ~/.ssh/id_ed25519.pub

Setup ssh keys
	https://github.com/settings/keys

## Run playbook

`./Library/Python/3.8/bin/ansible-playbook ansible-macos-setup.yml`
