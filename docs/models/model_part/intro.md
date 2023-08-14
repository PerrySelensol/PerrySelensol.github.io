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

| Getters                                                                       | Setters                                                                       |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| [getPos](/docs/models/model_part/full#getPos)                                 | [setPos](/docs/models/model_part/full#setPos)                                 |
| [getRot](/docs/models/model_part/full#getRot)                                 | [setRot](/docs/models/model_part/full#setRot)                                 |
| [getScale](/docs/models/model_part/full#getScale)                             | [setScale](/docs/models/model_part/full#setScale)                             |
| [getPivot](/docs/models/model_part/full#getPivot)                             | [setPivot](/docs/models/model_part/full#setPivot)                             |
|                                                                               |                                                                               |
| [getUV](/docs/models/model_part/full#getUV)                                   | [setUV](/docs/models/model_part/full#setUV)                                   |
| [getUVPixels](/docs/models/model_part/full#getUVPixels)                       | [setUVPixels](/docs/models/model_part/full#setUVPixels)                       |
| [getColor](/docs/models/model_part/full#getColor)                             | [setColor](/docs/models/model_part/full#setColor)                             |
|                                                                               |                                                                               |
| [getPrimaryRenderType](/docs/models/model_part/full#getPrimaryRenderType)     | [setPrimaryRenderType](/docs/models/model_part/full#setPrimaryRenderType)     |
| [getSecondaryRenderType](/docs/models/model_part/full#getSecondaryRenderType) | [setSecondaryRenderType](/docs/models/model_part/full#setSecondaryRenderType) |
|                                                                               |                                                                               |
| [getPrimaryColor](/docs/models/model_part/full#getPrimaryColor)               | [setPrimaryColor](/docs/models/model_part/full#setPrimaryColor)               |
| [getSecondaryColor](/docs/models/model_part/full#getSecondaryColor)           | [setSecondaryColor](/docs/models/model_part/full#setSecondaryColor)           |
|                                                                               |                                                                               |
| [getUVMatrix](/docs/models/model_part/full#getUVMatrix)                       | [setUVMatrix](/docs/models/model_part/full#setUVMatrix)                       |
| [getOpacity](/docs/models/model_part/full#getOpacity)                         | [setOpacity](/docs/models/model_part/full#setOpacity)                         |
| [getParentType](/docs/models/model_part/full#getParentType)                   | [setParentType](/docs/models/model_part/full#setParentType)                   |
| [getOverlay](/docs/models/model_part/full#getOverlay)                         | [setOverlay](/docs/models/model_part/full#setOverlay)                         |
|                                                                               |                                                                               |
| [getOffsetScale](/docs/models/model_part/full#getOffsetScale)                 | [setOffsetScale](/docs/models/model_part/full#setOffsetScale)                 |
| [getOffsetPivot](/docs/models/model_part/full#getOffsetPivot)                 | [setOffsetPivot](/docs/models/model_part/full#setOffsetPivot)                 |
| [getOffsetRot](/docs/models/model_part/full#getOffsetRot)                     | [setOffsetRot](/docs/models/model_part/full#setOffsetRot)                     |
|                                                                               |                                                                               |
| [getVisible](/docs/models/model_part/full#getVisible)                         | [setVisible](/docs/models/model_part/full#setVisible)                         |
| [getLight](/docs/models/model_part/full#getLight)                             | [setLight](/docs/models/model_part/full#setLight)                             |
|                                                                               |                                                                               |
| [getName](/docs/models/model_part/full#getName)                               | [setMidRender](/docs/models/model_part/full#setMidRender)                     |
| [getType](/docs/models/model_part/full#getType)                               | [setPostRender](/docs/models/model_part/full#setPostRender)                   |
| [getParent](/docs/models/model_part/full#getParent)                           | [setPreRender](/docs/models/model_part/full#setPreRender)                     |
| [getChildren](/docs/models/model_part/full#getChildren)                       | [setMatrix](/docs/models/model_part/full#setMatrix)                           |
|                                                                               |                                                                               |
| [getAnimPos](/docs/models/model_part/full#getAnimPos)                         | [setPrimaryTexture](/docs/models/model_part/full#setPrimaryTexture)           |
| [getAnimRot](/docs/models/model_part/full#getAnimRot)                         | [setSecondaryTexture](/docs/models/model_part/full#setSecondaryTexture)       |
| [getAnimScale](/docs/models/model_part/full#getAnimScale)                     |                                                                               |
|                                                                               |                                                                               |
| [getTruePos](/docs/models/model_part/full#getTruePos)                         |                                                                               |
| [getTrueRot](/docs/models/model_part/full#getTrueRot)                         |                                                                               |
| [getTrueScale](/docs/models/model_part/full#getTrueScale)                     |                                                                               |
| [getTruePivot](/docs/models/model_part/full#getTruePivot)                     |                                                                               |
|                                                                               |                                                                               |
| [partToWorldMatrix](/docs/models/model_part/full#partToWorldMatrix)           |                                                                               |
| [getPositionMatrix](/docs/models/model_part/full#getPositionMatrix)           |                                                                               |
| [getPositionMatrixRaw](/docs/models/model_part/full#getPositionMatrixRaw)     |                                                                               |
| [getNormalMatrix](/docs/models/model_part/full#getNormalMatrix)               |                                                                               |
| [getNormalMatrixRaw](/docs/models/model_part/full#getNormalMatrixRaw)         |                                                                               |
|                                                                               |                                                                               |
| [overrideVanillaPos](/docs/models/model_part/full#overrideVanillaPos)         |                                                                               |
| [overrideVanillaRot](/docs/models/model_part/full#overrideVanillaRot)         |                                                                               |
| [overrideVanillaScale](/docs/models/model_part/full#overrideVanillaScale)     |                                                                               |
|                                                                               |                                                                               |
| [getAllVertices](/docs/models/model_part/full#getAllVertices)                 |                                                                               |
| [getVertices](/docs/models/model_part/full#getVertices)                       |                                                                               |
|                                                                               |                                                                               |
| [getTextures](/docs/models/model_part/full#getTextures)                       |                                                                               |
| [getTextureSize](/docs/models/model_part/full#getTextureSize)                 |                                                                               |

| Miscellaneous                                           |Fields &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;|
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
