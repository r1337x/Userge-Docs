---
title: Writing Your Own Plugin
description: Here are some examples of the syntax for plugins used by UserGe.
---

This guide is more for advanced users looking to unleash the full potential of UserGe by creating their own plugins to assist with their needs. For new users, an understanding of the Python programming language as well as Pyrogram may be needed to make this task easier to understand.

---

## Example Command

```python
from userge import userge, Message

@userge.on_cmd("test", about="help text to this command")
async def test_cmd(message: Message):
   # some other stuff
   await message.edit("testing...")
   # some other stuff
```

## Example Filter

```python
from userge import userge, Message, filters

@userge.on_filters(filters.me & filters.private)
async def test_filter(message: Message):
   # some other stuff
   await message.reply(f"you typed - {message.text}")
   # some other stuff
```
