---
layout: page
title:
permalink: /docs/basic_func_full
---

<center style="font-size: 3em;">Basic Functions</center>
&nbsp;

***

<h1 id="print" style="font-size: 2.5em;color:#00008B">print</h1>

`print(···)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A function that writes its arguments to chat. Each of the argument printed will be separated by a tab space.

Returns the string representation of all values.

### Examples
```lua
print("Hello World!")
print("A string", "Another string", 2023, "So many arguments")

print(print("This is really cursed but it does work"))
```
&nbsp;

***

<h1 id="listFiles" style="font-size: 2.5em;color:#00008B">listFiles</h1>

`listFiles(String path, Boolean includeSubfolders)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A function that returns a table with all script file names from the specified `path`. If no path is specified, it will fetch from the root folder. An optional second boolean argument `includeSubfolders` can be given to also list files inside subfolders.

### Examples

Assuming part of your script files are located inside `scripts/some_module` folder

```lua
local file_list = listFiles("scripts.some_module") -- Excluding Subfolders
local deep_list = listFiles("scripts.some_module", true) -- Including Subfolders

printTable(file_list)
printTable(deep_list)
```

To print every script file present in your avatar

```lua
printTable(listFiles("", true))
```
&nbsp;

***

<h1 id="require" style="font-size: 2.5em;color:#00008B">require</h1>

`require(String scriptName, Function fallbackFunction)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The function runs `scriptName` file and return the value that the file returns or `true` if there isn't any (as a lua script file is essentially a one big function). If the script file has already run, then it only returns the value the file initially returned.
If `scriptName` is invalid, then `fallbackFunction` will be called instead.

### Examples

Assuming there is a file called `foo` in `scripts/bar`

```lua
-- This is a code in scripts/bar/foo

print("foo has run")

return "the string of foo"
```

Then run the following code

```lua
local x = require("scripts.bar.foo",
    function() print("Task X failed successfully") end
) --> x should now be "the string of foo"

print(x) --> does print "the string of foo"

local y = require("scripts.bar.faz",
    function() print("Task Y failed successfully") end
) --> y is nil and "Task Y failed successfully" is printed

print(y) --> nil
```
&nbsp;

***

<h1 id="printJson" style="font-size: 2.5em;color:#00008B">printJson</h1>

`printJson(···)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Takes Minecraft json strings arguments, and prints all of them to the chat formatted, without the lua print header. All of the arguments will be concatenated together. Returns the formatted string.

### Examples

```lua
printJson(
    '{"text":"Red","color":"red"}',
    '[{"text":"Blue","color":"blue"},{"text":"Green","color":"green"}]'
)
```

The output should be <span style="color:red">Red</span><span style="color:blue">Blue</span><span style="color:green">Green</span>
&nbsp;

***

<h1 id="printTable" style="font-size: 2.5em;color:#00008B">printTable</h1>

`printTable(Object object, Integer depth, Boolean silent)`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Prints an object as a formatted string. The `object` can be a lua table or any object type that Figura mod adds (such as vectors, matrices and modelPart.) The optional `depth` argument can also be passed to also print deeper entries in a table or Figura objects, and the boolean `silent` can be passed to prevent formatted result from appearing in chat.

The function always returns the formatted string.

### Examples

```lua
local Table = {
    value = 42,
    array = {2,7,1,4},
    text = "tabler table!"
}

printTable(Table) --> prints value, array and text but not the contents of array

printTable(Table, 2) --> prints value, array, text AND the contents of array

-- Store formatted result without it being printed into chat
local result = printTable(Table, 2, true)
```
