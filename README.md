available here : https://blog.sdormeau.com/

# Setup
## install Hugo

Windows
```powershell
winget install Hugo.Hugo.Extended
```

NixOS
```bash
nix-shell -p hugo
```

Clone
```bash
git clone git@github.com:sowdowdow/hugo-blog.git
cd .\hugo-blog\
git submodule update --init --recursive # needed when you reclone your repo (submodules may not get cloned automatically)
git submodule update --remote --merge
```

## Setup VSCode
install `Front Matter CMS` extension

## Launch preview
```powershell
hugo server
```

## Create an article
```powershell
hugo new content posts/<Y-m-d-title>.md
```
