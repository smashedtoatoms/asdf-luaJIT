# asdf-luaJIT

LuaJIT plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

This plugin also installs luarocks along with luaJIT.  It is not currently an optional install.  If you need it to be, please let me know.
You specify both versions in the asdf version.  For example, if you want luaJIT 2.0.4 with luarocks 2.4.2, your asdf version will be specified as 2.0.4--2.4.2.

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
asdf plugin-add luaJIT https://github.com/smashedtoatoms/asdf-luaJIT.git
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
1. Create your .tool-versions file in the project that needs luaJIT and add `luaJIT 2.0.4--2.4.2` or whatever version that you want. __Note: the version is luaJITVersion--luarocksVersion__
2. Add a `LUAJIT_EXTRA_CONFIGURE_OPTIONS` and/or `LUAROCKS_EXTRA_CONFIGURE_OPTIONS` environment variables with config options if you want. _You probably don't want/need to do this._
2. run `asdf install`

## Run
1. Once it is done, run `luajit`.  If it says something about having no version set, make sure you set `luaJIT luaJITVersion--luarocksVersion` in your ~/.tool-versions file.