---
type: post
title: Terminal shortcut nixOS (Ctrl+Alt+T)
description: ""
date: 2024-11-09T18:39:50.644Z
preview: ""
draft: false
tags: [NixOS, shortcut, <Ctrl><Alt>t, gnome]
ShowWordCount: true
---


This is a guide to allow you to **open a Gnome terminal in NixOS via a shortcut** (the default one in ubuntu)

First add this config to your `configuration.nix` :
```nix
programs.dconf = {
enable = true;
profiles.user.databases = [
    {
    settings = {
        "org/gnome/settings-daemon/plugins/media-keys" = {
            custom-keybindings = [
                "/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/"
            ];
        };

        "org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0" = {
            binding = "<Ctrl><Alt>t";
            command = "kgx";
            name = "GNOME Console";
        };
    };
    lockAll = true;
    }
];
};
```
Then rebuild nixOS via :
```bash
sudo nixos-rebuild switch
```
And then restart your computer, you're good to go !

*note : you can alway rollback via*
```bash
sudo nixos-rebuild switch --rollback
```


### sources 
[https://discourse.nixos.org/t/what-command-to-open-the-terminal/36148](https://discourse.nixos.org/t/what-command-to-open-the-terminal/36148)
[https://gitlab.com/engmark/root/-/merge_requests/446/diffs](https://gitlab.com/engmark/root/-/merge_requests/446/diffs)