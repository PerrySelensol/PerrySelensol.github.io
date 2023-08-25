---
layout: page
title:
permalink: /docs/models/model_part/full
---

<center style="font-size: 3em;">ModelPart Objects</center>

[< ModelPart Objects](/docs/models/model_part/intro)

***

<h1 id="setPos" style="font-size: 2.5em;color:#00008B">setPos</h1>

```lua
HeadPart = models.player.Root.Head:setPos(x, y, z)

HeadPart = models.player.Root.Head:setPos(xyz_vector)
```

Sets the position offset and its pivot for this part from its blockbench position.

### Parameters

Either a *vector* `xyz_vector` or 3 *numbers* `x`, `y`, `z` representing the offset. Nil values are taken as 0.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setPos(1, 2, 3)

models.player.Root.Head:setPos(vec(3, 6, 5))

-- Function chaining example
models.player.Root.Head:setPos(vec(3, 6, 5)):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getPos" style="font-size: 2.5em;color:#00008B">getPos</h1>

```lua
PartPos = models.player.Root.Head:getPos()
```

Gets the position offset of the model part. The values corresponds to the value passed in `setPos()`

### Return Value

Returns a *vector* which is the position offset of the model part.

### Examples

```lua
HeadPos = models.player.Root.Head:getPos()
```
&nbsp;

***

<h1 id="setRot" style="font-size: 2.5em;color:#00008B">setRot</h1>

```lua
HeadPart = models.player.Root.Head:setRot(x, y, z)

HeadPart = models.player.Root.Head:setRot(xyz_vector)
```

Sets the absolute rotation for this part in degrees. The rotations are euler angles in XYZ order (same format as blockbench's.)

### Parameters

Either a *vector* `xyz_vector` or 3 *numbers* `x`, `y`, `z` representing the absolute rotation. Nil values are taken as 0.

### Return Value

Returns *ModelPart* of the model of which the function is called from, so functions can be chained together.

### Examples

```lua
models.player.Root.Head:setRot(30, 45, -60)

models.player.Root.Head:setRot(vec(30, 45, -60))

-- Function chaining example
models.player.Root.Head:setRot(vec(30, 45, -60)):setColor(0, 0.5, 1)
```
&nbsp;

***

<h1 id="getRot" style="font-size: 2.5em;color:#00008B">getRot</h1>

```lua
PartRot = models.player.Root.Head:getRot()
```

Gets the absolute rotation of the model part in degrees. The angles are in euler angles in XYZ order (same as blockbench's.) The values corresponds to the value passed in `setRot()`

### Return Value

Returns a *vector* which is the absolute rotation of the model part.

### Examples

```lua
HeadPos = models.player.Root.Head:getRot()
```
&nbsp;

***
