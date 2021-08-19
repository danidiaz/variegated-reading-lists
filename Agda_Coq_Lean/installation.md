# Agda

Installed on Windows.

Used cabal new-install.

Had to do it from Git Bash, compilation failed from Powershell.

Symlink creation failed, had to localte the Agda packages in ~/AppData/Roaming/cabal/store/...

emacs agda-mode automatic installation failed, but adding the lines manually to .emacs did the trick.

Standard library has to be downloaded separately form [here](https://github.com/agda/agda-stdlib/tree/v0.16.1). Then I followed [these instructions](https://agda.readthedocs.io/en/latest/tools/package-system.html).

# Coq

## proof-general

As of 20/09/2018, use the "async" branch of proof-general.

I installed by cloning the git repo, not through MELPA.
