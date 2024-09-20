## Getting Started
```bash
ssh-keygen -t ed25519 -C "user@gmail.com" -f ~/.ssh/id_ed25519_first_github
```

## Add SSH Keys to SSH Agent
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519_first_github
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
cd /path/to/your/user-repo
git config user.name "Username"
git config user.email "user@gmail.com"
```

## Update Remote URLs
```bash
cd /path/to/your/harx-dev-repo
git remote set-url origin git@github-user:-Username/your-repo.git
```

## Verify Account in Use
```bash
git remote -v

git config user.name
git config user.email
```

## Verify SSH Key
```bash
ssh -T git@github-Username
```
