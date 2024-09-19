## Getting Started
```bash
ssh-keygen -t ed25519 -C "harx-dev@example.com" -f ~/.ssh/id_ed25519_harx-dev
```

## Add SSH Keys to SSH Agent
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519_harshathkulal
```

## Create an SSH Config File
```bash
nano ~/.ssh/config

```

## Update SSH Configuration
```bash
# First GitHub account
Host github-first
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_first_github

# Second GitHub account
Host github-second
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_ed25519_second_github
```

## Configure Git User for Each Repository
```bash
cd /path/to/your/harx-dev-repo
git config user.name "harx-dev"
git config user.email "harx-dev@example.com"
```

## Update Remote URLs
```bash
cd /path/to/your/harx-dev-repo
git remote set-url origin git@github-harx:harx-dev/your-repo.git
```

## Verify Account in Use
```bash
git remote -v

git config user.name
git config user.email
```

## Verify SSH Key
```bash
ssh -T git@github-harx
```
