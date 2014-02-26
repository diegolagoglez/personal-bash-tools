# Linux Resources #

## Introduction ##

This project has all my Linux resources (tools, scripts, configuration files…) to personalize my environment, which includes:

* `bashrc.d`: BASH configuration files.
* `bin`: Binary tools and scripts.
* `rc`: Linux console configuration files.
* `sublime-text`: Sublime Text configuration and customization files.

## Tools Installation ##

Make a link into your home directory to the binary tools directory. Example:

```bash
user@host:~:$ pwd
/home/user
user@host:~:$ ln -s ~/projects/linux-resources/bin
```

Insert, if needed, your home bin path into PATH environment variable:

```bash
export PATH=$PATH:~/bin
```

## Environment Installation ##

Copy the files into `~/projects/linux-resources/bashrc.d` to any directory you want (I prefer put them into `~/.bashrc.d/`) or link that directory into home with:

```bash
user@host:~:$ ln -s ~/projects/linux-resources/bashrc.d .bashrc.d
```

Then, add the following lines into `~/.bashrc`:

```bash
if [ -d ~/.bashrc.d/ ]; then
  for file in ~/.bashrc.d/*; do
    source $file
  done
fi
```
## Other files ##

There are other files in this repository to configure some commands, like `gitconfig`, `inputrc`… all of them under `rc` directory.

This files should be linked at `/home/user` with their corresponding names, e.g.:

```bash
user@host:~:$ ln -s projects/linux-resources/rc/gitconfig .gitconfig
user@host:~:$ ln -s projects/linux-resources/rc/inputrc .inputrc
```
Also, there are more files to configure other appliactions like Sublime Text. This other files should be linked in their corresponding places.

## Contribution ##

You can use and/or contribute to this configuration but keep in mind the KISS principle.

