# ATOMICGULP
#### Helper Aliases for Opening Projects and Running Build Tasks

This is a set of easy bash aliases to prompt for a directory to `cd` into, open the project in a text editor, and run a typical JS build script. The build scripts here are for `gulp`, `grunt`, `npm`, and `node`. When running the alias targeting `npm` or `node`, you will also be prompted for the command (`start`, `dev`, etc) or app root (`server.js`, `app.js`, etc).

Currently the aliases open Atom or Sublime Text, but feel free to adjust these to any other editor that you launch from the CLI! Aliases include:

* atomicgulp
* atomicgrunt
* atomicnpm
* atomicnode
* sublimegulp
* sublimegrunt
* sublimenpm
* sublimenode

#### Usage

Add the aliases to your `.bashrc` or `.bash_profile`, and run `.source bash_profile` or `source .bashrc`. Now you're free to `atomicgulp` or `sublimegrunt` anywhere that works for you!


### Atomic Gulp

```
# cd && atom && gulp
function atomicgulp(){
  read -e -p "Enter Project Directory: " inputpath
  cd "$inputpath" && atom . && gulp
}
```

### Atomic Grunt

```
# cd && atom && grunt
function atomicgrunt(){
  read -e -p "Enter Project Directory: " inputpath
  cd "$inputpath" && atom . && grunt
}
```

### Atomic NPM

```
# cd && atom && npm start
function atomicnpm(){
  read -e -p "Enter Project Directory: " inputpath
  read -e -p "Enter NPM command to run: NPM +" npmcmd
  cd "$inputpath" && atom . && npm "$npmcmd"
}

```

### Atomic node

```
# cd && atom && node filename
function atomicnode(){
  read -e -p "Enter Project Directory: " inputpath
  read -e -p "Enter App Root for Node: " approot
  cd "$inputpath" && atom . && node "$approot"
}

```


### Sublime Gulp

```
# cd && sublime && gulp
function sublimegulp(){
  read -e -p "Enter Project Directory: " inputpath
  cd "$inputpath" && subl . && gulp
}
```

### Sublime Grunt

```
# cd && sublime && grunt
function sublimegrunt(){
  read -e -p "Enter Project Directory: " inputpath
  cd "$inputpath" && subl . && grunt
}
```

### Sublime NPM

```
# cd && sublime && npm start
function sublimenpm(){
  read -e -p "Enter Project Directory: " inputpath
  read -e -p "Enter NPM command to run: NPM +" npmcmd
  cd "$inputpath" && subl . && npm "$npmcmd"
}
```

### Sublime node

```
# cd && sublime && node filename
function sublimenode(){
  read -e -p "Enter Project Directory: " inputpath
  read -e -p "Enter App Root for Node: " approot
  cd "$inputpath" && subl . && node "$approot"
}

```


# TO-DO

* present interactive options to prompt for build script or editor?
* execute command with default flags vs `read` prompts
