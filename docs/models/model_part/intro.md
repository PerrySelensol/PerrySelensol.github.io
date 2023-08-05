---
layout: page
title:
permalink: /docs/models/model_part/intro
---

<center style="font-size: 3em;">ModelPart Objects</center>

[< Model](/docs/models)

***

&nbsp;

`ModelPart` objects are groups, cubes and meshes of a `.bbmodel` file. They are indexed according to the hierachy it appears in Blockbench.

Thus, if a model file is called `player.bbmodel` which has hierachy as shown below and you want to index `Head` group, then the index is `models.player.Root.Head`

<figure>
    <img src="/docs/images/player_outliner.png" height="250">
    <figcaption>Outline of the example model file "player.bbmodel" viewed in Blockbench</figcaption>
</figure>

&nbsp;

***

<h2 id="index">List of all fields and methods present in ModelPart object</h2>

| Rendering Related                                        | Client Inputs                                                  |
|----------------------------------------------------------|----------------------------------------------------------------|
|||
