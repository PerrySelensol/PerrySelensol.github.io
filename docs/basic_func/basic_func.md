---
layout: page
title: "Basic Functions"
permalink: /docs/basic_func
---

***

<h2><span>print(</span><span style="color:blue">···</span><span>)</span></h2>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A function that writes its arguments to chat. Each of the argument printed will be separated by a tab space

Returns the string representation of all values

### Examples
```
print("Hello World!")
print("A string", "Another string", 2023, "So many arguments")
```

## listFiles(String folder, Boolean IncludeSubfolders)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A function that returns a table with all script file names from the specified path. If no path is specified, it will fetch from the root folder. A second boolean argument can be given to also list files inside subfolders

### Examples

Assuming part of your script files are located inside `scripts/some_module` folder

```
local file_list = listFiles("scripts.some_module")
printTable(file_list)
```

To print every script file present in your avatar

```
printTable(listFiles("", true))
```