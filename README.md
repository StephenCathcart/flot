# Flot

A tiny [Flot](https://www.flotcharts.org/) plotting library for Lua. Forked from [Lua Flot](https://github.com/stevedonovan/stevedonovan.github.com/blob/master/lua-flot/flot.lua)

## Installation
The flot.lua file should be dropped into an existing project and required by it.

```lua
local flot = require("flot")
```

## Usage

Basic plotting is very similar to the original Flot API:

```lua
-- basic-flot.lua
local flot = require('flot')

local sin, cos = {}, {}
for i = 1, 100 do
    local x = i / 10
    sin[i] = {x, math.sin(x)}
    cos[i] = {x, math.cos(x)}
end
local p = flot.Plot { -- legend at 'south east' corner
    legend = {position = 'se'}
}
p:add_series('sin', sin)
p:add_series('cos', cos, {color = '#000'})
flot.render(p)
```

Running this program will create a corresponding basic-flot.html which you can open in your browser.

![Flt](/example/example.png)
