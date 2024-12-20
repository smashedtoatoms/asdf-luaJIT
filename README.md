# asdf-luaJIT ![Build](https://github.com/smashedtoatoms/asdf-luaJIT/workflows/Build/badge.svg?branch=master)

LuaJIT plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

This plugin also installs luarocks along with luaJIT.  It is not currently an optional install.  If you need it to be, please let me know.

## Dependencies
1. You will need a compiler.
  * Mac
    1. ```gcc```
    1. Hit the ok button and it will install.  If it already has it, then you are good.
  * Ubuntu
    1. ```sudo apt-get install linux-headers-$(uname -r) build-essential```
1. On Ubuntu, you will need libreadline
  1. ```sudo apt-get install libreadline-dev```

## Install

```
asdf plugin-add luajit https://github.com/smashedtoatoms/asdf-luaJIT.git
```

## ASDF options

Check [asdf](https://github.com/asdf-vm/asdf) readme for instructions on how to install & manage versions of LuaJIT.

When installing LuaJIT using `asdf install`, you can pass custom configure options with the following env vars:

* `LUAJIT_CONFIGURE_OPTIONS` - use only your configure options
* `LUAJIT_EXTRA_CONFIGURE_OPTIONS` - append these configure options along with ones that this plugin already uses
* `LUAROCKS_CONFIGURE_OPTIONS` - use only your configure options
* `LUAROCKS_EXTRA_CONFIGURE_OPTIONS` - append these configure options along with ones that this plugin already uses

# How to use (easier version)
## Install
1. Create your .tool-versions file in the project that needs luaJIT and add `luaJIT 2.0.5` or whatever version that you want.
2. Add a `LUAJIT_EXTRA_CONFIGURE_OPTIONS` and/or
   `LUAROCKS_EXTRA_CONFIGURE_OPTIONS` environment variables with config options
   if you want. _You probably don't want/need to do this._
3. run `asdf install` (if on mac, you now need to set MACOSX_DEPLOYMENT_TARGET,
   so it will look like `MACOSX_DEPLOYMENT_TARGET=15.0 asdf install` for Sequoia
   for example)

## Run
1. Once it is done, run `luajit`.  If it says something about having no version set, make sure you set `luaJIT luaJITVersion` in your ~/.tool-versions file.
