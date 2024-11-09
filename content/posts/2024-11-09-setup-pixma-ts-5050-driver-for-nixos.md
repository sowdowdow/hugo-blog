---
type: post
title: Setup Pixma TS 5050 driver for NixOS
description: "a quick guide to print from NixOS on a Pixma TS5050"
date: 2024-11-09T11:38:19.690Z
preview: ""
draft: false
tags: [nixOs, PixmaTS5050, TS5050, Printer, Driver]
ShowWordCount: true
---
I struggled to launch a print job from NixOS on My Canon Pixma TS5050.
The solution is actually very simple ([credit to this post](https://medium.com/@f.s.a.kuzman/setting-up-your-local-printer-in-nixos-40c6e1cbb761)).
You just need to add this to you `configuration.nix` :

```nix
{config, pkgs, ... }: 
{
  # ...
  services.printing = {
    enable = true;
    drivers = [ pkgs.cnijfilter2 ];
  
  };
  # ...
}
```

and then rebuild your system with :
`sudo nixos-rebuild switch `

And that's it !


## Environnement 
- Nix 2.18.8
- NixOS 24.05
- Canon Pixma TS5050