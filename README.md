# repos

This meta-repo contains a tree of my development repos that I want to have available offline.
To download everything:

```console
git clone https://github.com/vogler/repos ~/dev && cd ~/dev
git submodule update --init --recursive
```

Name: locally it may have some uncommitted files, so I prefer `dev` for development over generic `repos`.

## Structure

Flat list of repos got confusing, but arbitrary nesting also is, so limit to two levels (category > repos).
Directories starting with uppercase character are *categories* which are listed first by `ls`.
See `.info` for descriptions of abbreviations / what should go inside.
For quicker access, use symlinks to nested repos.

```console
$ tree -L 2 -d --info
.
├── Git
│    { Tools for working with git
│   ├── repo-issues
│   └── repoman
├── HW
│    { Hardware projects: ESP, IoT, electronics, sensors, 3D printing
│   ├── LED-matrix
│   ├── SmartLock
│   ├── esp-distance-sensor
│   └── smart-home
├── PL
│    { Programming languages: type system examples, extensions
│   ├── OCaml
│   ├── lang
│   └── vadt
├── Tech
│    { Technologies: evaluate frameworks, libraries, tools...
│   └── web.tech
├── Web
│    { Web projects: sync data, automate
│   ├── epaper-downloader
│   ├── free-games-claimer
│   ├── swm
│   └── syncmine
├── WebExtensions
│    { Browser extensions: use WebExtensions API for Chrome/Firefox
│   ├── quick-start
│   ├── tablog
│   ├── tabman
│   └── tabtime
└── tasks -> Tech/web.tech/tasks/track-time_snowpack-react-chakra-prisma
```
