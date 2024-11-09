available here : https://www.simondormeau.com/

# How to use :
1. install Hugo
```powershell
winget install Hugo.Hugo.Extended
git clone git@github.com:sowdowdow/hugo-blog.git
cd .\hugo-blog\
git submodule update --init --recursive # needed when you reclone your repo (submodules may not get cloned automatically)
git submodule update --remote --merge
```

2. run

```powershell
hugo server
```

3. Add an article

```powershell
hugo new content posts/<Y-m-d-title>.md
```
