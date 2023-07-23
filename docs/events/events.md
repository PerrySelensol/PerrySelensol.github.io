---
layout: page
title:
permalink: /docs/events
---

<center style="font-size: 3em;">Events</center>
&nbsp;

***

&nbsp;

Events are objects belonging to `events` table, and have an ability to call your functions when a certain event occurs.

Functions can be registered to an event as follow

```lua
function my_function()
    ... -- Your code here
end

events.TICK:register(my_function, "my_event")
```

Or you can register an anonymous function.

```lua
events.TICK:register(
    function()
        ... -- Your code here
    end,
    "some_named_event"
)
```

A shortcut for this registration is to define an event as if it were a function itself.

```lua
function events.tick()
    ... -- Your code here
end
```

Note that since the shortcut syntax is essentially the same as the regular registration, you can 'define' more than one of these functions unlike other usual functions (although it does look really cursed.)

```lua
-- This is actually valid, and both will get called, but it's very cursed.

function events.use_item()
    ...
end

function events.use_item()
    ...
end
```
&nbsp;

***

## List of all events in Figura

- #### [ENTITY_INIT](/docs/events_full#ENTITY_INIT)

- #### [TICK](/docs/events_full#TICK)

- #### [WORLD_TICK](/docs/events_full#WORLD_TICK)

- #### [RENDER](/docs/events_full#RENDER)

- #### [POST_RENDER](/docs/events_full#POST_RENDER)

- #### [WORLD_RENDER](/docs/events_full#WORLD_RENDER)

- #### [POST_WORLD_RENDER](/docs/events_full#POST_WORLD_RENDER)

- #### [CHAT_SEND_MESSAGE](/docs/events_full#CHAT_SEND_MESSAGE)

- #### [CHAT_RECEIVE_MESSAGE](/docs/events_full#CHAT_RECEIVE_MESSAGE)

- #### [SKULL_RENDER](/docs/events_full#SKULL_RENDER)

- #### [MOUSE_SCROLL](/docs/events_full#MOUSE_SCROLL)

- #### [MOUSE_MOVE](/docs/events_full#MOUSE_MOVE)

- #### [MOUSE_PRESS](/docs/events_full#MOUSE_PRESS)

- #### [KEY_PRESS](/docs/events_full#KEY_PRESS)

- #### [CHAR_TYPED](/docs/events_full#CHAR_TYPED)

- #### [USE_ITEM](/docs/events_full#USE_ITEM)

- #### [ARROW_RENDER](/docs/events_full#ARROW_RENDER)

- #### [ITEM_RENDER](/docs/events_full#ITEM_RENDER)

- #### [ON_PLAY_SOUND](/docs/events_full#ON_PLAY_SOUND)

- #### [RESOURCE_RELOAD](/docs/events_full#RESOURCE_RELOAD)

