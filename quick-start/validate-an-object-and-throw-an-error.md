---
title: Validate an Object and Throw an Error
description: 
published: true
date: 2023-01-05T09:55:46.242Z
tags: validation
editor: markdown
dateCreated: 2023-01-05T09:37:11.793Z
---

### Validate an Object and Throw an Error

```js
import SimpleSchema from "simpl-schema";

new SimpleSchema({
  name: String,
}).validate({
  name: 2,
});
```