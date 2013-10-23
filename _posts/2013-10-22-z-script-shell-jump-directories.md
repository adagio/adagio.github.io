---
published: true
title: Jump to recently accessed directories with Z script
date: "2013-10-22 17:20"
tags: "script, shell, command line"
---

Get this from [rupa/z in github](https://github.com/rupa/z).

Install this way:

    cd /usr/bin
    sudo curl -O https://raw.github.com/rupa/z/master/z.sh
    sudo chmod 775 z.sh
    . /usr/bin/z.sh
    
Use this way.

1. Access directory `cd /Applications/MAMP/htdocs/greatsite.com`
2. Go to another path, let's say home  `cd ~`
3. Just type "z ww" `z ww`
4. Yes! Now we are in that `/blahblahblah/blehblehbleh/merrychristmas` path

Enjoy it!