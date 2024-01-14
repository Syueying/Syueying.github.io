---
layout: post
title: An Alternative Way Installing Homebrew - Using Mirror
date: 2023-02-28 
# description: Alternative solution when official command line for installing homebrew failed
tags: tech terminal macOS
# coverImage: ../assets/img/2023/02/28/screenshot_lazygit.png
permlink: /work/
---

1. Modify homebrew-related environment variables
```
export HOMEBREW_BREW_GIT_REMOTE="https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git"
export HOMEBREW_CORE_GIT_REMOTE="https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git"
export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles"
```

2. Install 
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

3. Configuration
```
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```
