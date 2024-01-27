---
layout: page
title:
permalink: /docs/models/model_part/intro
---

<style> span.hidden {visibility: hidden;} </style>

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

<h2 id="index">List of all fields and methods present in any ModelPart object</h2>

Note : examples in each of these methods and fields will use the `player.bbmodel` example file above as a reference.

| Part Transformations                                                          | <span class="hidden">Part Transformations</span>                              |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getPos](/docs/models/model_part/full1#getPos)                                | [setPos](/docs/models/model_part/full1#setPos)                                |
| [getRot](/docs/models/model_part/full1#getRot)                                | [setRot](/docs/models/model_part/full1#setRot)                                |
| [getScale](/docs/models/model_part/full1#getScale)                            | [setScale](/docs/models/model_part/full1#setScale)                            |
| [getPivot](/docs/models/model_part/full1#getPivot)                            | [setPivot](/docs/models/model_part/full1#setPivot)                            |
|                                                                               |                                                                               |
| [getOffsetRot](/docs/models/model_part/full1#getOffsetRot)                    | [setOffsetRot](/docs/models/model_part/full1#setOffsetRot)                    |
| [getOffsetScale](/docs/models/model_part/full1#getOffsetScale)                | [setOffsetScale](/docs/models/model_part/full1#setOffsetScale)                |
| [getOffsetPivot](/docs/models/model_part/full1#getOffsetPivot)                | [setOffsetPivot](/docs/models/model_part/full1#setOffsetPivot)                |
|                                                                               |                                                                               |
| [getTruePos](/docs/models/model_part/full1#getTruePos)                        | [getAnimPos](/docs/models/model_part/full1#getAnimPos)                        |
| [getTrueRot](/docs/models/model_part/full1#getTrueRot)                        | [getAnimRot](/docs/models/model_part/full1#getAnimRot)                        |
| [getTrueScale](/docs/models/model_part/full1#getTrueScale)                    | [getAnimScale](/docs/models/model_part/full1#getAnimScale)                    |
| [getTruePivot](/docs/models/model_part/full1#getTruePivot)                    |                                                                               |

| Appearence                                                                    | <span class="hidden">Appearence</span>                                        |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getVisible](/docs/models/model_part/full2#getVisible)                        | [setVisible](/docs/models/model_part/full2#setVisible)                        |
| [getUV](/docs/models/model_part/full2#getUV)                                  | [setUV](/docs/models/model_part/full2#setUV)                                  |
| [getUVPixels](/docs/models/model_part/full2#getUVPixels)                      | [setUVPixels](/docs/models/model_part/full2#setUVPixels)                      |
|                                                                               |                                                                               |
| [getColor](/docs/models/model_part/full2#getColor)                            | [setColor](/docs/models/model_part/full2#setColor)                            |
| [getPrimaryColor](/docs/models/model_part/full2#getPrimaryColor)              | [setPrimaryColor](/docs/models/model_part/full2#setPrimaryColor)              |
| [getSecondaryColor](/docs/models/model_part/full2#getSecondaryColor)          | [setSecondaryColor](/docs/models/model_part/full2#setSecondaryColor)          |
|                                                                               |                                                                               |
| [getPrimaryRenderType](/docs/models/model_part/full2#getPrimaryRenderType)    | [setPrimaryRenderType](/docs/models/model_part/full2#setPrimaryRenderType)    |
| [getSecondaryRenderType](/docs/models/model_part/full2#getSecondaryRenderType)| [setSecondaryRenderType](/docs/models/model_part/full2#setSecondaryRenderType)|
|                                                                               |                                                                               |
| [getTextures](/docs/models/model_part/full#getTextures)                       | [setPrimaryTexture](/docs/models/model_part/full#setPrimaryTexture)           |
| [getTextureSize](/docs/models/model_part/full#getTextureSize)                 | [setSecondaryTexture](/docs/models/model_part/full#setSecondaryTexture)       |
|                                                                               |                                                                               |
| [getOpacity](/docs/models/model_part/full2#getOpacity)                        | [setOpacity](/docs/models/model_part/full2#setOpacity)                        |
| [getOverlay](/docs/models/model_part/full#getOverlay)                         | [setOverlay](/docs/models/model_part/full#setOverlay)                         |
|                                                                               |                                                                               |
| [getLight](/docs/models/model_part/full#getLight)                             | [setLight](/docs/models/model_part/full#setLight)                             |
| [getUVMatrix](/docs/models/model_part/full2#getUVMatrix)                      | [setUVMatrix](/docs/models/model_part/full2#setUVMatrix)                      |

| Part Properties                                                               | <span class="hidden">Part Properties-----</span>                              |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getParentType](/docs/models/model_part/full1#getParentType)                  | [setParentType](/docs/models/model_part/full1#setParentType)                  |
|                                                                               |                                                                               |
| [getName](/docs/models/model_part/full#getName)                               | [setMidRender](/docs/models/model_part/full#setMidRender)                     |
| [getType](/docs/models/model_part/full#getType)                               | [setPostRender](/docs/models/model_part/full#setPostRender)                   |
| [getParent](/docs/models/model_part/full#getParent)                           | [setPreRender](/docs/models/model_part/full#setPreRender)                     |
| [getChildren](/docs/models/model_part/full#getChildren)                       |                                                                               |
|                                                                               |                                                                               |
| [overrideVanillaPos](/docs/models/model_part/full#overrideVanillaPos)         | [getAllVertices](/docs/models/model_part/full#getAllVertices)                 |
| [overrideVanillaRot](/docs/models/model_part/full#overrideVanillaRot)         | [getVertices](/docs/models/model_part/full#getVertices)                       |
| [overrideVanillaScale](/docs/models/model_part/full#overrideVanillaScale)     |                                                                               |

| Part Transformations via Matrices                                             | <span class="hidden">Part Transformations via Matrices</span>                 |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [partToWorldMatrix](/docs/models/model_part/full#partToWorldMatrix)           | [setMatrix](/docs/models/model_part/full#setMatrix)                           |
| [getPositionMatrix](/docs/models/model_part/full#getPositionMatrix)           |                                                                               |
| [getPositionMatrixRaw](/docs/models/model_part/full#getPositionMatrixRaw)     |                                                                               |
| [getNormalMatrix](/docs/models/model_part/full#getNormalMatrix)               |                                                                               |
| [getNormalMatrixRaw](/docs/models/model_part/full#getNormalMatrixRaw)         |                                                                               |

| Miscellaneous                                           | Fields  <span class="hidden">laneous</span>           |
| ------------------------------------------------------- | ----------------------------------------------------- |
| [newText](/docs/models/model_part/full#newText)         | [preRender](/docs/models/model_part/full#preRender)   |
| [newBlock](/docs/models/model_part/full#newBlock)       | [postRender](/docs/models/model_part/full#postRender) |
| [newItem](/docs/models/model_part/full#newItem)         | [midRender](/docs/models/model_part/full#midRender)   |
| [newSprite](/docs/models/model_part/full#newSprite)     |                                                       |
| [newTask](/docs/models/model_part/full#newTask)         |                                                       |
| [newPart](/docs/models/model_part/full#newPart)         |                                                       |
| [removeTask](/docs/models/model_part/full#removeTask)   |                                                       |
| [getTask](/docs/models/model_part/full#getTask)         |                                                       |
|                                                         |                                                       |
| [addChild](/docs/models/model_part/full#addChild)       |                                                       |
| [moveTo](/docs/models/model_part/full#moveTo)           |                                                       |
| [copy](/docs/models/model_part/full#copy)               |                                                       |
| [removeChild](/docs/models/model_part/full#removeChild) |                                                       |
| [isChildOf](/docs/models/model_part/full#isChildOf)     |                                                       |
