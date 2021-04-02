# homebrew-tap   
Tap Includes:   

  * mc 4.8.25 (because 4.8.26 have bug with custom zsh prompt and can stuck)

...

How to create formula for older version from official formula
https://stackoverflow.com/questions/62785290/installing-previous-versions-of-a-formula-with-brew-extract/64125796#64125796

```
TAP=...     # <org>/<repo>, for example "my-org/homebrew-old"
MODULE=...  # name of module you want to install, e.g. "hugo"
VERS=...    # version of $MODULE you want to install, e.g., "0.80.0"
brew tap-new $TAP
brew extract --version $VERS $MODULE $TAP
brew install $TAP/$MODULE@$VERS
```

