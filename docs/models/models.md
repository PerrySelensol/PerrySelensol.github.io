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
    <figcaption>Outline of the example model file "player.bbmodel" viewed in Blockbench</figcaption>
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

<h2 id="object_list">Types of objects in avatar models</h2>

| Blockbench's Groups, Cubes and Meshes      | Figura's Task Objects &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
|--------------------------------------------|------------------------------------------------|
| [ModelPart](/docs/models/model_part/intro) | [BlockTask](/docs/models/block_task/intro)     |
| [Vertex](/docs/models/vertex/intro)        | [ItemTask](/docs/models/item_task/intro)       |
|                                            | [RenderTask](/docs/models/render_task/intro)   |
|                                            | [SpriteTask](/docs/models/sprite_task/intro)   |
|                                            | [TextureTask](/docs/models/texture_task/intro) |
