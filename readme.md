# XHLP : compile files, delete the resulting binaries, with only one command.

## **DISCLAIMER** : this is a personal project and is only public so i can show it to my friends. It is in no way officially supported.

## but what's this for ?

xhlp (short for "exercise helper") was made to fill a niche annoyance i had. imagine you have multiple files, as such :

```text
ex1.cpp
ex2.cpp
ex3/q1.cpp
ex3/q2.cpp
```

obviously, you don't wanna compile them one by one. comes xhlp ! simply use `xhlp -c` to compile all files in your current directory that you marked beforehand, simply by writing `!xhlp marker` anywhere in them.  
to clean afterwards, simply use `xhlp -C`.  
and to do this recursively, simply add `-r` to either mode !

more information is available by running `xhlp -h` :)

## more details

### advantages

- only have to run one, short command
- same thing for cleaning !
- compiles in parallel
- deployed as a pacman (for Arch-based distros) or APT (for Debian-based distros) package, so easy to install/uninstall.
- does not leave behind any files, except `.xhlp` in a directory when ran.

### limitations

- long flags (e.g. `--compile`) are not supported
- this is a homemade, quick script ; it's not officially supported.
- you may have to manually handle different file types (e.g. if you need special compiler flags, or need to add a file type)
- not extensively tested (again, this is a script homemade in a few hours)
- does not run on Windows

### dependencies

- bash
- ripgrep
- compilers, depending on which languages you need them for
- usual utilities such as rm, wc...

