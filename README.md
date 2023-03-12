## Lua unit test example

This is a simple example of how to use the Lua unit test framework.

### install the unit test framework
    1. download luarocks from https://github.com/luarocks/luarocks/wiki and install it.
    2. luarocks install package for redis, `for i in luacov busted redis-lua lua-cjson; do luarocks install $i --local; done`
        - luacov is a code coverage tool
        - busted is a unit test framework
        - redis-lua is a redis client
        - lua-cjson is a redis cjson
    3. run busted, if busted command not found, add `~/.luarocks/bin` to your PATH, see https://github.com/exercism/lua/blob/main/docs/INSTALLATION.md 

### run the unit test
    1. run `busted` in the root directory of this project, you will see the test result.
        - busted -c , run the test with code coverage
    2. run `luacov` in the root directory of this project, you will see the code coverage report.
        - luacov '^word_count.lua' && cat luacov.report.out, run the code coverage with a filter
        - luacov '^lib.bob.lua' && cat luacov.report.out, run the code coverage with a filter

