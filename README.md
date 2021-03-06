md5.lua [![Build Status](https://travis-ci.org/kikito/md5.lua.svg)](https://travis-ci.org/kikito/md5.lua)
=========================================================================================================

This pure-Lua module computes md5 in Lua 5.1, Lua 5.2 and LuaJIT, using native bit-manipulation libraries when available, and falling back to table-based manipulation of integers in 5.1.

It implements md5.sum and md5.sumhex like the [kernel project md5 package](http://www.keplerproject.org/md5/), but it's done completely in Lua, with no dependencies on other libs or C files.

Usage
=====

    local md5 = require 'md5'

    local md5_as_hex   = md5.sumhexa(message)   -- returns a hex string
    local md5_as_data  = md5.sum(message)     -- returns raw bytes

Credits
=======

This is a cleanup of an implementation by Adam Baldwin - https://gist.github.com/evilpacket/3647908

Which in turn was a mix of the bitwise lib, http://luaforge.net/projects/bit/ by hanzhao (`abrash_han - at - hotmail.com`),
and http://equi4.com/md5/md5calc.lua, by Equi 4 Software.

Lua 5.2 and LuaJIT compatibility by [Positive07](https://github.com/kikito/md5.lua/pull/2)


License
=======

This library, as well as all the previous ones in which is based, is released under the MIT license (See license file for details).

Specs
=====

The specs for this library are implemented with [busted](http://ovinelabs.com/busted/). In order to run them, install busted and then:

    cd path/to/where/the/spec/folder/is
    busted




