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

[Bash pitfalls](http://mywiki.wooledge.org/BashPitfalls). [don't use the result of ls as a list](http://mywiki.wooledge.org/BashPitfalls#for_f_in_.24.28ls_.2A.mp3.29). [why not parse ls?](https://unix.stackexchange.com/questions/128985/why-not-parse-ls-and-what-to-do-instead).

> If you don't need recursion, you can use a simple glob. Instead of ls

> POSIX shells such as Bash have the globbing feature specifically for this purpose — to allow the shell to expand patterns into a list of matching filenames. There is no need to interpret the results of an external utility. Because globbing is the very last expansion step, each match of the ./*.mp3 pattern correctly expands to a separate word, and isn't subject to the effects of an unquoted expansion.

> Question: What happens if there are no *.mp3-files in the current directory? Then the for loop is executed once, with file="./*.mp3", which is not the expected behavior! The workaround is to test whether there is a matching file:

[starter workflow for GitHub pages](https://github.com/actions/starter-workflows/tree/main/pages). [GitHub Pages now uses Actions by default](https://github.blog/2022-08-10-github-pages-now-uses-actions-by-default/)

[watchman](https://news.ycombinator.com/item?id=33094829)

[the perfect commit](https://lobste.rs/s/tgen6r/perfect_commit)

[Developing on Remote Machines using SSH and Visual Studio Code ](https://lobste.rs/s/x1vu8l/developing_on_remote_machines_using_ssh)

[how to prevent osx from creating a new desktop/space when I fullscreen an app?](https://www.reddit.com/r/osx/comments/ctqaa4/anyone_know_how_to_prevent_osx_from_creating_a/). [mac split view](https://eshop.macsales.com/blog/83087-how-to-use-all-the-awesome-window-management-features-in-macos/)

[Keyboard shortcuts for GNU Readline](https://news.ycombinator.com/item?id=33785631)

[Git rebase --onto an overview](https://womanonrails.com/git-rebase-onto)

[tagref](https://www.reddit.com/r/haskell/comments/zgndwz/comment/izi5p7c/)

> a tool which enforces basic structural invariants regarding notes: (1) references actually refer to notes which exist, and (2) notes have unique names.

[FX Special Effects Image Operator in ImageMagick](http://www.imagemagick.org/script/fx.php)

[Employee Scheduling Software](https://peoplemanagingpeople.com/tools/best-free-employee-scheduling-software/). [ABC Roster](https://www.abc-roster.com/?r=pmp-esss). [Skello](https://www.skello.es/funciones/planificacion). [Software de Gestión de Turnos de Trabajo](https://www.bizneo.com/gestion-turnos/). [sbv](https://hackage.haskell.org/package/sbv) [Microsoft Teams Shifts](https://www.youtube.com/watch?v=7nPuWYC-wFs). [Automatically create shift schedule in Excel](https://www.youtube.com/watch?v=DYBteICNrQI). [Anyone with experience using abc-roster.com tool?](https://www.reddit.com/r/KitchenConfidential/comments/3ii8yq/anyone_with_experience_using_abcrostercom_tool/). [Las 7 mejores herramientas para la gestión de personal](https://www.thepowermba.com/es/blog/herramientas-de-gestion-de-personal). [Gurobi](https://www.gurobi.com/)

> A free software application for employee shift scheduling

> ABC Roster is a free software application especially designed to assist in the complex task of organising employee shift schedules (also known as rosters) for small organisations.

> Microsoft Teams Shifts is a Schedule Management tool

[getsling](https://getsling.com/). [Split Shifts: What Are They And Should You Be Using Them?](https://getsling.com/blog/split-shift/). [How to schedule shifts in Sling](https://www.youtube.com/watch?v=bRgNsZMjj_g). [Auto-assign shifts](https://support.getsling.com/en/articles/5203721-auto-assign-shifts). [7 Ways Automated Scheduling Benefits Modern Business](https://getsling.com/blog/automated-scheduling/)

> https://getsling.com/blog/split-shift/ 

> A split shift is a type of work schedule in which you divide an employee’s workday into two or more parts.

> It’s important to understand that the regular one-hour lunch break associated with a 9-to-5 schedule doesn’t count toward a split shift. A typical split shift is separated by two or more hours.

> As with all scheduling practices, only you, the manager, are allowed to call two separate work periods a split shift. An employee may leave for emergency or personal reasons (with your permission, of course) and then return to finish work, but that is not a split shift.

> Admin and Managers using the Business version of Sling have access to an auto-assign function. 

[9 Best Employee Scheduling Apps For Small Businesses](https://www.clockshark.com/blog/small-business-employee-scheduling-app)

[stacked spaces on Mac](https://twitter.com/t3dotgg/status/1613276064058593280). [rcmd](https://lowtechguys.com/rcmd/).

[close the error output panel on VSCode when it pops up?](https://stackoverflow.com/questions/46242720/what-keyboard-shortcuts-can-i-use-to-close-the-error-output-panel-on-vscode-wh)

> Cmd + j

[Reduce screen motion on Mac](https://support.apple.com/en-gb/guide/mac-help/mchlc03f57a1/mac)

[Make TMUX Look Amazing in 3 Minutes!](https://www.reddit.com/r/vim/comments/10in7wl/a_beautiful_tmux_setup_in_3_minutes/)

[Use spotlight to hop between apps](https://twitter.com/BHolmesDev/status/1620428468776476673)

[Configuring VSCode as a Keyboard-Centric IDE](https://davi.sh/blog/2023/01/vscode-like-emacs/)

[rcmd](https://lowtechguys.com/rcmd/). [things about windows](https://alinpanaitiu.com/blog/window-switcher-app-store/)

[How to combine Spaces & Stage Manager in macOS Ventura](https://appleinsider.com/inside/macos-ventura/tips/how-to-combine-spaces-stage-manager-in-macos-ventura). [Does Stage Manager do anything better than Spaces?](https://www.reddit.com/r/MacOS/comments/ycxl4r/does_stage_manager_do_anything_better_than_spaces/).

[Raycast](https://twitter.com/adamwathan/status/1621170237533200384). [rcmd](https://lowtechguys.com/rcmd/). [raycast tips](https://twitter.com/raycastapp/status/1610305097522892801)

[ Chrome: Keyboard shortcut to leave address bar and focus browsing area?  ](https://apple.stackexchange.com/questions/234706/chrome-keyboard-shortcut-to-leave-address-bar-and-focus-browsing-area)

[raycast quicklinks](https://twitter.com/raycastapp/status/1627595863668281344)

[some VSCode shortcuts](https://hachyderm.io/@DiazCarrete/109921261114588261)

[submodules yay or nay](https://lobste.rs/s/neab1g/never_use_git_submodules)

[vscode when clause contexts](https://code.visualstudio.com/api/references/when-clause-contexts). [PR](https://github.com/microsoft/vscode/issues/59858). list context is the one used in the outline view, it seems. Ctrl-Left collapses all. VSVim adds new shortcuts to list mode.

> UpArrow for Expand Selection in VSCode? If alrady using VSVim, why not? You're already using K for up.

[Why I Stopped Using an External Monitor](https://lobste.rs/s/igiytq/why_i_stopped_using_external_monitor). [HN](https://news.ycombinator.com/item?id=35015277).

[Be Careful Using tmux and Environment Variables](https://lobste.rs/s/j3fxpg/be_careful_using_tmux_environment)

[What a good debugger can do](https://lobste.rs/s/uo3sck/what_good_debugger_can_do)

[control mode in Tmux](https://github.com/tmux/tmux/wiki/Control-Mode). [iterm2 tmux integration](https://iterm2.com/documentation-tmux-integration.html). [iterm2 Shell Integration](https://iterm2.com/documentation-shell-integration.html).  

[Interactuar con texto en una foto con Live Text en la app Vista Previa en el Mac](https://support.apple.com/es-es/guide/preview/prvw625a5b2c/mac)

[So you've installed `fzf`. Now what?](https://andrew-quinn.me/fzf/)

[I use iterm2 and neovim. Is it worth using/adding tmux for local development?](https://news.ycombinator.com/item?id=15778260) NO

[Finder tip](https://hachyderm.io/@DiazCarrete/110072047932252517). [iterm tips](https://hachyderm.io/@DiazCarrete/110069119745145941)

[A Practical Guide to fzf: Shell Integration](https://thevaluable.dev/fzf-shell-integration/). [nixpkgs](https://nixos.wiki/wiki/Fzf)

[Vim paste marks](https://stackoverflow.com/a/10768030/1364288)

> By default, the p and P commands should leave the cursor at the last character of the pasted text. gp and gP go one character forwards (first character after pasted text).

> When you paste text, you have marks [ and ] set to the beginning and end of pasted text. Therefore you can use `[ and `] to move the cursor to begin/end of pasted content. 

[In diff view, there’s a copy path button next to each filename.](https://twitter.com/housecor/status/1643228268093382658)

> one can press the period (.)  key on pull request to bring up the browser-based VS Code environment

[sticky scroll in VSCode](https://twitter.com/andrewculver/status/1642645839876358144)

[Vim-like “jump” cursor for Mac OS Window Management](https://news.ycombinator.com/item?id=35451046)

[⌥+click on css/js paths that don't exist to quickly create that file](https://twitter.com/wesbos/status/1643975015606665218)

[VSCode Terminal Profiles](https://code.visualstudio.com/docs/terminal/profiles)

[Allow Ctrl-P in terminal](https://github.com/microsoft/vscode/issues/95383)

```
    "terminal.integrated.commandsToSkipShell": [
        "-workbench.action.quickOpen"
    ]
```

[VSCode HLS: How to use the eval plugin](https://github.com/haskell/haskell-language-server/issues/425)

VSCode quickfix != Code Lens actions

[pin project files in VSCode](https://stateful.com/blog/15-tips-and-tricks-of-vs-code)

[VSCode: focus next terminal group. ](https://www.youtube.com/watch?v=-p3umsw-HEs)

> Ctrl + PgDown 

[effective spaced repetition](https://news.ycombinator.com/item?id=35511357)

[wrk: Modern HTTP benchmarking tool](https://github.com/wg/wrk)

[Displaying My Washing Machine's Remaining Time with Curl, Jq, and Pizauth](https://news.ycombinator.com/item?id=35536202)

[JSON is YAML](https://alisoftware.github.io/yaml/2021/08/17/yaml-part1-json/).

[iterm - what's the key-combo to switch panes?](https://apple.stackexchange.com/questions/114177/iterm-whats-the-key-combo-to-switch-panes)

[Keyboard tricks from a macOS app dev](https://notes.alinpanaitiu.com/Keyboard%20tricks%20from%20a%20macOS%20app%20dev)


[OBS - Post Production Tools You Can Use](https://obsproject.com/wiki/Post-Production-Tools-you-can-use). how to switch scenes? [nested scenes](https://www.youtube.com/watch?v=Ad1mWf5m_Xs). ["be right back" scene](https://obsproject.com/kb/stream-tutorial-3-brb)

[OBS - browswer source](https://obsproject.com/kb/browser-source)

> Browser source is one of the most versatile sources available in OBS. It is, quite literally, a web browser that you can add directly to OBS. 

[scenes and sources overview](https://obsproject.com/wiki/Sources-Guide#scenes-and-sources-overview)

[from iterm2 back to Terminal](https://news.ycombinator.com/item?id=35673219)

>  I used to use iTerm 2 because I liked its pane management, but after switching to using tmux several years ago, I've solely used Terminal.app + tmux without any issues in my workflow. What am I missing out on?

[jq tricks](https://lobste.rs/s/nhcss0/more_on_comma_as_generator_streaming_with)

[github pages usagle limits](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#usage-limits). [prohibited uses](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#prohibited-uses)

[Building Websites With Jekyll and GitHub](https://carpentries-incubator.github.io/jekyll-pages-novice/). [Introduction to Jekyll](https://ubc-library-rc.github.io/intro-jekyll/).

[more about GH pages & Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll)

> The main types of content for Jekyll sites are pages and posts. A page is for standalone content that isn't associated with a specific date, such as an "About" page. 

> A post is a blog post. The default Jekyll site contains a directory named _posts that contains a default post file. 

[Somehow AutoHotKey is kinda good now](https://lobste.rs/s/hhcros/somehow_autohotkey_is_kinda_good_now)

[MH's setup](https://lobste.rs/s/wucxh0/mitchell_hashimoto_uses_simple_code)

[Split a commit in two with Git](https://emmanuelbernard.com/blog/2014/04/14/split-a-commit-in-two-with-git/). [docs](https://git-scm.com/docs/git-rebase#_splitting_commits)

> In interactive mode, you can mark commits with the action "edit". However, this does not necessarily mean that git rebase expects the result of this edit to be exactly one commit. Indeed, you can undo the commit, or you can add other commits. This can be used to split a commit into two:

> The explained method is good if you want to split a commit in 2 or more new commits. Often one only wants to extract some of the edits but maintain the whole commit more or less like it is. In that case Instead of calling git reset HEAD^ which will unstage the whole index, you can use git reset --soft HEAD^. So the commit will be opened but the files will stay in indexed. It is then possible to unstage selected files with git reset HEAD file... or even better, you can selectively unstage at the patch level with git reset -p HEAD file... (the symetric of git add -p). A git commit -c ORIG_HEAD will commit using the original message which only needs to be edited. That command can be used several times during that edit of the rebase.

> Thanks for the hint about 'git commit -c'. However, I think that when you are stopped in the middle of an (interactive) rebase, you need to specify 'REBASE_HEAD' instead of 'ORIG_HEAD' to use the commit message of the commit you are currently editing.

[Forgot "git rebase --continue" and did "git commit". How to fix?](https://stackoverflow.com/questions/6457044/forgot-git-rebase-continue-and-did-git-commit-how-to-fix)

> Just do git reset --soft HEAD^. It moves the HEAD pointer to its parent but keeps the work tree and adds the merge change to the index. So you can continue rebasing with git rebase --continue as before.

[How do contents of git index evolve during a merge (and what's in the index after a failed merge)?](https://stackoverflow.com/questions/21309490/how-do-contents-of-git-index-evolve-during-a-merge-and-whats-in-the-index-afte)

> For any given path, there are up to four "version numbers" in the index, numbered 0 (zero) through 3. I'll call them "slots" as if they were actually there for every entry, and then easily indexed (this makes them easier to think about), although actually extra versions are introduced dynamically only when needed. These "virtual slots" can be "empty", meaning the file does not exist. [...] Slot #0 is the "normal", un-conflicted, all-is-well entry. It contains a bunch of cache data, the path name, and the blob-ID (the SHA-1) for the file stored in the repository.

> Once you resolve the conflict and "git add", the #0 slot gets filled in with whatever you "add", wiping out the entries in #1 through #3—or, if you "git rm" the conflicted file, the other stage entries are still removed, but now the #0 slot remains empty, which also resolves the conflict.

> [me] During a #git merge conflict, it's the "git add" what removes the slots 1-through-3 from the index, and fills slot 0 for the added file.

> I should also note that git checkout -m will "re-create" a merge conflict, if you're in the middle of a conflicted merge, by erasing slot 0 and "resurrecting" the versions in slots 1-3 as needed (and writing the conflicted merge file to the working directory, obeying any change in your merge.conflictstyle setting as well).

[During a merge, the slot-zero copy winds up in slot 2 (--ours).](https://stackoverflow.com/questions/53652592/git-merge-get-conflicts-as-separate-files-for-merge-with-external-tool)

> The copy of that same file from the merge base goes into slot 1. The copy of that same file from the other commit—the one you're merging—goes into slot 3 (--theirs). Git attempts to combine all three copies, and if Git succeeds on its own, Git puts the combined version in slot zero (and copies it out to the work-tree) and empties out the merge slots. If Git fails, it leaves the merge slots occupied, with slot zero empty.

> Slot zero is left empty (you can't "commit" until you resolve the conflict, by which time this slot won't be empty anymore unless you really want the file to be removed).

[slots are called stage numbers in the official git docs](https://git-scm.com/docs/gitrevisions#Documentation/gitrevisions.txt-emltngtltpathgtemegem0READMEememREADMEem)

> :[<n>:]<path>, e.g. :0:README, :README
A colon, optionally followed by a stage number (0 to 3) and a colon, followed by a path, names a blob object in the index at the given path. A missing stage number (and the colon that follows it) names a stage 0 entry. During a merge, stage 1 is the common ancestor, stage 2 is the target branch’s version (typically the current branch), and stage 3 is the version from the branch which is being merged.

[good explanation of the motivation for git interactive rebase](https://git-scm.com/docs/git-rebase#_interactive_mode)

[YouTube shortcuts](https://www.howtogeek.com/243362/solve-youtubes-spacebar-problem-with-these-keyboard-shortcuts/)

[pbcopy, pbpaste, and other macos commandline goodies](https://news.ycombinator.com/item?id=35937763). [one list](https://ss64.com/osx/)

[umask instead of chmod](https://twitter.com/GabriellaG439/status/1659360924074151936)

[What is Dev Home?](https://learn.microsoft.com/en-us/windows/dev-home/)

[How to do tag wrapping in VS code?](https://stackoverflow.com/questions/40155875/how-to-do-tag-wrapping-in-vs-code)

[Control, Escape, and Meta Tricks](https://susam.net/blog/control-escape-meta-tricks.html)

[cleaning macks](https://twitter.com/nexxeln/status/1670325645111607297)

[moved off iTerm](https://twitter.com/t3dotgg/status/1671246311071559683)

[Use two Mac apps side by side in Split View](https://support.apple.com/en-us/HT204948)

[Advanced macOS Command-Line Tools](https://saurabhs.org/advanced-macos-commands)

[writing a book with markdown](https://news.ycombinator.com/item?id=36582208)

[git - How can I tell if one commit is a descendant of another commit?](https://stackoverflow.com/questions/3005392/how-can-i-tell-if-one-commit-is-a-descendant-of-another-commit)

[thunder client VSCode](https://www.thunderclient.com/)

[Internet Search Tips](https://gwern.net/search)

[vim's <<< EOF](https://twitter.com/learnvim/status/1681692119189139458)

[git notes](https://git-scm.com/docs/git-notes). [Improve your CI-CD-Workflow with Git-Notes](https://medium.com/digitalfrontiers/git-your-stuff-together-storing-test-reports-along-your-sources-with-git-notes-f5c8068dc981). [Git-Notes Your CI Process](https://itnext.io/git-notes-your-ci-process-46b2fd5ac52). [git notes for ci results](https://seankhliao.com/blog/12022-04-21-git-notes-for-ci-results/). [Storing CI data on Git notes](https://euandre.org/til/2020/11/30/storing-ci-data-on-git-notes.html). [Could this be used instead of tags as a CI build marker?](https://news.ycombinator.com/item?id=33767287). [A lot of comments are mentioning using git-notes with CI/CD systems](https://news.ycombinator.com/item?id=33775408). [I've seen implementations of gitops CD pipelines use git notes as a store for](https://news.ycombinator.com/item?id=33766915). [Git notes cheat sheet](https://gist.github.com/topheman/ec8cde7c54e24a785e52). [Git Notes: The Key to Better Collaboration and Code Review](https://levelup.gitconnected.com/git-notes-the-hidden-treasure-for-developers-64594d84dd9c). [Git Notes: git's coolest, most unloved­ feature](https://tylercipriani.com/blog/2022/11/19/git-notes-gits-coolest-most-unloved-feature/). [to speed up CI](https://www.reddit.com/r/programming/comments/zv5p8v/comment/j1oymc0/). [Why does GitHub no longer support git notes?](https://www.quora.com/Why-does-GitHub-no-longer-support-git-notes). [Separating notes by category](https://subscription.packtpub.com/book/programming/9781782168454/5/ch05lvl1sec39/separating-notes-by-category). [Git: Get all notes of a branch](https://stackoverflow.com/questions/20324417/git-get-all-notes-of-a-branch).

[git push --follow-tags](https://git-scm.com/docs/git-push)

[curl host trick](https://twitter.com/mholt6/status/1684962279669035008)

[jq 1.7rc1](https://github.com/jqlang/jq/releases/tag/jq-1.7rc1)

[My Favorite Vim Oneliners For Text Manipulation](https://lobste.rs/s/wqu83x/my_favorite_vim_oneliners_for_text)

> :%!foo replaces the entire buffer with the output of piping the buffer contents to foo.

> :w !foo just pipes the buffer contents to foo and displays the output, leaving the buffer unchanged.

[git rebase --interactive and patch commutation](https://news.ycombinator.com/item?id=37095893)

[navigating code on GitHub](https://docs.github.com/en/repositories/working-with-files/using-files/navigating-code-on-github)

[Tmux has forever changed the way I write code](https://www.youtube.com/watch?v=DzNmUNvnB04). [hn](https://news.ycombinator.com/item?id=37172711).

[init.defaultBranch in Git](https://github.blog/2020-07-27-highlights-from-git-2-28/). [SO question](https://stackoverflow.com/questions/68086082/how-to-find-out-which-of-master-or-main-branches-exists-in-a-repository)

[Find out which remote branch a local branch is tracking](https://stackoverflow.com/questions/171550/find-out-which-remote-branch-a-local-branch-is-tracking)

[mastering the curl command line](https://hachyderm.io/@bagder@mastodon.social/110988491509207488). [video](https://www.youtube.com/watch?v=V5vZWHP-RqU)

[Grep and Log Analysis](https://muhammadraza.me/2023/grep-log-analysis/)

[cheat sheet](https://grahamhelton.com/blog/ssh-cheatsheet/)

[Tmux fuzzy window matching](https://superuser.com/questions/569537/tmux-naming-windows-and-selecting-them-via-fuzzy-matching)

> C-b' (single quote) Prompt for window index to select
> Note this 'window index' wording is a little misleading. This prompt actually accepts target-window which is quite powerful and includes

[Drop git pull for fetch and rebase](https://developers.redhat.com/articles/2023/09/07/drop-git-pull-fetch-and-rebase)

[The Termux Wiki](https://wiki.termux.com/wiki/Main_Page)

From within the VSCode terminal:

```
code $(fzf) 
```

...or copy the path from github and call code with the path.

[org the ultimate API client](https://nikola.plejic.com/blog/org-the-ultimate-api-client/)

[Exploratory Data Analysis Using Awk ](https://news.ycombinator.com/item?id=37792916)

[Why Git is hard](https://roadrunnertwice.dreamwidth.org/596185.html)

[How to Setup Scenes, Sources, and Overlays in OBS](https://www.youtube.com/watch?v=tFmxhBsLEuE)

[HTTPie Desktop: cross-platform API testing client for humans](https://news.ycombinator.com/item?id=37815999)

[ffmpeg](https://twitter.com/FFmpeg/status/1710806212831248886)

[git rebase - what can go wrong?](https://jvns.ca/blog/2023/11/06/rebasing-what-can-go-wrong-/)

[neovim inside tmux inside a tiling wm](https://hachyderm.io/@haskman@functional.cafe/111373395694831212)

[Win-Vind: Vim powers with speed of thought throughout Windows 11](https://news.ycombinator.com/item?id=38236684)

[wslview](https://wslutiliti.es/wslu/). [so](https://superuser.com/a/1600972/185034).

[cursorless](https://news.ycombinator.com/item?id=38214915). [vscode](https://marketplace.visualstudio.com/items?itemName=pokey.cursorless). [Talon](https://talonvoice.com/).

[navigating around your shell](https://lobste.rs/s/0opm7c/navigating_around_your_shell)

[Vim's useful lists](https://codeinthehole.com/tips/vim-lists/)

[Git Branches: Intuition and Reality](https://news.ycombinator.com/item?id=38393238)

[stacked branches](https://twitter.com/jjenzz/status/1727398141123817948). [post](https://andrewlock.net/working-with-stacked-branches-in-git-is-easier-with-update-refs/)

> git rebase -i --update-refs

[squash commits considered harmful](https://dev.to/wesen/squash-commits-considered-harmful-ob1)

[vscode anchors plugin](https://marketplace.visualstudio.com/items?itemName=ExodiusStudios.comment-anchors)

[Fun with git rebase --interactive](https://gurudas.dev/blog/2023/12/02/git-rebase-interactive.html)

Chrome inspect pages

```
chrome://inspect/#pages
```

[the fn key](https://news.ycombinator.com/item?id=38514388)

[Reclaiming the Web with a Personal Reader](https://docs.spring.io/spring-framework/reference/core/beans/factory-scopes.html#beans-factory-scopes-other-injection). [hn](https://news.ycombinator.com/item?id=38622404).

[pspg - Postgres Pager](https://github.com/okbob/pspg)

[Hotkeys for Better Window Management in macOS](https://www.youtube.com/watch?v=VBgVaQscIWg)

[My macOS keyboard shortcuts](https://news.ycombinator.com/item?id=30876934)

[Git Things](https://matklad.github.io/2023/12/31/git-things.html#Git-Things). [hn](https://news.ycombinator.com/item?id=38830194). [should every commit compile?](https://alblue.bandlem.com/2013/08/should-every-commit-compile.html). [https://softwareengineering.stackexchange.com/questions/109107/should-every-git-commit-leave-the-project-in-a-working-state](https://softwareengineering.stackexchange.com/questions/109107/should-every-git-commit-leave-the-project-in-a-working-state).

[Do we think of git commits as diffs, snapshots, and/or histories?](https://jvns.ca/blog/2024/01/05/do-we-think-of-git-commits-as-diffs--snapshots--or-histories/). [hn](https://news.ycombinator.com/item?id=38889100).

> The exact way in which git handles commits is very muddied - it's snapshots on the surface, a bit of diffs when packed

> In my opinion, it's probably good enough to understand the model git is trying to emulate. Commits are stored more or less like snapshot copies of the working tree directory with commit information attached. The fact that there is de-duplication and packing behind the scenes is more a matter of trying to increase storage efficiency than of any practical difference from the directory snapshot model.

[Inside .git](https://jvns.ca/blog/2024/01/26/inside-git/)

[jscpd](https://twitter.com/housecor/status/1751269325313355971)

[jj init](https://lobste.rs/s/pvvbhm/jj_init)

[Managing a merge queue](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/managing-a-merge-queue)

> Merge limits: Select the minimum and maximum number of pull requests to merge in a single group (between 1 and 100), and a timeout after which the queue should stop waiting for more entries and merge with fewer than the minimum number of pull requests. 

[cool log streaming into VSCode?](https://twitter.com/jamesqquick/status/1754554825864249656)

[sticky scroll in VSCode (available both in editor and Workbench)](https://twitter.com/stefanjudis/status/1753114552307224635)

[combining branches in Git](https://wizardzines.com/comics/combining-branches/)

[Does git rebase create more conflicts than git merge?](https://stackoverflow.com/questions/34298273/does-git-rebase-create-more-conflicts-than-git-merge). [Git: Why does rebase result in conflicts while merge does not?](https://stackoverflow.com/questions/38391714/git-why-does-rebase-result-in-conflicts-while-merge-does-not?rq=3). [more](https://stackoverflow.com/questions/16283424/is-it-true-that-rebase-leads-to-a-fewer-number-of-conflicts-than-merge?rq=3). [Is merge without conflicts equivalent to rebase without conflicts? (no)](https://stackoverflow.com/questions/44530822/is-merge-without-conflicts-equivalent-to-rebase-without-conflicts?rq=3). [git merge vs git rebase for merge conflict scenarios](https://stackoverflow.com/questions/59622140/git-merge-vs-git-rebase-for-merge-conflict-scenarios?rq=3). [Git conflicts in rebase vs merge](https://stackoverflow.com/questions/66090607/git-conflicts-in-rebase-vs-merge?rq=3). [more](https://stackoverflow.com/a/54824509/1364288). [in one go](https://www.reddit.com/r/ProgrammerHumor/comments/12pp3et/comment/jgqt6x0/). [thouger to resolve conflicts](https://www.gitkraken.com/learn/git/problems/git-rebase-vs-merge). [more](https://www.donnywals.com/understanding-and-resolving-merge-conflicts/). [post on rerere](https://medium.com/@porteneuve/fix-conflicts-only-once-with-git-rerere-7d116b2cec67)

> With a rebase you run a high risk of having to resolve more conflicts, because two changes to the same codeblock that were done in two different commits might result in two conflicts during rebase, but only one in merge. Think about what happens when H is actually a revert of F.
Even if you have the same number of conflicts, rebasing is still a more tedious process: You have to open the same file multiple to times to resolve conflicts that happened at different commits.

> In my opinion rebase is actually the worse process and while that might be possible I am having trouble imagining a situation where it actually avoids conflicts. 

> One advantage of rebasing is that you can rebase on a portion of the total commits, stabilize, commit resolutions and you now have an atomic unit of progress that can be resumed later. This can be MUCH less daunting. In fact you can rebase some then merge the rest. More flexible.

> When you’re rebasing your branch on a new commit (or branch), you’re replaying every commit on your branch using a new commit as the starting point.

> This can sometimes lead to interesting problems during a rebase where it feels like you’re resolving the same merge conflicts over and over again.

> In reality, your conflicts can keep popping up because each commit will have its own incompatibilities with your new base commit.

[getting better at the keyboard](https://twitter.com/DaschnerS/status/1757015947909489098).

[gits tips and tricks](https://news.ycombinator.com/item?id=39356042)

[github commit statuses using the API](https://docs.github.com/en/rest/commits/statuses?apiVersion=2022-11-28)

[git - trees vs. blobs](https://stackoverflow.com/questions/39400848/in-github-urls-what-is-the-difference-between-a-tree-and-a-blob)

[never-ending txt file](https://news.ycombinator.com/item?id=39432876)

[git show --remerge-diff](https://hachyderm.io/@b0rk@jvns.ca/112003877785470280)

[DuckDB as the New jq](https://lobste.rs/s/x5immj/duckdb_as_new_jq). [hn](https://news.ycombinator.com/item?id=39782356).

[Maybe the easiest way to share HTML, CSS, and JS?](https://youtube.com/shorts/8Pbfxsq1ZN8)

[Double dollar $$() vs Dollar sign $() in Chrome console behavior](https://stackoverflow.com/questions/35682890/double-dollar-vs-dollar-sign-in-chrome-console-behavior)

[how I use git worktrees](https://notes.billmill.org/blog/2024/03/How_I_use_git_worktrees.html)

[Git as a debugging tool](https://news.ycombinator.com/item?id=39877637)

[rebase drama](https://twitter.com/AdamRackis/status/1774471119501660221). [more](https://twitter.com/JLarky/status/1773864713224609800).

[call hierarchy in IDEs](https://twitter.com/peter_a_goodman/status/1316917602934022145)

[Why Don't I Like Git More?](https://lobste.rs/s/mtyqib/why_don_t_i_like_git_more)

[automatic scene switcher in OBS](https://obsproject.com/forum/threads/how-to-record-multiple-windows-and-switch-automatically-between-them.162906/#post-597724) (regular expressions are allowed)

[Quick VS Code tip: skip selections when using Ctrl|Cmd + D](https://dev.to/codepo8/quick-vs-code-tip-skip-selections-when-using-ctrlcmd-d-36me). [tweet](https://twitter.com/kentcdodds/status/1783213095307128972). [vscode speed tips](https://twitter.com/syntaxfm/status/1783169384040878296)

[region folding plugin for VSCode](https://marketplace.visualstudio.com/items?itemName=maptz.regionfolder). [should you split that file?](https://news.ycombinator.com/item?id=38489485)

[how I search in 2024](https://newsletter.vickiboykis.com/archive/how-i-search-in-2024/)

[vscode: skip ctrl-p in terminal](https://github.com/microsoft/vscode/issues/100292). [also ctrl-f](https://stackoverflow.com/questions/68421287/how-to-send-ctrlf-to-shell-in-vs-codes-integrated-terminal). [Terminal basics](https://code.visualstudio.com/docs/terminal/basics). [advanced terminal tricks](https://code.visualstudio.com/docs/terminal/advanced).

[vscode: tab key moves focus](https://stackoverflow.com/questions/77167764/why-is-vs-code-using-the-tab-key-to-move-focus-from-the-integrated-terminal-inst). [github](https://github.com/microsoft/vscode/issues/128858).

[markers in the minimap](https://code.visualstudio.com/docs/getstarted/userinterface#_minimap)

[Principles for Keyboard Layouts](https://news.ycombinator.com/item?id=40186819)

VSCode simple config for recordings:

    "haskell.plugin.ghcide-completions.config.snippetsOn": false,
    "haskell.plugin.importLens.globalOn": false,
    "editor.hover.enabled": false,

[Zen Mode content no longer displays at full screen width](https://github.com/Microsoft/vscode/issues/44794)

>  "zenMode.centerLayout": false

[kdenlive](https://docs.kdenlive.org/)

- [monitors](https://docs.kdenlive.org/en/user_interface/monitors.html)

- [timeline](https://docs.kdenlive.org/en/user_interface/timeline.html#timeline)

- [track header](https://docs.kdenlive.org/en/user_interface/timeline.html#track-header)

[Youtube video chapters](https://support.google.com/youtube/answer/9884579?hl=en)

[multi-root workspaces in vscode](https://code.visualstudio.com/docs/editor/multi-root-workspaces)

[code actions](https://code.visualstudio.com/api/references/vscode-api#CodeActionProvider&lt;T&gt;). [code lenses](https://code.visualstudio.com/api/references/vscode-api#CodeLens). [more about code lenses](https://code.visualstudio.com/blogs/2017/02/12/code-lens-roundup). [in hls](https://haskell-language-server.readthedocs.io/en/latest/features.html#refine-import-code-lens). [short code lenses video](https://www.youtube.com/shorts/A_ggMC7XM8Q).

> code actions typically either fix problems or beautify/refactor code.

> A code lens represents a Command that should be shown along with source text, like the number of references, a way to run tests, etc.

> CodeLens is a popular feature in Visual Studio Code. The essence of the
> feature is "actionable contextual information interspersed" in your source
> code. 

> Shows refined imports and applies them with a click (same as the code action).

[Code Actions = Quick Fixes and refactorings](https://code.visualstudio.com/docs/editor/refactoring#_code-actions-quick-fixes-and-refactorings)

> If you prefer to only see refactorings without Quick Fixes, then you can use the Refactor command (Ctrl+Shift+R).

[ublock origin](https://x.com/SwiftOnSecurity/status/1794748936969715946)

[Demystifying git submodules](https://www.cyberdemon.org/2024/03/20/submodules.html)

[throw away Git submodule state](https://hachyderm.io/@jyn@tech.lgbt/112604949366154042)

[VSCode - using multi cursors like a boss](https://www.youtube.com/watch?v=1V4Lj8Eqdvc)

[why use job control when you have tmux?](https://hachyderm.io/@b0rk@jvns.ca/112716879660246971)

[Extracting and Propagating Multiple Values With #jq](https://x.com/gunnarmorling/status/1809979688670167188)

[Entering text in the terminal is complicated](https://jvns.ca/blog/2024/07/08/readline/)

[how I use Git worktrees](https://lobste.rs/s/rvqez7/how_i_use_git_worktrees)

[compare with VSCode](https://x.com/housecor/status/1817554130782568927)

[Raycast quick links](https://x.com/therealdanvega/status/1820805452193554720)

[ svgl raycast extension](https://x.com/t3dotgg/status/1826503098011189268)

[Using jq to parse and display multiple fields in a json serially](https://stackoverflow.com/questions/28164849/using-jq-to-parse-and-display-multiple-fields-in-a-json-serially)

[git merges and you](https://hackmd.io/@jMIQR1RjR1Sc6kLS4FhQ0w/SJNYSYssi)

[ jq: how to filter an array of objects based on values in an inner array?](https://stackoverflow.com/questions/26701538/jq-how-to-filter-an-array-of-objects-based-on-values-in-an-inner-array)

[Git hygiene](https://x.com/axboe/status/1834295657923825927). [repo](https://github.com/axboe/liburing/blob/master/CONTRIBUTING.md).

> . If you find yourself, in the commit message, adding phrases like "Also do [...]" or "While in here [...]", then that's a sign that the change should have been split into multiple commits.

>  If your change includes some refactoring of code to make your change possible, then that refactoring should be a separate commit, done first. That means this preparatory commit won't have any functional changes, and hence should be a no-op. It also means that your main commit, with the change that you actually care about, will be smaller and easier to review.

[Ultorg](https://www.ultorg.com/)

[cat script.R | llm "what does this code do?"](https://x.com/MarcJBrooker/status/1831731866527039615)

[Chrome dev tools "emulate focused page"](https://x.com/jacobmparis/status/1836424211365282086).

[Notes on using Linear](https://macwright.com/2024/04/09/linear-notes)

[Disable background transparency in (neo)vim](https://stackoverflow.com/questions/46570644/disable-background-transparency-in-neovim)

[In bash how can I change the color of my command prompt?](https://unix.stackexchange.com/questions/16120/in-bash-how-can-i-change-the-color-of-my-command-prompt)

[tput: Portable Terminal Control](https://www.gnu.org/software/termutils/manual/termutils-2.0/html_chapter/tput_1.html). [tput setaf color table? How to determine color codes?](https://unix.stackexchange.com/questions/269077/tput-setaf-color-table-how-to-determine-color-codes)

> The tput command allows shell scripts to do things like clear the screen, underline text, and center text no matter how wide the screen is. To do these things, it translates the terminal-independent name of a terminal capability into its actual value for the terminal type being used.

> The count of colors available to tput is given by tput colors.

[What is the best way now to make super long term backup? (low budget)](https://www.reddit.com/r/DataHoarder/comments/ltryd6/what_is_the_best_way_now_to_make_super_long_term/)

> Keep buying new drives is the easiest way (along with bit rot protection in the meantime). Asking for the same medium to last that long is just adding layers of complexity.

[TIL |& in bash](https://x.com/samwhoo/status/1836679992685584665). [What does "|&" mean in Bash?](https://stackoverflow.com/questions/35384999/what-does-mean-in-bash)

[vscode advanced search options](https://code.visualstudio.com/docs/editor/codebasics#_advanced-search-options)

[youtube shorts links](https://www.reddit.com/r/PartneredYoutube/comments/15q25f8/exciting_update_on_youtube_shorts_now_you_can/). [more](https://www.youtube.com/watch?v=IyOv7Yhxaaw). [more](https://www.youtube.com/watch?v=rffQb5N8c7s).

[btop for process inspection](https://x.com/thorstenball/status/1849800830809145479)

[Bluesky blocks are public](https://blueskyweb.zendesk.com/hc/en-us/articles/15835264007693-Data-Privacy)

[macos cmd utilities](https://weiyen.net/articles/useful-macos-cmd-line-utilities)

[MacBook Pro M4 Max (14-inch, 2024) Setup Guide](https://github.com/danvega/new-macbook-setup/blob/master/2024/README.md)

[Jujutsu Megamerges and jj absorb](https://v5.chriskrycho.com/journal/jujutsu-megamerges-and-jj-absorb/)

[What's like OSX's pbcopy for Linux](https://superuser.com/questions/288320/whats-like-osxs-pbcopy-for-linux#_=_)

[Developing inside a virtual machine](https://news.ycombinator.com/item?id=42541508)

Back and forward in vscode

```
{
  "key": "alt+]",
  "command": "workbench.action.navigateForward",
  "when": "canNavigateForward && activeWebviewPanelId != 'GitHub Copilot Suggestions'"
}
{
  "key": "alt+[",
  "command": "workbench.action.navigateBack",
  "when": "canNavigateBack && activeWebviewPanelId != 'GitHub Copilot Suggestions'"
}
```

[What's involved in getting a "modern" terminal setup?](https://jvns.ca/blog/2025/01/11/getting-a-modern-terminal-setup/)

[Beware tab trapping in VSCode!](https://code.visualstudio.com/docs/editor/accessibility#_tab-trapping)

[self-hosted bookmarks and link sharing](https://github.com/awesome-selfhosted/awesome-selfhosted?tab=readme-ov-file#bookmarks-and-link-sharing)

[terminal weirdness](https://hachyderm.io/@b0rk@jvns.ca/113986551269806331)

[AutoHotKey window switching](https://www.hillelwayne.com/post/ahk/)

[remap vs. send in AutoHotKey](https://www.autohotkey.com/boards/viewtopic.php?style=7&t=69117). [more](https://www.autohotkey.com/docs/v2/misc/Remap.htm#Remap).


