# asdf-luaJIT

LuaJIT plugin for [asdf](https://github.com/asdf-vm/asdf) version manager

## Dependencies
_This requires [brew](http://brew.sh) if you're on a mac, or a debian flavored linux.  If you need it to work on something else, you'll likely need to modify the plugin._

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

# How to use (easier version)
## Install
1. Create your .tool-versions file in the project that needs luaJIT and add `luaJIT 2.0.4` or whatever version that you want.
2. run `asdf install`

## Run
1. Once it is done, run `lua`