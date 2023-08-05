---
layout: page
title:
permalink: /docs/models
---

<center style="font-size: 3em;">Model</center>

[< Documentation](/docs)

***

&nbsp;

An avatar model usually contains groups, cubes and meshes; all of these are `ModelPart` objects. However, scripts can add "tasks" which includes `BlockTask`, `ItemTask`, `RenderTask`, `SpriteTask` and `TextureTask` objects which are attached to a `ModelPart` object.

All of `ModelPart` objects can be accessed via the `models` table. The table is a collection of all `.bbmodel` files present in your avatar (including those in subfolders.)

Thus, to get a model file called `player.bbmodel` and then get a group called `LeftArm` inside a `Root` group, the indexing will be `models.player.Root.LeftArm`

<figure>
    <img src="/docs/images/player_outliner.png" height="250">
    <figcaption>Outline of the example model file "player.bbmodel" viewed in BlockBench</figcaption>
</figure>

### Examples

```lua
-- Using the same player.bbmodel as above

models.player.Root.RightArm:setColor(0, 0.5, 1) -- Changes color of the RightArm group

L_Arm = models.player.Root.LeftArm -- You can also do this for easier reference
-- From here you can modify the LeftArm group which are now refered as L_Arm instead

L_Arm:setRot(0, 0, 90) -- Rotate the group
L_Arm:setPos(0, -2, 0) -- Move the group
L_Arm:setScale(0, 10, 0) -- Resize the group
```

&nbsp;

***

&nbsp;

| BlockBench's Groups, Cubes and Meshes | Figura's Task Objects &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
|---------------------------------------|------------------------------------------|
| [ModelPart](/docs/models/model_part)  | [BlockTask](/docs/models/block_task)     |
| [Vertex](/docs/models/vertex)         | [ItemTask](/docs/models/item_task)       |
|                                       | [RenderTask](/docs/models/render_task)   |
|                                       | [SpriteTask](/docs/models/sprite_task)   |
|                                       | [TextureTask](/docs/models/texture_task) |
