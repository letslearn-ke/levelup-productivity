+++
title = "Level up Git"
date = 2020-10-12T20:06:46Z
weight = 3
pre = "<b>2. </b>"
+++

## First-Time Git setup.

Now that you have git on your sytem, you'll want to do a few things to customize your environment. You should have to do thes things only once on any given computer. they'll stick around between upgrades. You can also change them at any time by running throught commands again.

git comes with a tool called **git config** that lets you get and set configuration variable that all aspects of how Git looks and operates. These variables can be stored in three different places.

1. **/etc/gitconfig/** file: Contains values applied to every user on the system and all their repositories. If you pass the option **--system** to **git config** , it reads and write from this file specifically.

2. **~/.gitconfig or ~/.config/git/config** file. Values specific personally to you, the user. You can make git read and write to this file by passing the **--global** option, this affects all the repositories you work on your system.

3. **config** file in the Git directory (that is **.git/config**) of whatever repository you're currently using. Specific to that single repository. You can force git to read from and writ to this file with the **--local** option.

On windows system, Git looks for the **.gitconfig** file in the $HOME directory (C:\Users\$USER for most people)

You can view all your settings and where they are coming from using.

```
git config --list --show-origin

```

### Your Identity.

The first thing you should do when you install Git is set your user name and email address. This is important because every Git commit uses this information, and it's immutable baked into the commits you start creating.

```
git config --global user.name "eduuh"
git config --global user.email "edwin@gmail.com"

```

### Your editor.

Now that your identity is set up, you can configure the default text editor that will be used when Git needs you to type in a message.

If not configured, Git uses your system defalt editor.

If you want to use a different text editor, such as **nvim** , you can do the following.

```
git config --global core.editor nvim
```

On a windows system, if you want to use a different text editor, you must specfy the full path to its executabl file. This can be different depending on how your editor is packaged.

```
git config --global core.editor "full path"
```

lets check our setting to ensure they are okay.

#### Checking Your settings.

If you want to check your configuration settings, you can use the **git config --list** command to list all the setting Git can find at that point.

Since Git might read the same configuration variable value form more than one file, it's possible that you have an unexpected value from more that one file. It's possible that you have an expected value for one of these values and you don't know why.

```
git config --show-origin user.name
```

### Getting help.

If you ever need help whil using Git, there are three equivalent ways to get the comprehensive manual page(manpages) help for any of the git commands.

```
git help <verb>
git <verb> --help
man git-<verb>


```

This commands are nice because you can access them anywhere, even offline. I recommend always using **man pages** before google. **google last.**

If you don't need a full blow manpage help, but just need a quick refresher on the available options for a git command. You can ask for the more concise.

