# SWGEmu Development Environment setup

****************************************************************************************************************
Special Thanks to lordkator for the initial FastTrack VM Image and the scripts that this repository is based on.
****************************************************************************************************************

## Install Debian 9.x 64bit or Ubuntu 16.x

## Import scripts

Copy this series of commands into a terminal: Installs git, downloads scripts and installs them.

```
sudo apt-get update && sudo apt-get install -y -q git && git clone https://github.com/Scurby/DevEnv.git && cp -i ~/DevEnv/README.md ~/Documents && mkdir setup && mkdir run && cp -r ~/DevEnv/run/* ~/run/ && chmod -v +x ~/DevEnv/bin/* && cat ~/DevEnv/bin/pathto &>> ~/.bashrc
```

## Run scripts

The following scripts are run from the command line. They are numbered in the order I use them.

1. reqd - Installs required packages and programs including Lua, BerkelyDB, and others.
2. setup - Setup of development environment follows these steps:
   * Clone repos and checkout a local branch of Core3 origin/unstable
   * Server configuration
   * Tre files (They will need to be copied or moved)
   * Asks if you want to build and run the server.
3. build - simple build script
   * 3 options- build, build config, build clean
4. start - Builds and runs the development server.
   * Using this command to start the server will:
   * launches the server under gdb on a 'screen'with gdb.
   * outputs a screenlog to ~/run/screenlog*
5. latest - do a quick git-stash, git-pull, and git-stash-apply so you can get to the latest code w/o loosing local work.

****************************************************************************************************************
