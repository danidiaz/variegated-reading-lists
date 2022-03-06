[readline cheat sheet](https://readline.kablamo.org/emacs.html)

>  Ctrl-] Search forwards for a single character in the current line and jump to that location.

[GitHub - generating SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

> prefer Ed25519

[Install WSL](https://docs.microsoft.com/en-us/windows/wsl/install)

[Set up a WSL development environment](https://docs.microsoft.com/en-us/windows/wsl/setup/environment#set-up-your-linux-username-and-password)

[Advanced settings configuration in WSL](https://docs.microsoft.com/en-us/windows/wsl/wsl-config)

> .wslconfig to configure settings globally across all installed distributions running on WSL 2.
> Stored in your %UserProfile% directory.

> wsl.conf to configure settings per-distribution for Linux distros running on WSL 1 or WSL 2
> Stored in the /etc directory of the distribution as a unix file.

[Basic commands for WSL](https://docs.microsoft.com/en-us/windows/wsl/basic-commands)

[Run Multiple Instances of Same Linux Distro on WSL (Windows 10/11)](https://sungkim11.medium.com/why-you-should-use-multiple-instances-of-same-linux-distro-on-wsl-windows-10-f6f140f8ed88)

> 1. Reset Linux Distro on WSL
> The first step is to create a baseline of your Linux distro/version.

[How to install multiple instances of Ubuntu in WSL2](https://cloudbytes.dev/snippets/how-to-install-multiple-instances-of-ubuntu-in-wsl2). [How to add second WSL2 Ubuntu distro (fresh install)](https://superuser.com/questions/1515246/how-to-add-second-wsl2-ubuntu-distro-fresh-install). [How do you install multiple, separate instances of Ubuntu in WSL?](https://stackoverflow.com/questions/51584765/how-do-you-install-multiple-separate-instances-of-ubuntu-in-wsl). [Setting up multiple WSL distribution instances](https://endjin.com/blog/2021/11/setting-up-multiple-wsl-distribution-instances)

> You may notice when you open the environment that it has logged in as the
> root user instead of a custom user that you set up as part of the "base"
> environment. The custom user exists, but is not configured as the default.
> You can either start the environment using:
>
> wsl -d <new distribution name> -u <username>
>
> or you can create/update a wsl.conf file in the /etc directory inside the environment,

[Windows Terminal Tips & Tricks](https://docs.microsoft.com/en-us/windows/terminal/tips-and-tricks)

[General profile settings in Windows Terminal](https://docs.microsoft.com/en-us/windows/terminal/customize-settings/profile-general)

[Appearance profile settings in Windows Terminal](https://docs.microsoft.com/en-us/windows/terminal/customize-settings/profile-appearance)

[Disabling swap files creation in vim](https://stackoverflow.com/questions/821902/disabling-swap-files-creation-in-vim)


