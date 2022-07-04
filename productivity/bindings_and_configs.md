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

[Set Default WSL Linux Distro in Windows 10](https://winaero.com/set-default-wsl-linux-distro-windows-10/)

> A default WSL Linux distro is a distro that runs when you issue the "wsl"
> command without parameters. Also, it opens from the "Open Linux here" context
> menu command. 

[Working across Windows and Linux file systems](https://docs.microsoft.com/en-us/windows/wsl/filesystems)

>  We recommend against working across operating systems with your files,
>  unless you have a specific reason for doing so. For the fastest performance
>  speed, store your files in the WSL file system if you are working in a Linux
>  command line (Ubuntu, OpenSUSE, etc). If you're working in a Windows command
>  line (PowerShell, Command Prompt), store your files in the Windows file
>  system.

> When you see /mnt/ in the file path of a WSL command line, it means that you
> are working from a mounted drive.  

[How do I uninstall a WSL Distribution?](https://docs.microsoft.com/en-us/windows/wsl/faq#how-do-i-uninstall-a-wsl-distribution-)

[Run Multiple Instances of Same Linux Distro on WSL (Windows 10/11)](https://sungkim11.medium.com/why-you-should-use-multiple-instances-of-same-linux-distro-on-wsl-windows-10-f6f140f8ed88)

> 1. Reset Linux Distro on WSL
> The first step is to create a baseline of your Linux distro/version.

[How to install multiple instances of Ubuntu in WSL2](https://cloudbytes.dev/snippets/how-to-install-multiple-instances-of-ubuntu-in-wsl2). [How to add second WSL2 Ubuntu distro (fresh install)](https://superuser.com/questions/1515246/how-to-add-second-wsl2-ubuntu-distro-fresh-install). [How do you install multiple, separate instances of Ubuntu in WSL?](https://stackoverflow.com/questions/51584765/how-do-you-install-multiple-separate-instances-of-ubuntu-in-wsl). 

[Setting up multiple WSL distribution instances](https://endjin.com/blog/2021/11/setting-up-multiple-wsl-distribution-instances)

> You may notice when you open the environment that it has logged in as the
> root user instead of a custom user that you set up as part of the "base"
> environment. The custom user exists, but is not configured as the default.
> You can either start the environment using:
>
> wsl -d <new distribution name> -u <username>
>
> or you can create/update a wsl.conf file in the /etc directory inside the environment,

When doing the import, remember that you have to provide the directory in which
the new image file will be created.

Editing the wsl.conf file seems to work, before that, you enter the copied image as root.

[Windows Terminal Tips & Tricks](https://docs.microsoft.com/en-us/windows/terminal/tips-and-tricks)

[General profile settings in Windows Terminal](https://docs.microsoft.com/en-us/windows/terminal/customize-settings/profile-general)

[Appearance profile settings in Windows Terminal](https://docs.microsoft.com/en-us/windows/terminal/customize-settings/profile-appearance)

[Disabling swap files creation in vim](https://stackoverflow.com/questions/821902/disabling-swap-files-creation-in-vim)

[Boost Your Coding Fu With Visual Studio Code and Vim](https://www.barbarianmeetscoding.com/blog/boost-your-coding-fu-with-vscode-and-vim)

[How to Change / Set up bash custom prompt (PS1) in Linux](https://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html). [How-to: Setup Prompt Statement variables](https://ss64.com/bash/syntax-prompt.html)

> if [ "$color_prompt" = yes ]; then
>     # PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
>     PS1='\[\033[01;34m\]\W\[\033[00m\]\$ '
> else
>     # PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '
>     PS1='\W\$ '
> fi

[Nix installation on WSL2](https://nixos.wiki/wiki/Nix_Installation_Guide)

> Installation finished!  To ensure that the necessary environment
> variables are set, either log in again, or type
> 
>   . /home/danidiaz/.nix-profile/etc/profile.d/nix.sh

> If you follow those instructions for using WSL2 [...] you can install Nix normally as described in Single-user install. 

What's added to .profile:

> if [ -e /home/danidiaz/.nix-profile/etc/profile.d/nix.sh ]; then . /home/danidiaz/.nix-profile/etc/profile.d/nix.sh; fi # added by Nix installer

[WSL2 port forwarding (video)](https://www.youtube.com/watch?v=ACjlvzw4bVE). [WSL-2: Which ports are automatically forwarded?](https://stackoverflow.com/questions/64513964/wsl-2-which-ports-are-automatically-forwarded). [Connecting to WSL2 server via local network](https://stackoverflow.com/questions/61002681/connecting-to-wsl2-server-via-local-network). [Access a localhost running in Windows from inside WSL2?](https://stackoverflow.com/questions/64763147/access-a-localhost-running-in-windows-from-inside-wsl2). [Sharing network between Windows and WSL apps](https://stackoverflow.com/questions/66328807/sharing-network-between-windows-and-wsl-apps). 

> Services listening on ports in WSL-2 are accesible from the host machine as localhost:<port>

> WSL-2 ports are not accessible from outside of the host machine   

> WSL-2 ports can be made available through netstat interface portproxy or other portforward tools using the ip address of the WSL instance. 

> In WSL2, the instance is running in a Hyper-V VM with a virtual NIC that is NAT'd behind the Windows host. However, the Windows host itself should have direct access to services running in the instance through localhost. WSL appears to do some automatic port-forwarding, but only from the local Windows host to the WSL instance.

[advanced tmux features](https://twitter.com/DiazCarrete/status/1341032047402512384) [How I navigate tmux in 2021](https://waylonwalker.com/tmux-nav-2021/). [playlist](https://www.youtube.com/playlist?list=PLTRNG6WIHETB4reAxbWza3CZeP9KL6Bkr). [interactive window selector fullscreen while in split](https://unix.stackexchange.com/questions/417853/tmux-interactive-window-selector-fullscreen-while-in-split). [The 10 Most Important Commands](https://danielmiessler.com/study/tmux/). [scripting tmux](https://www.arp242.net/tmux.html). [useful subcommands or shortcuts](https://mudongliang.github.io/2017/09/01/tmux-useful-subcommands-or-shortcuts.html). [Super Guide to the split-window tmux Subcommand (and Beyond)](https://steve.dondley.com/super-guide-to-the-split-window-tmux-subcommand-and-beyond/)

>  more advanced features such as hooks, targets and IDs, monitoring and
>  alerts, formats and #(), command sequences, if-shell and run-shell,
>  new/neww/splitw -P and shell scripting with tmux, buffers, capture-pane and
>  pipe-pane, find-window and filters etc in the choose modes, pane titles,
>  terminal-overrides, linking windows and session groups, detach -P,
>  remain-on-exit and exit-unattached and detach-on-destroy, the mouse and
>  advanced key bindings, the new status-format stuff in 2.9, and even menus
>  coming in 3.0.

> The default function for <prefix>w is choose-tree -w

> If you try to find information about starting tmux workspaces you typically
> get advised to use wrapper programs such as tmuxinator, tmux-resurrect, or
> tmux-continuum. These programs may be great, but I like a simple approach. 

[X server on windows + WSL2](https://www.reddit.com/r/bashonubuntuonwindows/comments/hl8lsf/comment/fwxw2t1/). 

> make sure "Disable access control" checkbox is ticked. [:(]

[Inspecting Web Views in macOS](https://news.ycombinator.com/item?id=30648424)

[Developing in WSL](https://code.visualstudio.com/docs/remote/wsl). [WSL 2 with Visual Studio Code](https://code.visualstudio.com/blogs/2019/09/03/wsl2). [Visual Studio Code Remote - WSL](https://www.youtube.com/watch?v=mIHprjsSO9o). 

> Install Visual Studio Code on the Windows side (not in WSL). 

> Opening a terminal in WSL from VS Code is simple. Once folder is opened in
> WSL, any terminal window you open in VS Code (Terminal > New Terminal) will
> automatically run in WSL rather than locally.

> You can also use the code command line from this same terminal window to
> perform a number of operations such as opening a new file or folder in WSL. 

> a console and a shell are different things

[I switched my primary dev environment to a graphical NixOS VM on a macOS host.](https://twitter.com/mitchellh/status/1346136404682625024)

[To flake or not to flake](https://discourse.nixos.org/t/to-flake-or-not-to-flake/10047)

[most useful aliases in your bashrc or zshrc](https://lobste.rs/s/qgqssl/what_are_most_useful_aliases_your_bashrc)

[git rebase -i --exec "cargo fmt" origin/master](https://twitter.com/steveklabnik/status/1508857688108806144). [docs](https://git-scm.com/docs/git-rebase#Documentation/git-rebase.txt---execltcmdgt)

[Mac - How to switch or close the new split Terminal pane?](https://apple.stackexchange.com/questions/87202/how-to-switch-or-close-the-new-split-terminal-pane)

> in general OS-X shortcuts that are done with ⌘ Command-char are undone (or
> the opposite/complement command is executed) with ⌘ Command ⌘ Shift-char.

> You're misinterpreting the feature. It's not meant for two separate
> terminals. It's intended to allow a user to see two different view points in
> the same terminal. For instance, if you have 3000 files in a directory, and
> you perform an ls command, that output is going to be very long.

[VSCode tips and tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)

[Go to symbol in file](https://code.visualstudio.com/docs/editor/editingevolved#_go-to-symbol). [Open symbol by name](https://code.visualstudio.com/docs/editor/editingevolved#_open-symbol-by-name). [Peek](https://code.visualstudio.com/docs/editor/editingevolved#_peek). [Code Navigation](https://code.visualstudio.com/docs/editor/editingevolved).

[List of all available commands in VSCode](https://stackoverflow.com/questions/58367207/list-of-all-available-commands-in-vscode)

> I believe that content of "Preferences: Default Keyboard Shortcuts (JSON)" (command ID workbench.action.openDefaultKeybindingsFile) really shows comprehensive list of all native and extensions-contributed commands VSC knows about at moment when invoked.

> { "key": "ctrl+shift+o",          "command": "workbench.action.gotoSymbol" },

[per-project postgres](https://jamey.thesharps.us/2019/05/29/per-project-postgres/). [direnv](https://lobste.rs/s/uevjtl/direnv_unclutter_your_profile).

[Include diagrams in your Markdown files with Mermaid](https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/)

[VS Code Has Dev Tools & Console!! No Need For Chrome Anymore](https://www.youtube.com/watch?v=vHZPeohPHqo)

[Escaping a git merge hell](https://threkk.medium.com/escaping-a-git-merge-hell-e08f37511f37). [proper use of Git tags](https://news.ycombinator.com/item?id=31480306)

[How to represent bindings in lambda calculus terms where one of the binders binds two names?](https://www.reddit.com/r/haskell/comments/uxidyw/how_to_represent_bindings_in_lambda_calculus/)

[OBS – Open Broadcaster Software ](https://news.ycombinator.com/item?id=31830046)

[In Bash, brace expansion is performed before variable expansion.](https://stackoverflow.com/questions/4956584/sequences-expansion-and-variable-in-bash)

[Bash pitfalls](http://mywiki.wooledge.org/BashPitfalls)


